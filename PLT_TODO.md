## PLT TODO LIST

+ Generate muon gun events with all combinations of the following:
    + pT in (0.5,5,50)
    + eta in (center of ch. 9, full range)
    + phi in (center of ch. 9, full range)
    + z in (keep at 0, sigmaz=5.3)
+ Make an alignment file for simulation
+ ~~Set up code to be able to study 3-fold coincidence rate as a function of pileup~~
    + Make up own PU distribution to pick exactly the number you want (or find more elegant way to do this)
    + Alternatively: use PileupInfoSummary object (but low statistics for nPU far away from the mean)
    + ### Neither of the above are implemented easily at this point, but what I did was to use my own generated events as pileup for themselves (see the code).
