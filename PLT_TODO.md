## PLT TODO LIST

+ ~~Generate muon gun events with all combinations of the following:~~
    + ~~pT in (0.5,5,50)~~
    + ~~eta in (center of ch. 9, full range)~~
    + ~~phi in (center of ch. 9, full range)~~
    + ~~z in (keep at 0, sigmaz=5.3)~~
    + UPDATE: ridiculous amount of muon gun scenarios in EOS now.
+ Analyze 3-fold coincidence rates as fn. of pileup
    + Lots of nPU data points on the low end (i.e. nPU=1,2,3,5,10,...), not so many on the high end
    + Edit PLTSimHitAnalyzer to be able to make these plots
    + Enact stricter definition of 3-fold coincidence, namely:
        + All 3 planes fired PLUS having a hit in ROC0 that points to the beamspot with some precision
    + Possibly repeat analysis for multiple beamspot scenarios and various definitions for what it means to 'point to the beamspot'
    + ~~**Fix the error bars on the 3 fold coincidence plots**~~
    + ~~**Plot 3 fold coincidence rate without cylinder constraint**~~
    + ~~**Plot 3 fold coincidence rate where ROC0 hit does NOT match to the cylinder**~~
    + ~~**Plot rMin going way out in r so that there is no overflow (with x-axis on log scale)**~~
        + Note: plotted zMin v. rMin, info is encapsulated in these plots 
    + ~~**For all 3 fold coincidence plots: Don't use L option when drawing, do linear fit instead!!!**~~
    + ~~**Plot |zMin| vs. rMin for all tracks for all p, low p (<1 GeV), and high p(>1 GeV)**~~
        + ~~**For each case, also plot the 3 fold coincidence rate vs. nInteractions**~~
+ Make sure the alignment file makes sense
+ Fit mustache from muon gun to get handle on accidentals:
    + More specifically need to generate muons with energy distribution from minBias, not just flat
    + Get the mustache shape from this muon setup (why? no accidentals expected, that's why!)
    + Fit as (possibly) Sy = c0 + c1*Sx^2 + c2*Sx^4 (maybe HOT as well? hope not..)
        + No even terms because we don't need a wiggly mustache, just a mustache
    + Transform mustache using this fit
        + i.e. for all points, Sy -> Sy' = Sy - c1*Sx^2 + c2*Sx^4
        + This should give Sy' vs. Sx a flat look (with some spread)
    + Cut on Sx in a range that contains the mustache (all tracks outside this range are for sure accidental)
        + Yes, this is arbitrary, BUT go far away from the mustache, cut outside this range, but also realize that there are accidentals inside of the mustache also.  Hopefully the accidentals are constant in Sx (i.e. Sx is a peak on top of a constant background, cut far from the peak to see how high the background is and extrapolate to get the accidentals throughout the whole range   
    + Cut on Sy' (i.e. the width of the mustache)
        + Yes, this is arbitrary, BUT go far away from the mustache, cut outside this range, but also realize that there are accidentals inside of the mustache also.  Hopefully the accidentals are constant in Sy' (i.e. Sy' is a broad bump on top of a constant background, cut far from the bump to see how high the background is and extrapolate to get the accidentals throughout the whole range 
+ ~~Set up code to be able to study 3-fold coincidence rate as a function of pileup~~
    + Make up own PU distribution to pick exactly the number you want (or find more elegant way to do this)
    + Alternatively: use PileupInfoSummary object (but low statistics for nPU far away from the mean)
    + **Neither of the above are implemented easily at this point, but what I did was to use my own generated events as pileup for themselves (see the code).**
