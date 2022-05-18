
![EdgeAIDevelopment SDK](./assets/edgeai-development-sdk.png)

<hr>

## Software Development Kit

**[Processor SDK Linux for Edge AI](https://www.ti.com/tool/download/PROCESSOR-SDK-LINUX-SK-TDA4VM)** - This also called as the Edge AI SDK in short. (SK in PROCESSOR-SDK-LINUX-SK-TDA4VM stands for Starter Kit). The SDK provides software and tools to let you effectively balance deep learning performance with system power and cost on Texas Instrument’s processors for edge AI applications such as latest TDA4 class of SoCs. We offer a practical embedded inference solution for next-generation vehicles, smart cameras, edge AI boxes, and autonomous machines and robots. In addition to general compute core and deep learning cores accelerator, our processors for edge AI integrate imaging, vision, multimedia cores hardware accelerators and with security enablers and optional microcontrollers for applications that require SIL-3 and ASIL-D functional safety certifications. With a few simple steps you can run high performance computer vision and deep learning demos using a live camera and display. This SDK extensively uses and builds upon several open source components including GStreamer, open source Deep Learning Runtimes such as ONNX Runtime, TFLite Runtime and Neo-DLR Runtime. While this is the easiest SDK to use, we also offer other SDKs for specialized use cases here: [PROCESSOR-SDK-J721E](https://www.ti.com/tool/PROCESSOR-SDK-J721E)

**[Robotics SDK for Edge AI](https://software-dl.ti.com/jacinto7/esd/robotics-sdk/latest/docs/index.html)** - The Robotics SDK provides software development environment on the latest TDA4 class of SoCs, and also provides software building blocks and example demos that can be leveraged in robotics software development. The SDK runs in Docker container environments on Processor SDK Linux for Edge AI. We provide detailed steps for setting up Docker container environments for ROS on the Processor SDK Linux for Edge AI. 


## Tools & Repositories

**[edgeai-tidl-tools](https://github.com/TexasInstruments/edgeai-tidl-tools)**: This repository contains examples developed for Deep learning runtime (DLRT) offering provided by TI’s edge AI solutions. This repository also provides model compilation tools that can help to compile DNN models (see the releases of this repository) and also run inference on PC (simulation). The resulting compiled model artifacts can be used to deploy AI applications on PROCESSOR-SDK-LINUX-SK-TDA4VM to achieve most optimal performance.


## Other Tools & Repositories (For information only)

Most of these components are packaged as part of the SDK or other tools. If you need to manually clone or download any of these repositories or tools, SDK documentation will provide that information.

**[TI Deep Learning Library/Product (TIDL)](https://software-dl.ti.com/jacinto7/esd/processor-sdk-rtos-jacinto7/latest/exports/docs/psdk_rtos/docs/user_guide/sdk_components_j721e.html#ti-deep-learning-product-tidl)** - The package that contains TI Deep Learning inference engine, deep learning network compiler (DLNAPS) and deep learning network import tool for C7x/MMA. *Note: This link is provided here only to easily access TIDL documentation.*

**[edgeai-gst-plugins](https://github.com/TexasInstruments/edgeai-gst-plugins)**: Repository to host GStreamer plugins for TI's EdgeAI class of devices

**[edgeai-tiovx-modules](https://github.com/TexasInstruments/edgeai-tiovx-modules)**: Repository to host TI's OpenVx modules used in EdgeAI SDK. These modules serve as the bridge between EdgeAI's custom GStreamer elements and underlying hardware accelerators and DSPs on Jacinto and Sitara class of processors.

**[tensorflow](https://github.com/TexasInstruments/tensorflow)**: TensorFlow is an end-to-end open source platform for machine learning. It has a comprehensive, flexible ecosystem of tools, libraries, and community resources that lets researchers push the state-of-the-art in ML and developers easily build and deploy ML-powered applications. Please see the branch **tidl-j7** for changes specific to our device.

**[onnxruntime](https://github.com/TexasInstruments/onnxruntime)**: ONNX Runtime is a cross-platform inference and training machine-learning accelerator. Please see the branch **tidl-j7** for changes specific to our device.

**[neo-ai-dlr](https://github.com/TexasInstruments/neo-ai-dlr)**: DLR is a compact, common runtime for deep learning models and decision tree models compiled by AWS SageMaker Neo, TVM, or Treelite. Please see the branch **tidl-j7** for changes specific to our device.

**[tvm](https://github.com/TexasInstruments/tvm)**: Apache TVM (incubating) is a compiler stack for deep learning systems. It is designed to close the gap between the productivity-focused deep learning frameworks, and the performance- and efficiency-focused hardware backends. TVM works with deep learning frameworks to provide end to end compilation to different backends.  Please see the branch **tidl-j7** for changes specific to our device.
