# Edge AI software and development tools for microprocessor devices with Linux and TIDL support

Embedded inference of Neural Network models is challenging due to high compute requirements. TI's Edge AI software optimizes and accelerates inference on TI's embedded devices, supporting heterogeneous execution of Neural Network models across Arm® Cortex®-A based MPUs and TI's latest generation C7™ NPU.

## Overview

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Workflows](../assets/icons/new/workflow-icon.svg ':size=96')](workflows.md)

</td>
<td>

Depending on where someone starts, there is an appropriate workflow for developing and deploying the model on device. This section explains the [BYOD / BYOM / TYOM workflows](workflows.md).

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Getting started](../assets/icons/new/getting-started-icon.svg ':size=96')](getting_started.md)

</td>
<td>

[Getting started guide](getting_started.md) for AM6xA and TDA4x devices

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Case Studies & Demos](../assets/icons/ti/robotic-arm-icon.svg ':size=96')](https://ti.com/edgeaiprojects)

</td>
<td>

[Case Studies & Demos](https://ti.com/edgeaiprojects)

Robotics, automotive and industrial demo applications.

</td>
</tr>
</table>


## Tools for every role

#### Tools for model development

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Latest models in Model Hub](../assets/icons/new/model-hub-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modelhub)

</td>
<td>

[Model Hub](https://github.com/TexasInstruments/edgeai-modelhub)

Collection of state-of-the-art pretrained models and export scripts. Also includes the details needed to compile, benchmark and deploy them. It is available at 
[huggingface](https://github.com/TexasInstruments/edgeai-modelhub) and at [github](https://github.com/TexasInstruments/edgeai-modelhub). This collection is frequently updated.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model Zoo](../assets/icons/new/model-zoo-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modelzoo)

</td>
<td>

[Model Zoo](https://github.com/TexasInstruments/edgeai-modelzoo)

Collection of new and legacy pretrained, benchmarked models, including TI-trained, embedded-friendly models.

</td>
<tr>
<td align="center" width="15%">

[![PyTorch model optimization & quantization](../assets/icons/new/quantization-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modeloptimization)

</td>
<td>

[PyTorch model optimization & quantization](https://github.com/TexasInstruments/edgeai-modeloptimization)

Tools and utilities for developing embedded-friendly Neural Network models in PyTorch.

</td>
</tr>
</tr>
<tr>
<td align="center" width="15%">

[![Model training and Model Maker](../assets/icons/new/model-training-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tensorlab)

</td>
<td>

[Model training and Model Maker](https://github.com/TexasInstruments/edgeai-tensorlab)

Train and compile models with the edgeai-modelmaker in edgeai-tensorlab. End-to-end development flow, with a simple interface - for beginners. 

Note: This package is a bit outdated now, but it still serves as an example for model training and compilation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Publications and technical reports](../assets/icons/new/publication-icon.svg ':size=96')](readme_publications.md)

</td>
<td>

[Publications and technical reports](readme_publications.md)

Papers, articles and technical deep-dives.

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

[Target devices & SDKs](readme_sdk.md)

AM6xA / TDA4x processors and their Linux SDKs.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![ONNX model surgery](../assets/icons/new/pruning-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools/tidl-onnx-model-optimizer)

</td>
<td>

[ONNX model surgery](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools/tidl-onnx-model-optimizer)

Convert ONNX operators that are unsupported by TIDL into supported equivalents.

Also see other [model-tools](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools) that are helpful for TIDL compilation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model compilation and deployment with tidl-tools](../assets/icons/new/model-compilation-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidl-tools)

</td>
<td>

[Model compilation and deployment with tidl-tools](https://github.com/TexasInstruments/edgeai-tidl-tools)

Compile ONNX/TFLite models with edgeai-tidl-tools or edgeai-tidlrunner.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Advanced model compilation and benchmark](../assets/icons/new/terminal-cli-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidlrunner)

</td>
<td>

[Advanced model compilation and benchmark](https://github.com/TexasInstruments/edgeai-tidlrunner)

Command-line tool for model compilation, inference, accuracy benchmarking, optimization and visualized model inspection - no scripting required.<br>Supports TI SoCs and x86 PC; does not support camera/display pipelines (use Edge AI SDK for that).

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model benchmarks at Model Selection Tool](../assets/icons/new/benchmark-icon.svg ':size=96')](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection)

</td>
<td>

[Model benchmarks at Model Selection Tool](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection)

Compare FPS, latency, DDR bandwidth and accuracy of various popular models.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Edge AI Studio](../assets/icons/new/studio-gui-icon.svg ':size=96')](https://www.ti.com/tool/EDGE-AI-STUDIO)

</td>
<td>

[Edge AI Studio (GUI)](https://www.ti.com/tool/EDGE-AI-STUDIO)

No-code data capture, training and compilation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Cloud-Based Evaluation](../assets/icons/ti/it-infrastructure-icon.svg ':size=96')](https://dev.ti.com/edgeaistudio/)

</td>
<td>

[Cloud-Based Evaluation (GUI)](https://dev.ti.com/edgeaistudio/)

Evaluate on TI's EVM farm - no local hardware needed.

</td>
</tr>
</table>


## Help and support

Submit an issue to get help & support from the TI [Processors E2E forum](https://e2e.ti.com/support/processors-group/processors/f/processors-forum/).

Help, support and training details for Edge AI Studio are listed at its [landing page](https://www.ti.com/tool/EDGE-AI-STUDIO).


## Release notes

Release notes are [here](./release_notes.md).
