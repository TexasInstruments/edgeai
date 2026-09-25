

## Overview

The figure below provides a high level summary of the relevant tools
![Edge AI tools overview](assets/workblocks_tools_software.svg ':size=800')

## Workflows

#### Bring your own model (BYOM) workflow
![BYOM workflow](assets/workflow_bring_your_own_model.svg ':size=800')

#### Train your own model (TYOM) workflow
![TYOM workflow](assets/workflow_train_your_own_model.svg ':size=800')
* PyTorch is used within edgeai-modeloptimization. Other training frameworks may be used without our optimization and QAT tools, but models must export to ONNX or TFLITE format. 

#### Bring your own data (BYOD) workflow
![BYOD workflow](assets/workflow_bring_your_own_data.svg ':size=800')

<hr>

