# Challenge Rules

## Teams

- Teams must have pre-registered and nominated a contact person.
- Teams can be from one or more institutions.

## Transparency

- Teams must submit a one page [system description](https://challenge.cogmhear.org/#/getting-started/systems-description) per entry. 
- Teams can also submit a paper to the AVSE challenge proceedings. Further information is available [here](submission.md). 
- Teams are encouraged – but not required – to provide us with access to the system/model and to make their code open source.
- Anonymous entries are not allowed.

## What information can I use?

### Track 1:

- Participants should only use the provided data, i.e. the noise audio files and the metadata files that define the list of target and competing speakers derived from the LRS3 dataset. It is not allowed to add own data for training purposes. 
- Teams are allowed to create more training data using our provided tools and dataset. 
- Participants are allowed to use audio-only or visual-only pretrained models, however, it is not allowed to use AV pretrained models. 

<!-- There is no limit on the amount of training data that can be generated using our tools and training data sets. Teams can also use their own data for training or expand the training data through simple automated modifications.  -->

### Track 2:

- Participants are allowed to use additional training data as long as it is publicly available or is made available to other participants in the Challenge.
- Teams are allowed to create more training data using our provided tools and dataset.
- Participants are allowed to use AV pretrained models as long as they are publicly available or are made available to other participants in the Challenge.

### Track 3 (low-latency track):

*Requirements:*
- The AVSE must take less than the stride time Ts (in ms) to process a frame of size T (in ms). For example, Ts = T/2 for 50% overlap between frames. 

- The total algorithmic latency allowed including the frame size T, stride time Ts and any look ahead must be less than or equal to 80ms. For example, if you use a frame length of 64ms with a stride of 16ms resulting in an algorithmic delay of 80ms, then you satisfy the latency requirements. 

[//]: # (If you use a frame size of 32ms with a stride of 16ms resulting in an algorithmic delay of 48ms, then your method does not satisfy the latency requirements as the total algorithmic latency exceeds 80ms. )
- If your frame size plus stride T1=T+Ts is less than 80ms, then you can use up to (80-T1) ms future information.

## Computational restrictions

- Teams may choose to use all, some or none of the parts of the baseline model.
- There is no limit on computational cost.
- Please not the specific requirements of the low-latency track if you are submitting to track 3. 

## Intellectual property

The following terms apply to participation in this machine learning challenge (“Challenge”). Entrants may create original solutions, prototypes, datasets, scripts, or other content, materials, discoveries or inventions (a “Submission”). The Challenge is organised by the Challenge Organiser.

Entrants retain ownership of all intellectual and industrial property rights (including moral rights) in and to Submissions.

As a condition of submission, Entrant grants the Challenge Organiser, its subsidiaries, agents and partner companies, a perpetual, irrevocable, worldwide, royalty-free, and non-exclusive licence to use, reproduce, adapt, modify, publish, distribute, publicly perform, create a derivative work from, and publicly display the Submission.

Entrants provide Submissions on an “AS IS” BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied, including, without limitation, any warranties or conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A PARTICULAR PURPOSE.


