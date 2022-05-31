# Scene Generation

Scenes are generated based on two scenarios involving a target and an interferer:

* Target speaker + Competing speaker
* Target speaker + Noise

Information about the speech and noise data can be found [here](https://challenge.cogmhear.org/#/challenge-data/data-spec).

## Building the scenes

Each scene in the training and development datasets is composed by a different target and a unique noise segment.

**Target and a Interferer selection**

Targets are randomly selected. Selection of interferers is balanced so that there is the same amount of competing speaker scenes as there are noise scenes. Moreover, noises are also selected so that all categories are equally presents. 
The noise categories are:

* From Clarity Challenge:
* From DEMAND:
* From DNS: 

**SNR ranges and computation**

To calculate the SNR levels between speech and masker we apply the method of Clarity Challenge that implements a speech-weighted function in the computation of the SNR. 

**Target speech + Competing speaker**

The mixes are built using different SNR levels that range from -15 dB to +5 dB. 

**Target speech + noise** 

The mixes are built using different SNR levels that range from -10 dB to +10 dB.

### Mix

Once the target, masker and SNR are selected, random segments of the noise files are chosen to build the mix. 


