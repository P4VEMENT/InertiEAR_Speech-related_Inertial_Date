# InertiEAR: Automatic and Device-independent IMU-based Eavesdropping on Smartphones

IMU-based zero-permission eavesdropping on smartphones is widely believed that can be defended by limiting sampling rates (within 200 Hz). However, we experimentally observe that IMUs sampling below 200 Hz still record adequate speech-related information because of aliasing distortions. Accordingly, we propose a practical side-channel attack, **InertiEAR**, which leverages IMUs to eavesdrop on both top and bottom speakers in smartphones to break the defense of sampling rate restriction on the zero-permission eavesdropping. We exploit coherence between responses of the built-in accelerometer and gyroscope and their hardware diversity using a mathematical model. The coherence allows precise segmentation without manual assistance. We also mitigate the impact of hardware diversity and achieve better device-independent performance than existing approaches that have to massively increase training data from different smartphones for a scalable network model. This repository includes IMU (accelerometer and gyroscope) data used in **InertiEAR: Automatic and Device-independent IMU-based Eavesdropping on Smartphones** (https://ieeexplore.ieee.org/document/9796890).

## Data

+ We play speech audios from [AudioMNIST](https://github.com/soerenab/AudioMNIST) using on-board top/bottom speaker of target smartphones and collect IMU readings sampled at 200Hz by default in background.
+ This dataset consists of IMU data collected from 12 smartphones. Under each fodler named by smartphone model, there are subfolders for data collected in top speaker setup, bottom speaker setup and different volumes setup.
+ Accelerometer data (acc.csv) and gyroscope data (gyro.csv) are placed in folders named by related speech audio from [AudioMNIST](https://github.com/soerenab/AudioMNIST), while the folder names (format as groundtruth_personId_sampleId) implies the groundtruth (0-9), personId (1-60) and sampleId (0-49) of the audio.
+ This GitHub repository only consists part of our dataset, the full version can be downloaded [here](https://drive.google.com/drive/folders/1F3sqTJizDdIAYeP1EQqgGDxFG46y-7Wf?usp=sharing).

## Reference

If you use the provided IMU dataset for your project, please cite [our paper](https://ieeexplore.ieee.org/document/9796890):

```
@INPROCEEDINGS{9796890,
  author    = {Gao, Ming and Liu, Yajie and Chen, Yike and Li, Yimin and Ba, Zhongjie and Xu, Xian and Han, Jinsong},
  booktitle = {IEEE INFOCOM 2022 - IEEE Conference on Computer Communications},
  title     = {InertiEAR: Automatic and Device-independent IMU-based Eavesdropping on Smartphones},
  year      = {2022},
  pages     = {1129-1138},
  doi       = {10.1109/INFOCOM48880.2022.9796890}
}
```
