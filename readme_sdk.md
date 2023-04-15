
<img src="./assets/sdk-code-cropped-icon.png" width=600>

<hr>

## Supported Devices & SDKs

### AM62A
* Product information: https://www.ti.com/product/AM62A7
* Development Board: https://www.ti.com/tool/SK-AM62A-LP
* SDK landing page: https://www.ti.com/tool/PROCESSOR-SDK-AM62A
* Edge AI Linux SDK: https://www.ti.com/tool/download/PROCESSOR-SDK-LINUX-AM62A
* Edge AI SDK documentation: https://software-dl.ti.com/jacinto7/esd/processor-sdk-linux-edgeai/AM62AX/latest/exports/docs/common/sdk_overview.html

### AM68A
* Product information: https://www.ti.com/product/AM68A
* Development Board: https://www.ti.com/tool/SK-AM68
* SDK landing page: https://www.ti.com/tool/PROCESSOR-SDK-AM68A
* Edge AI Linux SDK: https://www.ti.com/tool/download/PROCESSOR-SDK-LINUX-AM68A
* Edge AI SDK documentation: https://software-dl.ti.com/jacinto7/esd/processor-sdk-linux-edgeai/AM68A/latest/exports/docs/common/sdk_overview.html

### TDA4VM (AM68PA)
* Product information: https://www.ti.com/product/TDA4VM
* Development Board: https://www.ti.com/tool/SK-TDA4VM
* SDK landing page: https://www.ti.com/tool/PROCESSOR-SDK-J721E
* Edge AI Linux SDK: https://www.ti.com/tool/download/PROCESSOR-SDK-LINUX-SK-TDA4VM
* Edge AI SDK documentation: https://software-dl.ti.com/jacinto7/esd/processor-sdk-linux-edgeai/TDA4VM/latest/exports/docs/common/sdk_overview.html

### AM69A
* Product information: https://www.ti.com/product/AM69A
* Development Board: https://www.ti.com/tool/SK-AM69
* SDK landing page: https://www.ti.com/tool/PROCESSOR-SDK-AM69A
* Edge AI Linux SDK: To be released by April-End 2023
* Edge AI SDK documentation: To be released by April-End 2023

<hr>

## Developing edge AI applications with GStreamer 
<img src="https://software-dl.ti.com/jacinto7/esd/processor-sdk-linux-edgeai/TDA4VM/08_06_00/exports/docs/_images/open-src-components.png" width=600>

**[edgeai-gst-apps](https://github.com/TexasInstruments/edgeai-gst-apps)**: These are plug-and-play deep learning applications which support running open source runtime frameworks such as TFLite, ONNX and NeoAI-DLR with a live camera and display. They help connect realtime camera, video or RTSP sources to DL inference to live display, bitstream or RTSP sinks. (Note: **edgeai-gst-apps** is included in the SDK).

Apart from the applications that are part of edgeai-gst-apps, other example applications are also available at https://github.com/TexasInstruments. Look for forks of [edgeai-gst-apps](https://github.com/TexasInstruments/edgeai-gst-apps) that contains more examples.

<hr>

## Tools & Repositories

**[edgeai-tidl-tools](https://github.com/TexasInstruments/edgeai-tidl-tools)**: This repository contains examples developed for TI Deep Learning Library/Product (TIDL) and Deep learning runtime (DLRT) offering provided by TI’s edge AI solutions. This repository also provides model compilation tools that can help to compile DNN models (see the releases of this repository) and also run inference on PC (simulation). The resulting compiled model artifacts can be used to deploy AI applications on the SDK to achieve optimal performance. DLRT is packaged as part of the EdgeAI SDK.
