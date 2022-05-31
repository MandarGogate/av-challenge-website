# Scene Generation

Scenes are generated based on two scenarios involving a target and a masker:

* Target speaker + Competing speaker
* Target speaker + Noise

Information about the speech and noise data can be found [here](https://challenge.cogmhear.org/#/challenge-data/data-spec).

## Building the scenes

Next, we present an overview of the scene generation process:

### Target and a Masker selection

Targets are randomly selected. Half of the maskers are competing speakers and half of them are noises. 
Noises are selected so that all noise categories present in the training and development sets are balanced.

### SNR ranges and computation

To calculate the SNR levels between speech and masker we apply the method of Clarity Challenge that implements a speech-weighted function in the computation of the SNR. 

**Target speech + Competing speaker**

The mixes are built using different SNR levels that range from -15 dB to +5 dB. 

**Target speech + noise** 

The mixes are built using different SNR levels that range from -10 dB to +10 dB.

### Mix

Once the target, masker and SNR are selected, random segments of the noise files are chosen to build the mix. 


