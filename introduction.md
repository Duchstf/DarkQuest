# Introduction to DarkQuest

<p align="left">
  <img src="/images/darkquest.png" width="200" alt="DarkQuest">
</p>

DarkQuest is a proton fixed-target experiment especially sensitive to visible dark sector signatures in MeV-GeV mass range. 
It proposes a few low-cost upgrades to existing detectors from the SeaQuest/SpinQuest (E-1039) Fermilab fixed target beam-dump experiment.

# Theory and Experimental moitvation 

## Dark sector signatures

DarkQuest will directly search for the decays of unstable mediators and dark states to visible Standard Model particles.
It can produce these dark sector particles by shooting protons into a nuclear target. 
When protons collide with a nucleus, a new dark sector particle might be produced.

DarkQuest distinguishes itself from other experimental initiatives in that it can cover a unique parameter space 
of dark matter scenarios as a compact beam dump spectrometer detector.

<p align="left">
  <img src="/images/brem_production.png" width="300" alt="NM4 Location">
  <img src="/images/eta_production.png" width="300" alt="NM4 Location">
  <img src="/images/sipm_production.png" width="300" alt="NM4 Location">
</p>

## DarkQuest experimental setup

DarkQuest would operate on the neutrino-muon beamline of the Fermilab Accelerator Complex (NM4) and 
receive a high-intensity beam of 120 GeV protons from the Main Injector. 

The next figure shows the location of the experiment in the Fermilab beam-line.

<p align="left">
  <img src="/images/location2.png" width="300" alt="NM4 Location">
</p>

The DarkQuest detector
The detector setup would be a version of the SeaQuest/SpinQuest spectrometer, but with an added Electromagnetic Calorimeter (Ecal).
The spectrometer is made of magnets, hodoscopes (scintillator planes) and drift chambers.

Here is the schematic of the DarkQuest experiment with the Ecal in red.

<p align="left">
  <img src="/images/detector.png" width="500" alt="Detector Setup">
</p>

Here:
* `DP` stands for `Dark Photon Hodoscope`. There are two 

Find more on this [blog post by Duc](https://medium.com/darkquest/the-darkquest-experiment-1b8e46de1e40).

## Bibliography

\[1\]. Dark Sectors at the Fermilab SeaQuest Experiment: [Arxiv.1804.00661](https://arxiv.org/pdf/1804.00661.pdf)

\[2\]. Dark Scalars and Heavy Neutral Leptons at DarkQuest: [Arxiv.2008.08108](https://arxiv.org/pdf/2008.08108.pdf)

\[3\]. DarkQuest Snowmass LOI: [Link](https://www.snowmass21.org/docs/files/summaries/RF/SNOWMASS21-RF6_RF0_Nhan_Tran-025.pdf)

\[4\]. Phenix calorimeter: [Link](https://www.sciencedirect.com/science/article/pii/S016890020201954X)


# Computing 

## Getting started with computing accounts

If you do not have a Fermilab Kerberos account follow these instructions:

1. Fill out the [Fermilab Access Form for Users](https://get-connected.fnal.gov/users/access/). 

There are detailed instructions on how to get a computing 
account [here](hhttps://uscms.org/uscms_at_work/physics/computing/getstarted/getaccount_fermilab.shtml#ComputingAccountDetails). 
*Note that these have been written for the CMS experiment, so you need to change the affiliation to SpinQuest/E1039.
If your institute is in CMS then you can also get a CMS account first and later a SpinQuest account - see instructions below.*
For point-of-contact please put your supervisor who is associated/user w. Fermilab.

2. After the request has been accepted, you are given a default password for your Kerberos and Services account.

Contact the Service Desk (630-840-2345) to get your default passwords. Follow these links 
to change the [Kerberos password](https://fermi.servicenowservices.com/kb_view.do?sysparm_article=KB0010628) 
and the [Services password](https://fermi.servicenowservices.com/kb_view.do?sysparm_article=KB0010542).

3. Setting up the Kerberos configuration and connecting to the cluster:

Find detailed instructions [here](https://uscms.org/uscms_at_work/physics/computing/getstarted/uaf.shtml#prerequisiteKerberosConfig) 
(note that again some of these instructions have been written for CMS accounts).
Once you have set up the kerberos configuration you can obtain a ticket by:
```
kinit username@FNAL.GOV
```    
4. Connecting to the spinQuest cluster
```
ssh -KXY username@spinquestgpvm01.fnal.gov
```    
or if jupyter notebook is needed to run plotting code interactively, one can connect to the cluster via
```
ssh -KXY -L localhost:9999:localhost:9999 username@spinquestgpvm01.fnal.gov
```
where `9999` can be replaced with other port number.


If you already have a Fermilab Kerberos account and want to obtain access to the SpinQuest experiment:

1. Go to the Fermilab service desk to [request computing accounts](https://fermi.servicenowservices.com/wp).
2. Click in `Request Service`. Search for, or find in the list, `Experiment/Project/Collaboration Computing Account`. 
3. Fill in name, Kerberos Principal (username), desired affiliation/experiment, your institution name. By default, keep “No” for Computing/IT Professional Access Only section.
4. Wait for approval! It is recommended that we contact Kun Liu [liuk.pku@gmail.com] in advance so that he knows that the request is coming and can approve faster.
