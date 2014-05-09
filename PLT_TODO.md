## PLT TODO LIST

+ ~~Change PLTU.h to reflect pixel geometry in silicon~~
+ Make sure there is a threshold of 4000 electrons.  For this, add this to PLTSimHitAnalyzer so these hits don't get written to the text file in the first place.
    + ~~For existing files, get rid of those lines below threshold~~
+ Figure out how to convert text digi format to binary
    + Afterward, send the binary file to Keith to see if it works with the LumiDAQ software
+ Make an alignment file for simulation
