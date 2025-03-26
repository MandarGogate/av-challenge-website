# Scene Generation

Each scene is composed by audio and video of a target speaker mixed with one up to three interferes. 
Interferers can be either:
- A competing speaker
- A non-speech noise source (i.e., domestic noises, human non-speech noises, etc.)
- A music noise source

Scenes with multiple interferers can have up to one music interferer but multiple competing speakers or non-speech noise interferers. 

Information about the speech and noise data can be found [here](https://challenge.cogmhear.org/#/challenge-data/data-spec).

## Building the scenes

Training and development datasets are disjoint regarding speakers and noise files (but share same noise categories). 
Each scene is composed by a unique target.

**Target and Interferer selection**

Targets are randomly selected. Selection of interferers is balanced so that there are similar amounts of scenes containin one, two or theree interferers. Moreover, it is also balanced in terms of the number of interferer combinations (i.e.,competing speaker, non-speech noises, music) when multiple noise sources are present in a scene. 

**SNR ranges and computation**

To calculate the SNR levels between speech and interferer we apply the method of Clarity Challenge that implements a speech frequency-weighted function in the computation of the SNR. 

The mixes are built using different SNR levels that range from **-10 dB to +10 dB**.


## Main differences to AVSEC{1,2,3} datasets

- AVSEC-4 scripts generate binaural data. A monophonic mix is provided to participants working on single-channel audio-visual speech enhancement systems.
- Multiple interferers: A scene can have up to three interferers. 
- Reverberation. More information about the rooms (i.e., geometry, location of listener and sound sources) made available by the Clarity Challenge can be found [here.](https://claritychallenge.org/clarity_CEC1_doc/docs/cec1_scenario)
- No separation between noise/speech interferers SNR ranges. All SNR levels range from **-10 dB to +10 dB**.


[//]: # (## Basic stats of train/dev sets)

[//]: # ()
[//]: # (Duration of target files:)

[//]: # (- Target files have different durations. They range from 0.6 seconds to  )