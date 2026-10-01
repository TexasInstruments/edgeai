# Edge AI tools for MPUs

Embedded inference of Neural Network models is challenging due to high compute requirements. TI's Edge AI software optimizes and accelerates inference on TI's embedded devices, supporting heterogeneous execution of Neural Network models across Arm® Cortex®-A based MPUs and TI's C7™ NPU.

The C7 NPU is a power-efficient AI accelerator built on TI's DSP heritage, combining a SIMD-DSP with a matrix multiplication accelerator for fast neural network execution. Integrated into the AM6xA and TDA4x family of processors, it offloads inference from the Arm Cortex-A cores and supports multiple concurrent AI workloads, such as simultaneously processing camera, radar and lidar data, making it well suited for vision-heavy applications like ADAS, robotics and industrial automation.

TI Deep Learning (TIDL) is TI's software for compiling, optimizing and deploying neural network models on TI's embedded microprocessors, without needing to hand-write code for the underlying AI accelerator.

## Overview

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Getting started](../assets/icons/new/getting-started-icon.svg ':size=96')](getting_started.md)

</td>
<td>

Start with the [getting started guide](getting_started.md) for AM6xA and TDA4x devices.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Workflows](../assets/icons/new/workflow-icon.svg ':size=96')](workflows.md)

</td>
<td>

