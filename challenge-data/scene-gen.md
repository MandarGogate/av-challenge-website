# Scene Generation

Scenes are generated based on two scenarios involving a target and an interferer. 
Interferers can be either a competing speaker or a noise:

* Scenario 1: Target speaker + Competing speaker
* Scenario 2: Target speaker + Noise

Information about the speech and noise data can be found [here](https://challenge.cogmhear.org/#/challenge-data/data-spec).

## Building the scenes

Training and development datasets are disjoint regarding speakers and noises. 
Each scene is composed by a unique target and a unique noise.

**Target and Interferer selection**

Targets are randomly selected. Selection of interferers is balanced so that there is the same amount of competing speaker scenes as there are noise scenes. Moreover, noises are also selected so that all categories are similarly present. 

**SNR ranges and computation**

To calculate the SNR levels between speech and interferer we apply the method of Clarity Challenge that implements a speech frequency-weighted function in the computation of the SNR. 

**Target speech + Competing speaker**

The mixes are built using different SNR levels that range from -15 dB to +5 dB. 

**Target speech + noise** 

The mixes are built using different SNR levels that range from -10 dB to +10 dB.



