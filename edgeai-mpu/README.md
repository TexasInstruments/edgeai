# Edge AI software and development tools for microprocessor devices with Linux and TIDL support

Embedded inference of Neural Network models is challenging due to high compute requirements. TI's Edge AI software optimizes and accelerates inference on TI's embedded devices, supporting heterogeneous execution of Neural Network models across Arm® Cortex®-A based MPUs and TI's latest generation C7™ NPU.

## Details

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Workflows](../assets/icons/new/workflow-icon.svg ':size=96')](workflows.md)

</td>
<td>

Depending on where someone starts, there is an appropriate workflow for developing and deploying the model on device. This section explains the **[BYOD / BYOM / TYOM workflows](workflows.md)**

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Getting started](../assets/icons/new/getting-started-icon.svg ':size=96')](getting_started.md)

</td>
<td>

**[Getting started guide](getting_started.md)** for AM6xA and TDA4x devices

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Full Details](../assets/icons/new/steps-checklist-icon.svg ':size=96')](details.md)

</td>
<td>

**[Full details of every tool](details.md)**

</td>
</tr>
</table>


## Tools for every role

#### For ML engineers

<table style="display:table; width:100%; table-layout:fixed;">
<tr>
<td align="center" width="15%">

[![Latest models in Model Hub](../assets/icons/new/model-hub-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modelhub)

</td>
<td>

[Model Hub](https://github.com/TexasInstruments/edgeai-modelhub) has the latest models and is available at 
**[huggingface](https://github.com/TexasInstruments/edgeai-modelhub)** and at **[github](https://github.com/TexasInstruments/edgeai-modelhub)** - this is continuously being updated. See the state-of-the-art, pretrained models - benchmarked and ready to deploy.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model Zoo](../assets/icons/new/model-zoo-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modelzoo)

</td>
<td>

**[Model Zoo](https://github.com/TexasInstruments/edgeai-modelzoo)** - collection of old and new pretrained, benchmarked models, including TI trained embedded friendly models.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model Training](../assets/icons/new/model-training-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tensorlab)

</td>
<td>

**[Model Training](https://github.com/TexasInstruments/edgeai-tensorlab)**

Train and optimize models with edgeai-tensorlab.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![PyTorch model optimization & quantization](../assets/icons/new/quantization-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-modeloptimization)

</td>
<td>

**[PyTorch model optimization & quantization](https://github.com/TexasInstruments/edgeai-modeloptimization)**

Tools and utilities for developing embedded-friendly Neural Network models in PyTorch.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Tech Reports & Publications](../assets/icons/new/publication-icon.svg ':size=96')](readme_publications.md)

</td>
<td>

**[Tech reports & publications](readme_publications.md)**

Papers, articles and technical deep-dives.

</td>
</tr>
</table>

#### For embedded engineers

<table style="display:table; width:100%; table-layout:fixed;">

<tr>
<td align="center" width="15%">

[![Target Devices & SDKs](../assets/icons/ti/processor-chip-icon.svg ':size=96')](readme_sdk.md)

</td>
<td>

**[Target Devices & SDKs](readme_sdk.md)**

AM6xA / TDA4x processors and their Linux SDKs.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![ONNX Model Surgery](../assets/icons/new/pruning-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools/tidl-onnx-model-optimizer)

</td>
<td>

**[ONNX Model Surgery](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools/tidl-onnx-model-optimizer)**

Convert ONNX operators unsupported by TIDL into supported equivalents, plus other [model-tools](https://github.com/TexasInstruments/edgeai-tidl-tools/tree/master/model-tools) for TIDL compilation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Model Compilation](../assets/icons/new/model-compilation-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidl-tools)

</td>
<td>

**[Model Compilation (CLI)](https://github.com/TexasInstruments/edgeai-tidl-tools)**

Compile ONNX/TFLite models with edgeai-tidl-tools or edgeai-tidlrunner.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Advanced Compilation & Benchmark (CLI)](../assets/icons/new/terminal-cli-icon.svg ':size=96')](https://github.com/TexasInstruments/edgeai-tidlrunner)

</td>
<td>

**[Advanced Compilation & Benchmark (CLI)](https://github.com/TexasInstruments/edgeai-tidlrunner)**

Command-line tool for model compilation, inference, accuracy benchmarking, optimization and visualized model inspection - no scripting required.<br>Supports TI SoCs and x86 PC; does not support camera/display pipelines (use Edge AI SDK for that).

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Benchmarks](../assets/icons/new/benchmark-icon.svg ':size=96')](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection)

</td>
<td>

**[Benchmarks](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection)**

Compare FPS, latency, DDR bandwidth and accuracy.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Edge AI Studio](../assets/icons/new/studio-gui-icon.svg ':size=96')](https://www.ti.com/tool/EDGE-AI-STUDIO)

</td>
<td>

**[Edge AI Studio (GUI)](https://www.ti.com/tool/EDGE-AI-STUDIO)**

No-code data capture, training and compilation.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Cloud-Based Evaluation](../assets/icons/ti/it-infrastructure-icon.svg ':size=96')](https://dev.ti.com/edgeaistudio/)

</td>
<td>

**[Cloud-Based Evaluation](https://dev.ti.com/edgeaistudio/)**

Evaluate on TI's EVM farm - no local hardware needed.

</td>
</tr>
<tr>
<td align="center" width="15%">

[![Case Studies & Demos](../assets/icons/ti/robotic-arm-icon.svg ':size=96')](https://ti.com/edgeaiprojects)

</td>
<td>

**[Case Studies & Demos](https://ti.com/edgeaiprojects)**

Robotics, automotive and industrial demo applications.

</td>
</tr>
</table>


## Help & support

Submit an issue to get help & support from the TI [Processors E2E forum](https://e2e.ti.com/support/processors-group/processors/f/processors-forum/)

Help, support and training details for Edge AI Studio is listed at its [landing page](https://www.ti.com/tool/EDGE-AI-STUDIO).


## Release Notes

Release notes are [here](./release_notes.md)


