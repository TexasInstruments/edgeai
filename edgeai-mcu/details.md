# Edge AI / Tiny ML Software and Development Tools for Microcontrollers

## 1. Introduction

**Analytics for TI's Application Specific Microcontrollers (MCUs)**
* The integration of Artificial Intelligence (AI) on the edge, particularly on Microcontrollers (MCUs), has revolutionized the way we approach data processing and analysis. Edge AI MCU applications offer numerous advantages, including reduced latency, improved real-time decision-making, and enhanced security. One of the key drivers of this trend is TinyML, a subset of machine learning that enables AI models to run on resource-constrained devices like MCUs. By leveraging TinyML, developers can deploy AI models on MCUs, allowing for the analysis of time-series data from various sensors such as current sensors, accelerometers, and vibration sensors.

* **Texas Instruments (TI)** offers a range of devices that support Edge AI applications, including C2000™ (F28x and F29x) devices, as well as the MSPM0 and Connectivity MCUs. The company's product roadmap is focused on providing a comprehensive portfolio of devices that cater to the growing demand for Edge AI applications. Additionally, TI's solution offering includes Bring Your Own Device (BYOD) and Bring Your Own Model (BYOM) workflows, which enable developers to seamlessly integrate their own devices and models with TI's Edge AI ecosystem.

### 1.1 Devices Supported

* **F28P55**: Product information: https://www.ti.com/product/TMS320F28P550SJ
* **F28P65**: Product information: https://www.ti.com/product/TMS320F28P650DK
* **F2837**: Product information: https://www.ti.com/product/TMS320F28377D
* **F28004**: Product information: https://www.ti.com/product/TMS320F280049C
* **F28003**: Product information: https://www.ti.com/product/TMS320F280039C
* **M0G3507**: Product information: https://www.ti.com/product/MSPM0G3507

Coming Soon:
* Radar, Connectivity and AM2x devices


<hr>

## 	2. BYOD and BYOM Workflows: 

* TI's **BYOD** and **BYOM** workflows provide developers with the flexibility to use their own devices and models with TI's Edge AI solutions. These workflows enable developers to:
  * **Bring Your Own Data (BYOD)**: Use their own data or collect data with TI's Edge AI software tools and frameworks. This allows developers to leverage their existing investments and integrate TI's Edge AI solutions with TI's devices.
  * **Bring Your Own Model (BYOM)**: Use their own AI models with TI's Edge AI software tools and frameworks. This allows developers to leverage their existing model development investments and integrate their own models with TI's Edge AI solutions.
  

* The **BYOD** and **BYOM** workflows provide several benefits, including:
  * Reduced Development Time: Developers can quickly integrate their own data and models with TI's Edge AI solutions, reducing the time and effort required to develop and deploy Edge AI applications.
  * Increased Flexibility: Developers can use their own data and models, providing them with the flexibility to choose the best solutions for their specific use cases.
  * Improved Performance: Developers can optimize their own data collected and models for their specific use cases, resulting in improved performance and efficiency.

* TI's Edge AI software tools and frameworks provide a range of features and functionalities to support the BYOD and BYOM workflows, including:
  * Device Abstraction: TI's Edge AI software tools provide device abstraction layers that enable developers to use same application but deploy it on different TI devices.
  * Model Import: TI's Edge AI software tools provide model import features that enable developers to import their own AI models and integrate them with TI's Edge AI solutions.
  * Optimization: TI's Edge AI software tools provide optimization features that enable developers to optimize their own devices and models for their specific use cases.

<hr>

## 3. Applications/Use-cases Supported by TI:
TI supports a wide range of Edge AI applications, including:

### 3.1. Applications with reference Designs:
  * **Arc Fault Monitoring:** This use case involves detecting arc faults in electrical systems, which can help prevent fires and ensure safe operation. TI provides reference designs and software tools to support the development of arc fault monitoring systems. Find more about it here: https://www.ti.com/technologies/edge-ai/edge-ai-use-cases.html#real
  * **Motor Bearing Fault Monitoring:** This application involves monitoring the condition of motor bearings to predict potential failures and schedule maintenance. TI's Edge AI solutions enable developers to build systems that can detect anomalies in motor bearing behavior and provide early warnings of potential faults. Find more about it here: https://www.ti.com/technologies/edge-ai/edge-ai-use-cases.html#real
  * **Fan Blower Imbalance:** This use case involves detecting imbalances in fan blowers, which can help improve efficiency and reduce energy consumption. TI's Edge AI solutions provide the necessary tools and software to support the development of fan blower imbalance detection systems.

### 3.2. Application Examples on Public Datasets
  * In addition to these examples, TI also provides public datasets that can be used to develop and test Edge AI models for various applications.

<hr>

## 4. MCU AI Software Breadth:

TI offers a comprehensive range of software tools to support the development of Edge AI applications on MCUs, including:

| Category                                      | Tool/Link                                                                                                           | Purpose                                                                                                                                                                                                | IS NOT |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| **Edge AI Studio**             | [Edge AI Studio](https://www.ti.com/tool/EDGE-AI-STUDIO/)                                                  | GUI based, No-Code AI development for MCUs and MPUs - Data Capture, Annotation, Model Training, Compilation and Live Preview                                         |        |
| **Tiny ML Model development for MCUs**        | [tinyml-tensorlab](https://github.com/TexasInstruments/tinyml-tensorlab)                                            | Commandline based development for advanced users - Model Zoo, ModelMaker, Model Optimization Tools, Model training, compilation, examples and other tools. Browse the link for detailed documentation. |        |
| **Tiny ML Model Optimization Toolkit**        | [tinyml-modeloptimization](https://github.com/TexasInstruments/tinyml-tensorlab/tree/main/tinyml-modeloptimization) | This open-source software framework provides a flexibility for customers with their own training frameworks to optimize their models for TI devices with TinyEngine™ NPUs.                  |        |
| **Neural Network Compilation Tools for MCUs** | [Neural Network Compiler for MCUs](https://software-dl.ti.com/mctools/nnc/mcu/users_guide/)                         | Compile Neural Network Models for accelerated inference in TI MCUs                                                                                                                                     |        |

<hr>

## 5. Benchmarks for Models and Devices

TI provides a range of benchmarks for Edge AI models and devices, including:
* Models: TI's tinyml-modelzoo repository provides a range of pre-trained models for various applications, including image classification, object detection, and speech recognition. These models can be used as benchmarks for evaluating the performance of Edge AI systems.  (Refer this: https://github.com/TexasInstruments/tinyml-tensorlab/tree/main/tinyml-modelzoo )
* Devices: TI provides benchmarks for its range of MCUs, including C2000, MSPM0 and Connectivity MCUs. These benchmarks provide a measure of the performance and power consumption of these devices in various Edge AI applications.

<hr>

Edge AI applications on MCUs offer a range of benefits, including improved real-time decision-making, reduced latency, and enhanced security. TI's comprehensive portfolio of devices, software tools, and solution offerings provides a robust ecosystem for developing and deploying Edge AI applications. The BYOD and BYOM workflows provide developers with the flexibility to use their own data and models with TI's Edge AI solutions, reducing development time and improving performance. By leveraging TI's Edge AI solutions, developers can build a wide range of applications, from arc fault monitoring to fan blower imbalance detection, and take advantage of the benefits of Edge AI on MCUs.

<hr>

