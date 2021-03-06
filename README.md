# Next

This repository contains the code and models for the following paper:


**[Peeking into the Future: Predicting Future Person Activities and Locations in Videos](https://arxiv.org/abs/1902.03748)** \
[Junwei Liang](https://www.cs.cmu.edu/~junweil/),
[Lu Jiang](http://www.lujiang.info/),
[Juan Carlos Niebles](http://www.niebles.net/),
[Alexander Hauptmann](https://www.cs.cmu.edu/~alex/),
[Li Fei-Fei](http://vision.stanford.edu/feifeili/) \
[CVPR 2019](http://cvpr2019.thecvf.com/)

You can find more information at our [Project Page](https://next.cs.cmu.edu/).\
*Please note that this is not an officially supported Google product.*


If you find this code useful in your research then please cite

```
@inproceedings{liang2019peekingfuture,
  title={Peeking into the Future: Predicting Future Person Activities and Locations in Videos},
  author={Junwei Liang and Lu Jiang and Juan Carlos Niebles and Alexander G. Hauptmann and Li Fei-Fei},
  booktitle={CVPR},
  year={2019}
}
```


## Introduction
In applications like self-driving cars and smart robot assistant it is important
for a system to be able to predict a person's future locations and activities.
In this paper we present an end-to-end neural network model that
**deciphers human behaviors** to predict their future paths/trajectories and
their future activities jointly from videos.

Below we show an example of the task. The green and yellow line show two
possible future trajectories and two possible activities are shown in the
green and yellow boxes. Depending on the future activity,
the target person(top right) may take different paths,
e.g. the yellow path for “loading” and the green path for “object transfer”.

<div align="center">
  <img src="images/title_image.png" width="700px" />
  <br/>
  <p style="font-weight:bold;font-size:1.2em;">
  	<a href="http://www.youtube.com/watch?feature=player_embedded&v=NyrGxGoS01U" target="_blank">Demo Video </a>
  </p>
</div>

## Model
Given a sequence of video frames containing the person for prediction,
our model utilizes person behavior module and person interaction module
to encode rich visual semantics into a feature tensor.
We propose novel person interaction module that takes into account both
person-scene and person-object relations for joint activities
and locations prediction.
<div align="center">
  <img src="images/model_overview.png" width="700px" />
</div>

## Dependencies
+ Python 2.7; TensorFlow == 1.10.0

## Pretrained Models
You can download pretrained models by running the script
`bash scripts/download_single_models.sh`.
This will download the following models, and will require
about 5.8 GB of disk space:

- `next-models/actev_single_model/`: This folder
includes single model for the ActEv experiment.
- `next-models/ethucy_single_model/`: This folder includes five single
models for the ETH/UCY leave-one-scene-out experiment.

## Testing
Instructions for testing pretrained models can be [found here](TESTING.md).

## Training new models
Instructions for training new models can be [found here](TRAINING.md).