Pick the matching workflow for developing and deploying your model: [bring your own data (BYOD), bring your own model (BYOM), or train your own model (TYOM)](workflows.md).

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Case Studies & Demos](../assets/icons/ti/robotic-arm-icon.svg ':size=96')](https://ti.com/edgeaiprojects)

</td>
<td>

[Case Studies & Demos](https://ti.com/edgeaiprojects) - Robotics, automotive and industrial demo applications.

</td>
</tr>
</table>


## Quickstart
Here is a brief guide to get started with the tools.

1. Read the [getting started guide](getting_started.md) and also browse through [edgeai-tidl-tools](https://github.com/TexasInstruments/edgeai-tidl-tools) - understand the basic documentation and features of TIDL
2. Select the basic example in edgeai-tidl-tools and compile a model for the C7™ NPU.
3. Try to run it EVM board with edgeai-tidl-tools basic example.
4. Pick another pretrained model from the [Model Hub](https://github.com/TexasInstruments/edgeai-modelhub) or [Model Zoo](https://github.com/TexasInstruments/edgeai-modelzoo) and try to repeat the above process.
5. Once the usage of these tools are understood, go to the full tool list below for further optimization, benchmarking or custom model training.

## Tools for every role

#### Tools for model development

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![edgeai-modelhub](../assets/icons/new/model-hub-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modelhub)

</td>
<td>

[edgeai-modelhub](https://github.com/TexasInstruments/edgeai-modelhub) - Latest pretrained models from various public sources (recommended).

Collection of state-of-the-art pretrained models and export scripts. Also includes the details needed to compile, benchmark and deploy them. It is available at 
[huggingface](https://huggingface.co/TexasInstruments) and at [github](https://github.com/TexasInstruments/edgeai-modelhub). This collection is frequently updated. The repositories from which these models are exported are listed and can be used to train custom models with your own data (BYOD) using the pretrained model as the checkpoint.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![edgeai-modelzoo](../assets/icons/new/model-zoo-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modelzoo)

</td>
<td>

[edgeai-modelzoo](https://github.com/TexasInstruments/edgeai-modelzoo) - New and legacy models, including TI trained models.

Collection of new and legacy pretrained, benchmarked models, including TI-trained embedded-friendly models. The repositories from which these models are exported are listed and can be used to train custom models with your own data (BYOD) using the pretrained model as the checkpoint.

</td>
<tr>
<td align="center" width="15%">

[![edgeai-modeloptimization](../assets/icons/new/quantization-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modeloptimization)

</td>
<td>

[PyTorch model optimization & quantization](https://github.com/TexasInstruments/edgeai-modeloptimization)- Model optimization - quantization, sparsity, distillation.

Tools and utilities for developing embedded-friendly Neural Network models.

</td>
</tr>
</tr>
<tr>
<td align="center" width="15%">

[![Model training and Model Maker](../assets/icons/new/model-training-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tensorlab)

</td>
<td>

[edgeai-tensorlab/edgeai-modelmaker](https://github.com/TexasInstruments/edgeai-tensorlab) - Integrated CLI for model training and compilation (deprecated tool)

Train and compile models with the edgeai-modelmaker in edgeai-tensorlab. End-to-end development flow, with a simple interface - for beginners. 

Note: This package is no longer actively supported, but may still be used as an example to train and export ONNX models (which can then be compiled for latest TIDL with edgeai-tidlrunner or edgeai-tidl-tools).

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Publications and technical reports](../assets/icons/new/publication-icon.svg ':size=96')](readme_publications.md)

</td>
<td>

[Publications and technical reports](readme_publications.md) - Papers, articles and technical deep-dives.

</td>
</tr>
</table>


#### Tools for embedded deployment

<table style="display:table; width:100%; table-layout:fixed;">

<tr>
<td align="center" width="15%">

[![Target Devices & SDKs](../assets/icons/ti/processor-chip-icon.svg ':size=96')](readme_sdk.md)

</td>
<td>

[Target devices & SDKs](readme_sdk.md) - AM6xA / TDA4x processors with C7™ NPU acceleration, and their Linux/RTOS SDKs.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![ONNX model surgery](../assets/icons/new/pruning-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools/tidl-onnx-model-optimizer)

</td>
<td>

[ONNX model surgery](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools/tidl-onnx-model-optimizer) - Convert ONNX operators that are unsupported by TIDL into supported equivalents.

Also see other [model-tools](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools) that are helpful to modify models for TIDL compilation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model compilation and deployment with tidl-tools](../assets/icons/new/model-compilation-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidl-tools)

</td>
<td>

[edgeai-tidl-tools](https://github.com/TexasInstruments/edgeai-tidl-tools) - Model compilation and deployment.

Compile and infer ONNX/TFLite models for the C7™ NPU with edgeai-tidl-tools.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![edgeai-tidlrunner](../assets/icons/new/terminal-cli-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidlrunner)

</td>
<td>

[edgeai-tidlrunner](https://github.com/TexasInstruments/edgeai-tidlrunner) - Advanced model compilation and benchmark.

Command-line tool for model compilation, inference, accuracy benchmarking, optimization and visualized model inspection - no scripting required. Supports model compilation and accuracy benchmark on x86 PC emulation and inference on EVM.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![edgeai-modelselection](../assets/icons/new/benchmark-icon.svg ':size=96')](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection)

</td>
<td>

[edgeai-modelselection](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection) - Model benchmarks are available at Model Selection Tool.

Compare FPS, latency, DDR bandwidth and accuracy of various popular models.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Edge AI Studio](../assets/icons/new/studio-gui-icon.svg ':size=96')](https://www.ti.com/tool/EDGE-AI-STUDIO)

</td>
<td>

[Edge AI Studio (GUI)](https://www.ti.com/tool/EDGE-AI-STUDIO) - No-code, end-to-end model development.

Data capture, model training and compilation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Cloud-Based Evaluation](../assets/icons/ti/it-infrastructure-icon.svg ':size=96')](https://dev.ti.com/edgeaisession/)

</td>
<td>

[Cloud-Based Evaluation (GUI)](https://dev.ti.com/edgeaisession/) - Evaluate on TI's EVM farm - no local hardware needed (deprecated tool).

Note: This tool is a bit outdated now, and is no longer recommended.

</td>
</tr>
</table>


## Help and support

Submit an issue to get help & support from the TI [Processors E2E forum](https://e2e.ti.com/support/processors-group/processors/f/processors-forum/).

Help, support and training details for Edge AI Studio are listed at its [landing page](https://www.ti.com/tool/EDGE-AI-STUDIO).


## Release notes

Release notes are [here](./release_notes.md).
