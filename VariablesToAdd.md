### Variables with branches created but not filled in BTagAnalyzer

+ trackPtRel
+ trackEtaRel
+ trackDeltaR
+ trackPtRatio
+ trackJetDist
+ trackDecayLenVal
+ trackSumJetEtRatio
+ trackSumJetDeltaR

### Variables I added and were successfully written to the ntuple

+ trackSip2dSigAboveCharm
+ chargedHadronMultiplicity
+ neutralHadronMultiplicity
+ photonMultiplicity
+ chargedHadronEnergyFraction
+ muonEnergyFraction

### Variables I added but were NOT successfully written to the ntuple

Both of these are failing the checkTag method...why?
+ trackSip3dValAboveCharm
+ trackSip2dValAboveCharm


### Variables already added before I began:

+ TrackSip3dVal (Track_IP)
+ TrackSip3dSig (Track_IPsig) (note that errors are also included for both 2 and 3D)
+ TrackSip2dVal (Track_IP2D)
+ TrackSip2dSig (Track_IP2Dsig)
+ trackSip3dSigAboveCharm (SV_AboveC)
+ nTracks (Jet_ntracks)
+ VertexNTracks (SV_nTrk) (assuming this means secondary vertex)
+ VertexMass (SV_mass) (assuming this means secondary vertex)
+ vertexEnergyRatio (SV_energy_ratio) (assuming vertex == SV)
+ VertexFitProb (SV_chi2, SV_ndf)
+ VertexJetDeltaR (SV_deltaR_jet)
+ FlightDistance3dSig (SV_flight, SV_flightErr)
+ FlightDistance2dSig (SV_flight2D, SV_flight2DErr)
+ jetPt (Jet_pt)
+ jetEta (Jet_eta)
+ jetNSecondaryVertices (Jet_SV_multi)
