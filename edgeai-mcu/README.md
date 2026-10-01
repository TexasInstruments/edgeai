# Edge AI tools for MCUs

Edge AI on TI's Application Specific Microcontrollers (MCUs) - Tiny ML brings AI models to resource-constrained devices like C2000™ (F28x/F29x), MSPM0, Connectivity and Radar MCUs, enabling real-time analysis of sensor data such as current, accelerometer and vibration signals.

## Quickstart

Here is a brief guide to get started with the tools.

1. Browse through the [Example applications](readme_examples.md) described in this repository and in [tinyml-modelzoo](https://github.com/TexasInstruments/tinyml-modelzoo#examples-reference) to understand the kind of applications that can be developed.
2. [Edge AI Studio (GUI)](https://www.ti.com/tool/EDGE-AI-STUDIO/) is the easiest starting point for a beginner. Try out an already existing example to get an idea about the development flow.
3. Use or capture your own data in Edge AI Studio and then try out the model training and compilation flow.
4. Browse through and try out the CLI tools provided in [tinyml-modelzoo](https://github.com/TexasInstruments/tinyml-modelzoo)
5. Once the usage of these tools is understood, go to the full tool list below for further optimization and benchmarking or custom model training.


## Tools for every role

### Tools for model development

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Example applications](../assets/icons/new/app-gallery-icon.svg ':size=96')](readme_examples.md)

</td>
<td>

[Example applications](readme_examples.md) - Browse 30+ ready-to-run example applications.

Examples include Time Series Classification, Regression, Forecasting, Anomaly Detection, Audio Classification, Image Classification, and Radar Point Cloud Classification, each with a dataset, tuned model, and device-specific config.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![tinyml-tensorlab](../assets/icons/new/model-training-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-tensorlab)

</td>
<td>

[tinyml-tensorlab html user guide](https://software-dl.ti.com/C2000/esd/mcu_ai/user_guide/index.html) and [tinyml-tensorlab](https://github.com/TexasInstruments/tinyml-tensorlab) - Integrated model training and compilation.

The Tiny ML Tensorlab is the starting point to explore TI's AI models for MCUs. It supports training models across Time Series Classification, Regression, Forecasting, Anomaly Detection, and Image Classification tasks across 24+ TI microcontrollers with 30+ example applications.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model Optimization Toolkit](../assets/icons/new/accelerator-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-tensorlab/tree/main/tinyml-modeloptimization)

</td>
<td>

[tinyml-modeloptimization](https://github.com/TexasInstruments/tinyml-tensorlab/tree/main/tinyml-modeloptimization) - Model quantization tools.

Tools to quantize models for TI devices with TinyEngine™ NPUs. Supports Quantization Aware Training (QAT) and Post Training Quantization (PTQ).

</td>
</tr>
</table>

### Tools for embedded deployment

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Target devices & SDKs](../assets/icons/new/mcu-icon.svg ':size=96')](readme_sdk.md)

</td>
<td>

[Target devices & SDKs](readme_sdk.md) - Software development kits of supported devices.

C2000™ (F28x/F29x), MSPM0, Connectivity and Radar MCUs, and their supported SDKs.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![tinyml-modelzoo](../assets/icons/new/model-zoo-icon.svg ':size=96')](https://github.com/TexasInstruments/tinyml-modelzoo)

</td>
<td>

[tinyml-modelzoo](https://github.com/TexasInstruments/tinyml-modelzoo) - MCU AI models, examples, and configurations with integrated model training, quantization, and compilation.

Texas Instruments' central repository for AI models, examples, and configurations for microcontroller (MCU) applications. Clone this repo, install it, and run any example config against your target device — training, quantization, and compilation all happen automatically underneath.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Edge AI Studio (GUI)](../assets/icons/new/studio-gui-icon.svg ':size=96')](https://www.ti.com/tool/EDGE-AI-STUDIO/)

</td>
<td>

[Edge AI Studio (GUI)](https://www.ti.com/tool/EDGE-AI-STUDIO/) - End-to-end GUI solution.

The Edge AI Studio graphical user interface provides a fully integrated solution for data management, model training and deployment on a live development platform. Select from a variety of optimized pre-trained models in the TI Model Zoo and optionally re-train them with custom data (BYOD) to improve accuracy and performance. Edge AI Studio is available as both a cloud and desktop application for microcontrollers, connectivity devices and radar sensors. 

</td>
</tr>
<tr>
<td align="center" width="15%">

[![NN Compiler for MCUs](../assets/icons/new/model-compilation-icon.svg ':size=96')](https://software-dl.ti.com/mctools/nnc/mcu/users_guide/)

</td>
<td>

[NN Compiler for MCUs](https://software-dl.ti.com/mctools/nnc/mcu/users_guide/) - Neural Network Compiler (NNC) for MCUs.

Texas Instruments’ Neural Network Compiler (NNC) for MCUs enables machine learning networks to be compiled for TI MCUs. The output from this compiler is an inference library (.h, .a). These files, in turn, are compiled by the MCU compiler along with other application code managed as a Code Composer Studio (CCS) project.

</td>
</tr>
</table>
