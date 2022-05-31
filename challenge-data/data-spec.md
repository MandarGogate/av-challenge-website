# Data

To obtain the data and baseline code, please see the download page.


# Video and audio data sources

The video and audio data sources are as follows:

## Video data:

Video data is obtained from the [LRS3 dataset](https://www.robots.ox.ac.uk/~vgg/data/lip_reading/lrs3.html). LRS3 is composed by spoken sentences from TED and TEDx videos. 

## Audio data:

Audio data can be split into two main categories: speech and noise. 

**Speech:** speech signals for both target speaker and competing speakers are obtained from LRS3 TED talks. 

**Noise:** the noise dataset is built based on three different datasets. These are:

- [1st Clarity Enhancement Challenge](https://github.com/claritychallenge/clarity/tree/main/recipes/cec1): The Clarity Challenge noise dataset comprises around 6 hours of domestic noises. 
- [DEMAND](https://zenodo.org/record/1227121#.YpZHLRPMLPY): The DEMAND noise dataset includes multi-channel recordings of 18 soundscapes that account for a little over 1 hour of data. Each soundscape is recorded using 16-channel array. We select only one of the channels to be used in our dataset. Moreover, we don't consider soundscapes assigned to the "domestic" category as there can be overlapping to the sounds of the Clarity Challenge. Additionally, 
- [Deep Noise Supression challenge (DNS) 2nd version](https://github.com/microsoft/DNS-Challenge): From the DNS dataset we consider only audios that are obtained from Freesound, which result in around 29 hours of data. 

All audios are downsampled to 16 KHz. 

## A. Training, development, evaluation data

The dataset is divided into training and development data. 
The evaluation dataset will be added later on. 





# Training



