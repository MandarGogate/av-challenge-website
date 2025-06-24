# Data
To obtain the necessary data and baseline code, please register for the challenge. You will then get a link for the download page and the necessary credentials to download it.

Data preparation scripts are located in our [GitHub page](https://github.com/cogmhear/avse_challenge) (see readme on "Data preparation").

AVSEC-4 scripts will create **binaural signals**. Alternatively, we provide a **monophonic** mix for participants that want to implement monophonic audio-visual speech enhancement systems.

AVSEC-4 target and interferer files are single channel, downsampled to 16 kHz and a bit depth of 16.
Impulse responses are 6th order (49 channels) ambisonics signals downsampled to 16 kHz.

## Target

The target data is composed of videos from the [LRS3 dataset](https://mm.kaist.ac.kr/datasets/lip_reading/). 
LRS3 is composed by spoken sentences from TED and TEDx videos.

## Interferers

We have three types of interferers:

**Speech:** competing speakers are derived from the [LRS3 dataset](https://mm.kaist.ac.kr/datasets/lip_reading/). 
Competing speakers and target speakers are disjoint sets.

**Non-speech noise:** the non-speech noise dataset is built from two different datasets:

- [Clarity Enhancement Challenge (CEC1)](https://github.com/claritychallenge/clarity/tree/main/recipes/cec1): The Clarity Challenge noise dataset comprises around 7 hours of domestic noises. 
- [Deep Noise Supression challenge (DNS) 2nd version](https://github.com/microsoft/DNS-Challenge): The DNS dataset released in the second version of the challenge is composed by sounds from AudioSet, DEMAND and Freesound. In our selection we only consider audios that are obtained from Freesound.\*\* 

Note: in AVSEC-4 we don't consider sounds from [DEMAND](https://zenodo.org/record/1227121#.YpZHLRPMLPY) or [ESC-50 Dataset for Environmental Sound Classification](https://github.com/karolpiczak/ESC-50)

**Music:** the noise dataset is built based on three different datasets:
- [MedleydB Audio](https://medleydb.weebly.com/): MedleyDB audio is a multi-track music dataset containing 122 royalty-free songs. 
The dataset includes stereo mixes, individual stems (per instrument or group of instruments) and annotations for each song. We selected one channel of each stereo mix. The dataset is licensed under CC BY-NC-SA 4.0. 

  
\*\* From DNS, we remove sounds that belong to the *Fan* category to avoid overlapping with Clarity Challenge sounds. As a result in our noise dataset there are 25 hours of data derived from DNS noises. 

## Datasets: training and development

* Training dataset: 
  - 34,524 scenes (113hours 17mins)
  - 605 target speakers
  - interferers were selected from a pool of 405 competing speakers and 7,346 noise files (15 noise categories)

* Development dataset: 
  - ~~3,365 scenes (9hrs 30mins)~~ 3,306 scenes (8hrs 38mins)
  - 85 target speakers
  - interferers were selected from a pool of 30 competing speakers and 1,825 noise files (same 15 noise categories) 

[//]: # (* Evaluation dataset:)

[//]: # (  - 1,389 scenes &#40;2hrs 23mins&#41;)

[//]: # (  - 2,792 scenes &#40;4hours 32mins&#41;. Divided into 1,396 scenes for leadeboard and 1,396 scenes for listening test &#40;2hours 16 minutes each&#41;.)


The data preparation script will generate, for each scene, the following files as binaural or monoaural signals:

S00001 is the scene ID

**Video signal**

- S00001_silent.mp4 (video without audio)

**Binaural signals**

- S00001_target.wav (target signal)
- S00001_target_anechoic.wav (target anechoic signal to compute objective metrics (MBSTOI))
- S00001_interferer.wav (interferer signal)
- S00001_mix.wav (mixed audio = target signal + interferer signal)

**Monoaural signals**
- S00001_target_mono.wav (monoaural target signal)
- S00001_target_mono_anechoic.wav (monoaural target anechoic signal to compute objective metrics (STOI))
- S00001_interferer_mono.wav (monoaural interferer signal)
- S00001_mono_mix.wav (mixed audio = target signal + interferer signal)

*The **config file** provides parameters to choose which signals to render (i.e, monoaural, binaural, all signals).*

**Scenes metadata**

Metadata of the scenes is provided as JSON files (scenes.train.json and scenes.dev.json). Metadata includes information such as scene ID, room ID, target, number of interferers and type of interferers (music, noise, speech), SNR, HRTF and segment selection offset. 

**Target and interferers metadata**

Metadata of target speakers (target_speech_list.json) and interferers (masker_speech_list.json, masker_nonspeech_list.json, masker_music_list.json) is also provided. These can be used to generate other scenes, i.e. a different selection of target, interferer and SNR.

## Evaluation dataset AVSEC4

### In-domain: Listening test evaluation set

The in-domain evaluation set has 3180 scenes. A set of those are used in the leaderboard (i.e., 1500 scenes) and the remaining ones will be set aside for the listening test. 

[//]: # (Please submit all 3180 scenes when uploading to the leaderboard.  )

Each scene in the evaluation data has three files:
- S5xxxx_silent.mp4 (the silent video)
- S5xxxx_mono_mix.wav (monoaural mix)
- S5xxxx_mix.wav (binaural mix)

Teams working on single channel submissions should use *S5xxxx_mono_mix.wav* files while teams working on binaural submissions should use *S5xxxx_mix.wav* files.

A few remarks about in-domain the evaluation set:

- Target speakers are derived from Ted and TedX talks.
- Noises are a subset of those preset in the training set. 
- *Impulse Responses* used to create the evaluation set are not simulated as in the training set, but instead they were recorded in three different rooms (2 small/medium size meeting rooms and one large meeting room). 
Impulse responses for the target speaker were recorded at 1m and 1.5m of the target source, while those used for noise sources are place at different angles and distances between 1m and 2m.  
- SNRs range from -18 dB to 6.55 dB. SNRs were selected according to listening test results of previous editions of AVSEC and they reflect intelligibility scores that range from 28 to 85 percent. 
Please download the in-domain dataset [here](https://data.cstr.ed.ac.uk/cogmhear/protected/avsec4_evalset.tar). Use the credentials your received when joining the mailing list. 

### Out-of-domain evaluation set

**Important information: Please note that the listening test will be carried out with the in-domain evaluation dataset**

Additionally, we provide and out-of-domain evaluation set for the teams who would like to test their systems under more challenging conditions. 

This dataset is a first-of-its-kind audio-visual (AV) evaluation corpus designed to test the real-world performance of multimodal hearing technologies, such as audio-visual speech enhancement. It features free-flowing, spontaneous conversations between small groups in realistic and challenging sound environments.

Recording Setup:

Environment: Recordings took place in a specialized Auralisation Suite equipped with a 24-loudspeaker array (eight on the ceiling, eight at ear-level, and eight at ground-level) to create immersive and complex acoustic scenes.
Audio: A binaural microphone was placed on a designated listener (either hearing aid user or normal hearing participant) to capture the full acoustic mix (i.e., the speech from all participants plus the ambient noise).
Video: Two high-definition cameras were used to capture synchronized video streams, with one focused on each speaker's face.
Participants and Signals:

Speakers: Conversations were held in dyads (groups of two). Each dyad consisted of either two participants with normal hearing or one experienced hearing aid user and one normal hearing participant.
Provided Signals: The dataset provides the mixed audio from the reference microphone in both binaural and monophonic formats.
Content and Labels:

Content: The speech is entirely spontaneous and unscripted. Participants were given conversational prompts to encourage natural, free-flowing dialogue. This is a spontaneous speech corpus, not a read-speech corpus.
Noise Conditions and SNRs:

The noise was played through the loudspeaker array during the recording sessions, creating a highly realistic and dynamic signal-to-noise ratio (SNR) that varies naturally throughout the conversations. This differs from datasets where noise is synthetically added in post-processing.
Recordings were conducted in a variety of simulated scenes (e.g., a cafeteria, a train station, and a busy street) with signal-to-noise ratios (SNRs) ranging from +5 dB to -20 dB.

Please download the out-of-domain dataset [here](https://bit.ly/avsec4_outofdomain_dataset). Use the credentials you received through the mailing list when this dataset was released. 

[//]: # (- Contains 2,400 scenes. )

[//]: # (- Results from the leaderboard are computed from 1,000 scenes. Scenes that will be used in the listening test are different from those used in the leaderboard.)

[//]: # ()
[//]: # (The evaluation dataset can be found here: )

[//]: # ()
[//]: # (https://data.cstr.ed.ac.uk/cogmhear/protected/avsec3_evalset.tar)

[//]: # ()
[//]: # (Clean targets for avsec-3 eval set:)

[//]: # ()
[//]: # (https://data.cstr.ed.ac.uk/cogmhear/protected/avsec3_clean_targets.tar)

[//]: # ()
[//]: # (Hint: credentials are the same as the ones used to download the noise dataset and the metadata)

[//]: # (### SNRs in the evaluation set)

[//]: # ()
[//]: # (In AVSEC-1 and AVSEC-2 we selected SNRs in the evaluation set to reflect accuracy scores of 25%, 50% and 75% &#40;noise&#41; and 40%, 55%, and 70% &#40;competing speaker&#41;. We estimated psychometric curves according to word accuracy scores obtained from a listening test to find the corresponding SNRs. A broader description of the method, and the psychometric curves, can be found in section 2.4 of our challenge [paper]&#40;https://www.pure.ed.ac.uk/ws/portalfiles/portal/305863115/AVSE_Challenge_ALDANA_DOA30092022_AFV.pdf&#41;.)

[//]: # ()
[//]: # (In AVSEC-3 and AVSEC-4, we take an alternative approach to select SNRs in the evaluation set that we hope allow us to gain better understanding about system's performance.)

[//]: # (As a first step, we look at intelligibility scores from unmodified samples in the previous editions of the challenge and fit psychometric curves according to each interferer &#40;speech or noise&#41;. Then, we select three inteligibility accuracy intervals of [22.5, 47.5], [47.5, 72.5], and [72.5, 97.5] with means of 35, 60, and 85, respectively. These means are similar to the values used in the previous editions of the challenge. The SNRs chosen for the evaluation set are uniformly sampled from each interval.  )

[//]: # ()
[//]: # (This process allows us to sample a wide range of SNR values while ensuring that mean accuracies for each interval are consistent with values used in the previous challenges.)


[//]: # (AVSEC-LTR contains listening test responses of previous editions of the Challenge. )

[//]: # (Please refer to the README file to find more information about the license. )

## Face landmarks train/dev sets

For each set we provide the following landmarks:

1) Face embedding: embedding of the face region extracted using FaceNet model.
2) Facemesh landmark: 486 point 3D landmarks of face extracted using google mediapipe library.
3) Lip embedding: these are embeddings from the models trained to do the visual speech recognition or lip reading.
4) Lips: lip region extracted using facemesh landmark.

- Dev landmarks can be downloaded from the following link: 

https://data.cstr.ed.ac.uk/cogmhear/protected/dev_face_landmarks.tar (9.1 GB) 

- Train landmarks are split into the following links/files:

Train set face embeddings: https://data.cstr.ed.ac.uk/cogmhear/protected/train_face_embedding.tar (36 GB) 

Train set facemesh landmark: https://data.cstr.ed.ac.uk/cogmhear/protected/train_facemesh_landmark.tar (24 GB) 

Train set lip embedding: https://data.cstr.ed.ac.uk/cogmhear/protected/train_lip_embedding.tar (18 GB) 

Train set lips cropped video: https://data.cstr.ed.ac.uk/cogmhear/protected/train_video_lips.zip (4.2 GB) 

To download them, use the credentials you received after registering for the challenge.

- Additionally, we provide scripts for extracting face landmarks. These are available at:

https://github.com/cogmhear/avsec_preprocessing



