# EdgeAI Software And Development Tools
Models Training, Quantization, Model Zoo, Benchmarking For Embedded AI Development.

<hr>

## Introduction
Embedded Inference of Deep Learning models is quite challenging - due to high compute requirements. This repository provides various **tools for AI**, including Deep Learning, traditional Machine Learning and Computer Vision. We show several **low complexity** Deep Learning models that make  Inference on Low Power Embedded Platforms practical. We also have examples for **Quantization Aware Training** for 8-bit fixed point inference.

This github repository does not contain any code, but has links that point to the actual repositories containing code. 

<hr>


## Model Zoo & Benchmark
- **Jacinto-AI-ModelZoo**: Large collection of pre-trained models that are verified to work on our platform. We also information on how to train some of the important models, and also the complexity and what accuracy to expect. These models are primarily intended as examples for development. This repository also contains Pre-Imported model artifacts that can be used for inference on our device. <br>
-- Documentation: [**link**](http://git.ti.com/cgit/jacinto-ai/jacinto-ai-modelzoo/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/jacinto-ai-modelzoo/) <br>

- **Jacinto-AI-Benchmark**: Accuracy benchmarking of Deep Learning models is a difficult task. We make it easy for our platform with a Python package that runs on PC as well as on our EVM. The pre-trained models in our Model Zoo are supported off-the-shelf in this benchmark code. Accuracy benchmark of custom models can also be done easily with just a few lines of code. <br>
-- Documentation: [**link**](http://git.ti.com/cgit/jacinto-ai/jacinto-ai-benchmark/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/jacinto-ai-benchmark/) <br>


## Model Training for Jacinto7 family of devices
Deep Learning Examples for Jacinto7 family of devices - e.g. [TDA4VM](http://www.ti.com/product/TDA4VM) <br>
- **Pytorch-Jacinto-AI-DevKit**: PyTorch based training of Image Classification, Semantic Segmentation, Depth Estimation, Motion Segmentation and various other Pixel2Pixel tasks, Multi-Task Learning and [Quantization Aware Training](https://git.ti.com/cgit/jacinto-ai/pytorch-jacinto-ai-devkit/about/docs/Quantization.md). <br>
-- Documentation: [**link**](https://git.ti.com/cgit/jacinto-ai/pytorch-jacinto-ai-devkit/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/pytorch-jacinto-ai-devkit/) <br>

- **PyTorch-MMDetection**: PyTorch based **Object Detection** training/quantization <br>
-- Documentation: [**link**](https://git.ti.com/cgit/jacinto-ai/pytorch-mmdetection/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/pytorch-mmdetection/) <br>

- **PyTorch-SSDS-Keypoints**: This repository contains implementation of our work "Deep Learning based Parking Spot Detection and Classification in Fish-Eye Images". <br>
-- Documentation: [**link**](https://git.ti.com/cgit/jacinto-ai/pytorch-ssds-keypoints/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/pytorch-ssds-keypoints/) <br>


<hr>


## Model Training for Jacinto6 family of devices
Deep Learning and Traditional ML examples for Jacinto 6 family of devices - e.g. (TDA2x, TDA3x). These older modules are not included as submodules in this repo, but can be obtained using the links below. <br>
- **Caffe-Jacinto**: Our Caffe fork for training sparse CNN models including Object Detection and Semantic Segmentation models. <br>
-- Documentation: [**link**](https://git.ti.com/cgit/jacinto-ai/caffe-jacinto/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/caffe-jacinto/) <br>

- **Caffe-Jacinto-Models**: Scripts and examples for training sparse CNN models for Image Classification, Object Detection and Semantic Segmentation. <br>
-- Documentation: [**link**](https://git.ti.com/cgit/jacinto-ai/caffe-jacinto-models/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/caffe-jacinto-models/) <br>

- **Acf-Jacinto** - training tool for HOG/ACF/AdaBoost Object Detector (traditional machine learning based) <br>
-- Documentation: [link](https://git.ti.com/cgit/jacinto-ai/acf-jacinto/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/acf-jacinto/) <br>

<hr>


## Model Quantization
Quantization (especially 8-bit Quantization) is important to get best throughput for inference. Quantization can be done using either **Post Training Quantization (PTQ)** or **Quantization Aware Training (QAT)**.

[TI Deep Learning Library (TIDL)](https://software-dl.ti.com/jacinto7/esd/processor-sdk-rtos-jacinto7/latest/exports/docs/psdk_rtos/docs/user_guide/sdk_components_j721e.html#ti-deep-learning-library-tidl) that is part of the [Processor SDK RTOS for Jacinto7](https://www.ti.com/tool/download/PROCESSOR-SDK-RTOS-J721E) natively supports PTQ - TIDL can take floating point models and can quantize them using advanced calibration methods. 

We have  guidelines on how to choose models and how train them to get best accuracy with Quantization. It is unlikely that there will be significant accuracy drop with **PTQ** if these guidelines are followed. In spite of this, if there are models that have significant accuracy drop with quantization, it is possible to improve the accuracy using **QAT**. Please read more details in the [pytorch-jacinto-ai-devkit](https://git.ti.com/cgit/jacinto-ai/pytorch-jacinto-ai-devkit/about) and its documentation on **[Quantization](https://git.ti.com/cgit/jacinto-ai/pytorch-jacinto-ai-devkit/about/docs/Quantization.md)**.

<hr>


## Notes: 
- If you click on one of the links above - it will navigate to a repository hosted in **https://git.ti.com/jacinto-ai**. From there, you can click on one of the tabs to get more information on that repository. 
- For example, the **about** tab shows documentation. The **summary** tab lists all the branches, commit information and links for git clone/pull that repository.
- Each of those repositories also have separate LICENSE files. 

<hr>

## Issue Trackers: 
- **Issue Tracker for TIDL:** [https://e2e.ti.com/support/processors/f/791/tags/TIDL](https://e2e.ti.com/support/processors/f/791/tags/TIDL). Please include the tag **TIDL** (as you create a new issue, there is a space to enter tags, at the bottom of the page). 
- **Issue Tracker for jacinto-ai-devkit:** You can file issues or ask questions at **e2e**: [https://e2e.ti.com/support/processors/f/791/tags/jacinto_2D00_ai_2D00_devkit](https://e2e.ti.com/support/processors/f/791/tags/jacinto_2D00_ai_2D00_devkit). While creating a new issue kindly include **jacinto-ai-devkit** in the tags (as you create a new issue, there is a space to enter tags, at the bottom of the page). 

<hr>

## What is New:
- [2021-July] Several of our repositories are being moved from git.ti.com to github.com

<hr>

## License
Please see the [LICENSE](./LICENSE) file for more information about the license under which this landing repository is made available. The LICENSE file of each repository mentioned here is inside that repository.