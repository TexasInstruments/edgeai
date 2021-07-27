# EdgeAI Software And Development Tools
Models Training, Quantization, Model Zoo, Benchmarking For Embedded AI Development.

<hr>

## Introduction
Embedded Inference of Deep Learning models is quite challenging - due to high compute requirements. This repository provides various **tools for AI**, including Deep Learning, traditional Machine Learning and Computer Vision. We show several **low complexity** Deep Learning models that make  Inference on Low Power Embedded Platforms practical. We also have examples for **Quantization Aware Training** for 8-bit fixed point inference.

This github repository does not contain any code, but has links that point to the actual repositories containing code. 

<hr>


## Model Zoo & Benchmark
Example Deep Neural Network Models for our embedded devices - e.g. [TDA4VM](http://www.ti.com/product/TDA4VM) <br>

![TDA4VM](./assets/TDA4VM.jpg) 

- **Jacinto-AI-ModelZoo**: Large collection of pre-trained models that are verified to work on our platform. We also information on how to train some of the important models, and also the complexity and what accuracy to expect. These models are primarily intended as examples for development. This repository also contains Pre-Imported model artifacts that can be used for inference on our device. <br>
-- Documentation: [**link**](http://git.ti.com/cgit/jacinto-ai/jacinto-ai-modelzoo/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/jacinto-ai-modelzoo/) <br>

- **Jacinto-AI-Benchmark**: Accuracy benchmarking of Deep Learning models is a difficult task. We make it easy for our platform with a Python package that runs on PC as well as on our EVM. The pre-trained models in our Model Zoo are supported off-the-shelf in this benchmark code. Accuracy benchmark of custom models can also be done easily with just a few lines of code. <br>
-- Documentation: [**link**](http://git.ti.com/cgit/jacinto-ai/jacinto-ai-benchmark/about/) <br>
-- git clone/pull URLs: [link](https://git.ti.com/cgit/jacinto-ai/jacinto-ai-benchmark/) <br>


## Model Training Tools And Repositories
Deep Neural Network Model Training for our embedded devices.

![Model Training](./assets/dnn-picture-small.png) 

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


## Model Quantization
Quantization (especially 8-bit Quantization) is important to get best throughput for inference. Quantization can be done using either **Post Training Quantization (PTQ)** or **Quantization Aware Training (QAT)**.

[TI Deep Learning Library (TIDL)](https://software-dl.ti.com/jacinto7/esd/processor-sdk-rtos-jacinto7/latest/exports/docs/psdk_rtos/docs/user_guide/sdk_components_j721e.html#ti-deep-learning-library-tidl) that is part of the [Processor SDK RTOS for Jacinto7](https://www.ti.com/tool/download/PROCESSOR-SDK-RTOS-J721E) natively supports PTQ - TIDL can take floating point models and can quantize them using advanced calibration methods. 

We have  guidelines on how to choose models and how train them to get best accuracy with Quantization. It is unlikely that there will be significant accuracy drop with **PTQ** if these guidelines are followed. In spite of this, if there are models that have significant accuracy drop with quantization, it is possible to improve the accuracy using **QAT**. Please read more details in the [pytorch-jacinto-ai-devkit](https://git.ti.com/cgit/jacinto-ai/pytorch-jacinto-ai-devkit/about) and its documentation on **[Quantization](https://git.ti.com/cgit/jacinto-ai/pytorch-jacinto-ai-devkit/about/docs/Quantization.md)**.

<hr>

## What is New:
- [2021-July] Several of our repositories are being moved from git.ti.com to github.com

<hr>

## Notes: 
- Information about Deep Neural Network Model training software for our older family of devices is [here](./readme_modelzoo-j6.md).

<hr>

