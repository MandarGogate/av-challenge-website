# Scene Generation

Scenes are generated based on two scenarios:

* Target speaker + Competing speaker
* Target speaker + noise

## Scenario 1: Target speech + Competing speaker

Target speech and competing speakers are obtained from TED talks. 
These are mixed using different SNR levels that range from -15 dB to +5 dB. 
To calculate the SNR levels we use the scripts provided by the Clarity Challenge that provide speech-weighted calculation of SNR levels. 


## Scenario 2: Target speech + noise

Target speakers are obtained from TED talks and then mixed with a selection of [noises] (https://github.com/MandarGogate/av-challenge-website/challenge-data/data-spec.md) using different SNR levels that range from -10 dB to +10 dB. 



