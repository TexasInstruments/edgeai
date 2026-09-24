# Edge AI Software and Development Tools for Microprocessor devices with Linux and TIDL support

Embedded inference of Deep Learning models is challenging due to high compute requirements. TI's Edge AI software optimizes and accelerates inference on TI's embedded devices, supporting heterogeneous execution of DNNs across Arm® Cortex®-A based MPUs and TI's latest generation C7™ NPU.

📖 [Full details of every tool](DETAILS.md) &nbsp;|&nbsp; 🚀 [Getting Started guide](./getting_started.md) for AM6xA and TDA4x devices

The figure below provides a high level summary of the relevant tools:<br>![Edge AI tools overview](assets/workblocks_tools_software.svg ':size=800')

<hr>

## Tools for every role

<table>
<tr>
<th width="50%">For ML Engineers</th>
<th width="50%">For Embedded Engineers</th>
</tr>
<tr>
<td>

![Model Zoo](../assets/icons/new/model-zoo-icon.svg ':size=44') **[Model Zoo](https://github.com/TexasInstruments/edgeai-modelzoo)**

Pretrained, benchmarked models ready to deploy.

</td>
<td>

![Target Devices & SDKs](../assets/icons/ti/processor-chip-icon.svg ':size=44') **[Target Devices & SDKs](readme_sdk.md)**

AM6xA / TDA4x processors and their Linux SDKs.

</td>
</tr>
<tr>
<td>

![Model Training](../assets/icons/new/model-training-icon.svg ':size=44') **[Model Training](https://github.com/TexasInstruments/edgeai-tensorlab)**

Train and optimize models with edgeai-tensorlab.

</td>
<td>

![SDK Software](../assets/icons/ti/sdk-code-icon.png ':size=44') **[SDK Software](DETAILS.md#sdk)**

End-to-end camera + inference + display pipeline.

</td>
</tr>
<tr>
<td>

![Model Compilation](../assets/icons/new/model-compilation-icon.svg ':size=44') **[Model Compilation (CLI)](https://github.com/TexasInstruments/edgeai-tidl-tools)**

Compile ONNX/TFLite models with edgeai-tidl-tools or edgeai-tidlrunner.

</td>
<td>

![Benchmarks](../assets/icons/new/benchmark-icon.svg ':size=44') **[Benchmarks](https://dev.ti.com/gallery/view/edgeai/edgeai-modelselection)**

Compare FPS, latency, DDR bandwidth and accuracy.

</td>
</tr>
<tr>
<td>

![Edge AI Studio](../assets/icons/new/studio-gui-icon.svg ':size=44') **[Edge AI Studio (GUI)](https://www.ti.com/tool/EDGE-AI-STUDIO)**

No-code data capture, training and compilation.

</td>
<td>

![Cloud-Based Evaluation](../assets/icons/ti/it-infrastructure-icon.svg ':size=44') **[Cloud-Based Evaluation](https://dev.ti.com/edgeaistudio/)**

Evaluate on TI's EVM farm - no local hardware needed.

</td>
</tr>
<tr>
<td>

![Quantization](../assets/icons/new/quantization-icon.svg ':size=44') **[Quantization (PTQ/QAT)](./getting_started.md#ti-edge-ai-model-development-flow)**

Recover accuracy lost to fixed-point inference.

</td>
<td>

![Workflows](../assets/icons/new/workflow-icon.svg ':size=44') **[BYOD / BYOM / TYOM Workflows](DETAILS.md#workflows)**

Bring your own data, bring your own model, or train from scratch.

</td>
</tr>
<tr>
<td>

![Tech Reports & Publications](../assets/icons/new/publication-icon.svg ':size=44') **[Tech Reports & Publications](readme_publications.md)**

Papers, articles and technical deep-dives.

</td>
<td>

![Case Studies & Demos](../assets/icons/ti/robotic-arm-icon.svg ':size=44') **[Case Studies & Demos](https://ti.com/edgeaiprojects)**

Robotics, automotive and industrial demo applications.

</td>
</tr>
</table>

<hr>

![Issue Trackers](../assets/icons/new/issue-tracker-icon.svg ':size=28') [Issue Trackers](DETAILS.md#issue-trackers) &nbsp;·&nbsp; ![Release Notes](../assets/icons/new/release-notes-icon.svg ':size=28') [Release Notes](DETAILS.md#release-notes) &nbsp;·&nbsp; ![License](../assets/icons/new/license-icon.svg ':size=28') [License](DETAILS.md#license)
