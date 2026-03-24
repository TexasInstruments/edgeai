# Edge AI Software and Development Tools for Microprocessor devices with Linux and TIDL support
<hr>

## Release Notes

- [2026 March 10] Edgeai-tidlrunner release and edgeai-tidl-tools refactor
- [2025 September 25] 11.1 release. SDKs, edgeai-tidl-tools and edgeai-tensorlab are updated.

Further details are in the [Release Notes](./docs/release_notes.md). 

Also see the SDKs release notes, [edgeai-tidl-tools release notes](https://github.com/TexasInstruments/edgeai-tidl-tools/releases) and [edgeai-tensorlab release notes](https://github.com/TexasInstruments/edgeai-tensorlab/blob/main/docs/release_notes.md)

<hr>

## Introduction

Embedded inference of Deep Learning models is quite challenging - due to high compute requirements. TI’s Edge AI comprehensive software product help to optimize and accelerate inference on TI’s embedded devices. It supports heterogeneous execution of DNNs across Arm® Cortex®-A based MPUs, TI’s latest generation C7™ NPU. 

TI's edge AI solution simplifies the whole product life cycle of DNN development and deployment by providing a rich set of tools and optimized libraries. 

See our [Getting Started guide](./getting_started.md) for AM6xA and TDA4x with Edge AI and TI Deep Learning

## Overview

The figure below provides a high level summary of the relevant tools:<br><img src="assets/workblocks_tools_software.svg" width="800">

<hr>

## Details of various tools

The table below provides detailed explanation of each of the tools:

| Category                                                | Tool/Link| Purpose     | IS NOT                |
|---------------------------------------------------------|----------|-------------|-----------------------|
| **Inference and compilation Tools** |[edgeai-tidl-tools](https://github.com/TexasInstruments/edgeai-tidl-tools)| Compile ONNX and TFLite models and run model inference in PC emulation and on target hardware with simple python scripts and C++ applications<br>- Benchmark latency with out of box example models (10+)<br>- Compile user / custom model for deployment<br>- Inference of compiled models on X86_PC or TI SOC using file base input and output<br>- Core [documentation](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/docs) for TI Deep Learning<br>- Automated optimizations for ONNX-format models<br>- Docker for easy development environment setup |- Does not support benchmarking accuracy of models using TIDL with standard datasets, for example - accuracy benchmarking using MS COCO dataset for object detection models. Please refer to edgeai-tidlrunner or edgeai-benchmark.<br>- Does not support Camera, Display and inference based end-to-end pipeline development. Please refer to the SDK    | 
| **Inference and compilation Tools** |[edgeai-tidlrunner](https://github.com/TexasInstruments/edgeai-tidlrunner)| Command-line tool for model compilation, inference, accuracy benchmark, model optimization, analysis, and visualized model inspection<br>- No scripting required; set all model settings via command-line arguments or config file |- Does not support Camera, Display and inference based end-to-end pipeline development. Please refer Edge AI SDK for such usage<br>- Supports TI SOC and x86 PC    | 
| **Model Selection Tool** |[Model Selection Tool](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection) | Understand validated models' performance statistics such as FPS, latency, DDR bandwidth and accuracy (for standard datasets like imagenet1k). Find the model that best meets your performance and accuracy goals on TI Processor from TI Model Zoo.| |
| **Integrated environment for training and compilation** |[Model Analyzer](https://dev.ti.com/edgeaisession/)| Browser based environment to allow model evaluation with TI EVM farm<br>- Allow model evaluation without and software/hardware setup at user end<br>- User can reserve EVM from TI EVM farm and perform model evaluation using jupyter notebook |- Does not support Camera, Display and inference based end-to-end pipeline development. Please refer Edge AI SDK for such usage<br>- Does not give full access to the target processor; limited to on-target model inference and benchmarking results   | 
|**Integrated environment for training and compilation** |[Edge AI Studio](https://www.ti.com/tool/EDGE-AI-STUDIO)| GUI based Integrated environment for data set capture, annotation, training, compilation with connectivity to TI development board<br>- Bring/Capture your own data, annotate, select a model, perform training and generate artifacts for deployment on SDK<br>- Live preview for quick feedback |- Does not support Bring Your Own Model workflow  |
|**Edge AI Software Development Kit**| [Devices & SDKs](readme_sdk.md) | SDK to develop end-to-end AI pipeline with camera, inference and display<br>- Different inference runtime: TFLite/LiteRT, ONNXRT, TVM, TIDL-RT<br>- Framework: openVX, gstreamer<br>- Device drivers: Camera, display, networking<br>- OS: Linux, RTOS<br>- Many other software modules: codecs, OpenCV, OpenGL, …   | Does not support model compilation: this is supported only on an x86 machine  |


<hr>

| Category                                                | Tool/Link       | Purpose           | IS NOT    |
|---------------------------------------------------------|-----------------|-------------------|-----------|
| **Model Zoo, Model training, compilation/benchmark & associated tools** | [edgeai-tensorlab](https://github.com/TexasInstruments/edgeai-tensorlab)   | Provide model training software, collection of pretrained models with documentation and compilation/benchmark scripts. <br>Includes edgeai-modelzoo, edgeai-benchmark, edgeai-modeloptimization, edgeai-modelmaker, edgeai-torchvision, and model-training repo forks like edgeai-mmdetection.      |  |


<hr>

## Workflows
Bring your own model (BYOM) workflow:<br><img src="assets/workflow_bring_your_own_model.svg" width="800">

Train your own model (TYOM) workflow:<br><img src="assets/workflow_train_your_own_model.svg" width="800">
* PyTorch is used within edgeai-modeloptimization. Other training frameworks may be used without our optimization and QAT tools, but models must export to ONNX or TFLITE format. 

Bring your own data (BYOD) workflow:<br><img src="assets/workflow_bring_your_own_data.svg" width="800">

<hr>

## Tech Reports

Technical documentation can be found in the documentation of each repository. Here we have a collection of technical reports & tutorials that give high level overview on various topics.

- [**Edge AI Tech Reports in edgeai-tensorlab**](https://github.com/TexasInstruments/edgeai-tensorlab/blob/main/docs/tech_reports/README.md)

<hr>

## Publications

- Read some of our [**Technical publications**](./readme_publications.md)

<hr>

## Issue Trackers
**Issue tracker for [Edge AI Studio](https://www.ti.com/tool/EDGE-AI-STUDIO)** is listed in its landing page.

**[Issue tracker for TIDL](https://e2e.ti.com/support/processors/f/791/tags/TIDL)**: Please include the tag **TIDL** (as you create a new issue, there is a space to enter tags, at the bottom of the page). 

**[Issue tracker for edge AI SDK](https://e2e.ti.com/support/processors/f/791/tags/EDGEAI)** Please include the tag **EDGEAI** (as you create a new issue, there is a space to enter tags, at the bottom of the page). 

**[Issue tracker for ModelZoo, Model Benchmark & Deep Neural Network Training Software](https://e2e.ti.com/support/processors/f/791/tags/MODELZOO):** Please include the tag **MODELZOO** (as you create a new issue, there is a space to enter tags, at the bottom of the page). 

<hr>

## License
Please see the [LICENSE](./LICENSE) file for more information about the license under which this landing repository is made available. The LICENSE file of each repository is inside that repository.
