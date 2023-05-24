# Data

To obtain the necessary data and baseline code, please register for the challenge. You will then get a link for the download page and the necessary credentials to download it.

Data preparation scripts are located in our [GitHub page](https://github.com/cogmhear/avse_challenge) (see readme on "Data preparation").

All audio files are single channel, downsampled to 16 kHz and a bit depth of 16.

## Target

The target data is composed of videos retrieved from the [LRS3 dataset](https://mm.kaist.ac.kr/datasets/lip_reading/). LRS3 is composed by spoken sentences from TED and TEDx videos. 

## Interferers

We have two types of interferers:

**Speech:** competing speakers are derived from the [LRS3 dataset](https://mm.kaist.ac.kr/datasets/lip_reading/). Competing speakers and target speakers are disjoint sets.

**Noise:** the noise dataset is built based on three different datasets:

- [Clarity Enhancement Challenge (CEC1)](https://github.com/claritychallenge/clarity/tree/main/recipes/cec1): The Clarity Challenge noise dataset comprises around 7 hours of domestic noises. 
- [DEMAND](https://zenodo.org/record/1227121#.YpZHLRPMLPY): The DEMAND noise dataset includes multi-channel recordings of 18 soundscapes that represent over 1 hour of data. Each soundscape is recorded using a 16-channel array.\*
- [Deep Noise Supression challenge (DNS) 2nd version](https://github.com/microsoft/DNS-Challenge): The DNS dataset released in the second version of the challenge is composed by sounds from AudioSet, DEMAND and Freesound. In our selection we only consider audios that are obtained from Freesound.\*\* 

\* From DEMAND, we only select one channel per soundscape. Moreover, we don't consider soundscapes assigned to the "domestic" category to avoid overlapping with the sounds of the Clarity Challenge. Additionally, we remove the soundscape labeled as OMEETING because this example resembles the competing speaker scenario. 

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

* Evaluation dataset:
  - 2,792 scenes (4hours 32mins). Divided into 1,396 scenes for leadeboard and 1,396 scenes for listening test (2hours 16 minutes each).

The data preparation script will generate, for each scene, the following files:
- S00001_silent.mp4 (video without audio)
- S00001_target.wav (target audio)
- S00001_interferer.wav (interferer audio)
- S00001_mixed.wav (mixed audio = target audio + interferer audio)
where S00001 is the scene ID.

Metadata on the scenes is provided as JSON files (scenes.train.json and scenes.dev.json). Metadata includes information such as scene ID, target, SNR, masker, masker type (speech/noise) and segment selection offset. 

Metadata on target speakers (target_speech_list.json) and interfereres (masker_noise_list.json, masker_speech_list.json) is also provided. These can be used to generate other scenes, i.e. a different selection of target, interferer and SNR.

## Evaluation dataset

The evaluation for the 2nd edition of the challenge set can be downloaded from [this](https://data.cstr.ed.ac.uk/cogmhear/protected/avsec2_evalset.tar) link.

To download it, use the credentials you received after registering for the challenge.

Hint: credentials are the same as the ones used to download the noise dataset and the metadata

## Face landmarks train/dev sets

For each set we provide the following landmarks:

1) Face embedding
2) Facemesh landmark
3) Lip embedding
4) Lips: cropped video (lip region)

- Dev landmarks can download at: 

https://data.cstr.ed.ac.uk/cogmhear/protected/dev_face_landmarks.tar (9.1 GB) 

- Train landmarks are split into the following links/files:

Train set face embeddings: https://data.cstr.ed.ac.uk/cogmhear/protected/train_face_embedding.tar (36 GB) 
Train set facemesh landmark: https://data.cstr.ed.ac.uk/cogmhear/protected/train_facemesh_landmark.tar (24 GB) 
Train set lip embedding: https://data.cstr.ed.ac.uk/cogmhear/protected/train_lip_embedding.tar (18 GB) 
Train set lips cropped video: https://data.cstr.ed.ac.uk/cogmhear/protected/train_video_lips.zip (4.2 GB) 

