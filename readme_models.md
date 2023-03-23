# EdgeAI DNN Model Development Tools

![EdgeAI Development Flow](./assets/edgeai-development-models.png)

Models Zoo, Model Selection, Training, Quantization & Benchmarking

<hr>

## Introduction
We showcase several **low complexity** Deep Learning models that make  Inference on Low Power Embedded Platforms practical. 

Model training repositories are provided to help to train embedded friendly models. 

We also have Python modules and examples for **Quantization Aware Training** to generate quantized models for 8-bit fixed point inference.

<hr>

## EdgeAI Studio
*URL*: [https://www.ti.com/tool/EDGE-AI-STUDIO](https://www.ti.com/tool/EDGE-AI-STUDIO)

Supports the following functionalities:

**Model Analyzer** is a free online service that lets you evaluate accelerated deep learning inference on TI devices from your browser in minutes. Also provided there, is TI's Model Selection Tool that enables picking the ideal model for TI's embedded devices.

Model Composer - **coming soon**: Train, optimize and compile AI models for TI embedded processors. Supports Bring your own data (BYOD) - retrain TI models from TI Model Zoo to fine-tune performance for your unique application requirements.

<hr>


## EdgeAI Model Development for Beginners
**[EdgeAI-ModelMaker](https://github.com/TexasInstruments/edgeai-modelmaker)** is an easy-to-use model development tool for Edge AI. This brings together dataset handling, model training and model compilation using a command line interface. (Currently, dataset labelling is not integrated, but datasets annotated using an external tool such as Label Studio can be imported). This is achieved by stitching together several of the below model development repositories together - making it easy to install them and use them with a unified interface. This does not support all the below repositories and models, but only a subset. This tool makes it easy to get started with Edge AI model development.

<hr>


## Model Zoo & Benchmark
Example Deep Neural Network Models for our embedded devices.

**[edgeai-benchmark](https://github.com/TexasInstruments/edgeai-benchmark)**: A python based framework which can used for model compilation, accuracy benchmark and performance benchmark. Accuracy benchmark can be performed on PC  without a development board / EVM. But for performance benchmark, a development board is needed. The pre-trained models in our Model Zoo are supported off-the-shelf in this benchmark code and pre-compiled model artifacts provided along with the Model Zoo can be used. This uses [edgeai-tidl-tools](https://github.com/TexasInstruments/edgeai-tidl-tools) for model compilation and inference.

**[edgeai-modelzoo](https://github.com/TexasInstruments/edgeai-modelzoo)**: Large collection of pre-trained example models for our platform. Also provides information on how to train models using popular model training repositories. Pre-compiled model artifacts (compiled using edgeai-benchmark) are also provided.

<hr>


## Model Training Tools
Training tools based on popular Deep Learning Frameworks, allowing data scientists to make DNNs more suitable for TI devices.

**[edgeai-torchvision](https://github.com/TexasInstruments/edgeai-torchvision)**: Enhancement of [pytorch/vision a.k.a. torchvision](https://github.com/pytorch/vision). Support is added for training [embedded friendly Lite versions](https://github.com/TexasInstruments/edgeai-torchvision/tree/master/references) of torchvision's Classification, Segmentation & Detection reference models. We also have **[our own embedded friendly Lite models](https://github.com/TexasInstruments/edgeai-torchvision/tree/master/references/pixel2pixel)** for Image Classification, Semantic Segmentation, Depth Estimation, Motion Segmentation and various other Pixel2Pixel tasks including Multi-Task Learning.

**[edgeai-mmdetection](https://github.com/TexasInstruments/edgeai-mmdetection)**: PyTorch based **Object Detection** training of embedded friendly Lite models. Uses the popular [mmdetection](https://github.com/open-mmlab/mmdetection) repository.

**[edgeai-yolov5](https://github.com/TexasInstruments/edgeai-yolov5)**: PyTorch based **Object Detection** training of YOLOv5 models. This is a fork of the popular [ultralytics/yolov5](https://github.com/ultralytics/yolov5) repository - we have tweaked it to make the resulting models embedded friendly.


<hr>


## Guidelines for Model training & Quantization
Quantization (especially 8-bit Quantization) is important to get best throughput for inference. Quantization can be done using either **Post Training Quantization (PTQ)** or **Quantization Aware Training (QAT)**.

- TIDL natively supports PTQ - it can take floating point models and can quantize them using advanced calibration methods. In the below page, we have provided guidelines on how to choose models and how train them for best accuracy with Quantization - these guidelines are important to reduce accuracy drop during quantization with **PTQ**. 

- In spite of following these guidelines, if there are models that have significant accuracy drop with PTQ, it is possible to improve the accuracy using **QAT**. 

- Guidelines and tools for Model training and Quantization are given in [edgeai-torchvision](https://github.com/TexasInstruments/edgeai-torchvision) and its documentation on **[Quantization](https://github.com/TexasInstruments/edgeai-torchvision/blob/master/docs/pixel2pixel/Quantization.md)**. We also have tools for **Quantization Aware Training (QAT)** in this repository.


<hr>


## Notes: 
Information about Deep Neural Network Model training software for our older family of devices is [here](./readme_models-j6.md).

<hr>

