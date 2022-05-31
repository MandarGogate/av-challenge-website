# Scene Generation

Scenes are generated based on two scenarios involving a target and a masker:

* Target speaker + Competing speaker
* Target speaker + Noise

## Building the scenes

Overview:

**Scenario 1: Target speech + Competing speaker**

Target speech and competing speakers are from the LRS3 TED talks. 
These are mixed using different SNR levels that range from -15 dB to +5 dB. 
To calculate the SNR levels we use the scripts provided by the Clarity Challenge that provide speech-weighted calculation of SNR levels. 

**Scenario 2: Target speech + noise**

Target speakers are are from the LRS3 TED talks and then mixed with a selection of [noises](https://challenge.cogmhear.org/#/challenge-data/data-spec) using different SNR levels that range from -10 dB to +10 dB. 


### Selecting a Target and a masker


### Creating the mix


### Data summary

trainset: 
605 speakers / 113hrs (there is at least 9mins of data per speaker)
devset: 
85 speakers / 9hrs (there is between 5 to 9mins of data per speaker)

