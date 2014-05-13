## PLT TODO LIST

+ ~~Change PLTU.h to reflect pixel geometry in silicon~~
+ Make sure there is a threshold of 4000 electrons.  For this, add this to PLTSimHitAnalyzer so these hits don't get written to the text file in the first place.
    + ~~For existing files, get rid of those lines below threshold~~
+ Figure out how to convert text digi format to binary
    + Afterward, send the binary file to Keith to see if it works with the LumiDAQ software
+ Make an alignment file for simulation
+ Set up code to be able to study 3-fold coincidence rate as a function of pileup
    + Make up own PU distribution to pick exactly the number you want (or find more elegant way to do this)
    + Alternatively: use PileupInfoSummary object (but low statistics for nPU far away from the mean)
