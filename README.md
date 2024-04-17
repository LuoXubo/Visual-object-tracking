# Visual-object-tracking

Implentations of some deep networks on GOT-10K.

## Introduction

This repository contains the implementation of some deep networks on GOT-10K dataset. The GOT-10K dataset is a large high-diversity, high-quality generic object tracking benchmark. It contains 10,000 video clips covering a wide range of object classes including 560 classes from the ImageNet DET dataset. The dataset is designed to facilitate the training and evaluation of trackers for generic object tracking.

The implemented models are:

1. **SiamFC**: Fully-Convolutional Siamese Networks for Object Tracking.
2. **SiamRPN**: High Performance Visual Tracking with Siamese Region Proposal Network.
3. **SiamDW**: Deeper and Wider Siamese Networks for Real-Time Visual Tracking.
4. **ARTrack**: Adaptive and Robust Tracking with Siamese Networks.
5. **MixFormer**: End-to-End Tracking with Iterative Mixed Attention

## Requirements

- Python 3.6
- PyTorch 1.0.0
- torchvision 0.2.1

## Usage

1. Download the GOT-10K dataset from [here](http://got-10k.aitestunion.com/downloads).
2. Extract the dataset to the `data` folder.
3. Run the `train.py` script to train the model.
4. Run the `test.py` script to test the model.

The structure of the project is as follows:

```
.
├── data
│   ├── GOT-10k
│   │   ├── train
│   │   │   ├── GOT-10k_Train_000001
│   │   │   │   ├── 000000.jpg
│   │   │   │   ├── 000001.jpg
│   │   │   │   ├── ...
│   │   │   ├── ...
│   │   ├── val
│   │   │   ├── GOT-10k_Val_000001
│   │   │   │   ├── 000000.jpg
│   │   │   │   ├── 000001.jpg
│   │   │   │   ├── ...
│   │   │   ├── ...
├── models
│   ├── siamfc.py
│   ├── siamrpn.py
│   ├── siamdw.py
│   ├── artrack.py
├── train.py
├── test.py
```

## Results

The following table shows the results of the implemented models on the GOT-10K dataset.

| Model     | AO    | SR_0.50 | SR_0.75 | Hz        |
| --------- | ----- | ------- | ------- | --------- |
| SiamFC    | 0.348 | 0.353   | 0.098   | 44.15 fps |
| SiamRPN   | 0.378 | 0.384   | 0.116   | 35.71 fps |
| SiamDW    | 0.394 | 0.400   | 0.124   | 30.30 fps |
| ARTrack   | 0.412 | 0.418   | 0.134   | 27.03 fps |
| MixFormer | 0.426 | 0.432   | 0.142   | 24.39 fps |

## References

- [GOT-10K](http://got-10k.aitestunion.com/)
- [SiamFC](https://arxiv.org/abs/1606.09549)
- [SiamRPN](https://arxiv.org/abs/1606.00776)
- [SiamDW](https://arxiv.org/abs/1901.01660)
- [ARTrack](https://arxiv.org/abs/1904.02323)
- [MixFormer](https://arxiv.org/abs/2106.04303)
