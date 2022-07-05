Getting Started
- [ ] Quick Start Guide 快速使用指南
- [ ] release_notes 发布笔记
- [ ] Support Matrix 支持矩阵
- [x] Installation Guide 安装指南

Inference Library 
- [x] API Reference 推理接口
- [x] Developer Guide 开发者指南
- [x] Sample Support Guide 样例支持指南

Optimized Frameworks
- [ ] Container Release Notes 

Tools
- [ ] ONNX GraphSurgeon API Reference
- [ ] Polygraphy API Reference
- [ ] PyTorch-Quantization Toolkit User Guide
- [ ] TensorFlow Quantization Toolkit User Guide

Licenses
- [ ] LICENSE AGREEMENT FOR NVIDIA SOFTWARE DEVELOPMENT KITS

Archives
- [ ] Documentation Archives



<style>
    .nv_color{
        color:#78B721;
    }
</style>


<h1 class="nv_color">  NVIDIA TensorRT </h1>
<h2 class="nv_color"> 快速入门指南 </h2>

本NVIDIA TensorRT 8.4.1快速入门指南是希望试用TensorRT SDK的开发人员的起点；具体来说，本文演示了如何快速构建应用程序以在TensorRT引擎上运行推理。

<h2 class="nv_color"> 发行说明 </h2>


NVIDIA TensorRT是一个C++库，有助于在NVIDIA GPU上进行高性能推理。它旨在与通常用于培训的深度学习框架结合使用。TensorRT专注于在GPU上快速高效地运行已经训练过的网络，以产生结果；也称为推断。这些发行说明描述了TensorRT 8.4.1产品包的主要功能、软件增强和改进以及已知问题。

<h2 class="nv_color"> 支持矩阵 </h2>
这些支持列表提供了NVIDIA TensorRT 8.4.1 API、解析器和层支持的平台、功能和硬件功能。

<h2 class="nv_color"> 安装指南 </h2>
本NVIDIA TensorRT 8.4.1安装指南提供了安装要求、TensorRT软件包中包含的内容列表以及安装TensorRT的分步说明。

<h1 class="nv_color"> 推理库 </h1>

---
<h2 class="nv_color"> API参考 </h2>
这是NVIDIA TensorRT库的API参考文档。以下API集允许开发人员导入预先训练的模型，校准INT8的网络，并使用TensorRT构建和部署优化的网络。可以从ONNX导入网络。它们也可以使用C++或Python API通过实例化各个层并直接设置参数和权重来编程创建。

<h2 class="nv_color"> 开发者指南 </h2>
本NVIDIA TensorRT开发者指南演示了如何使用C++和Python API实现最常见的深度学习层。它展示了如何使用深度学习框架构建的现有模型，并使用提供的解析器构建TensorRT引擎。《开发人员指南》还为常见用户任务提供了分步说明，例如创建TensorRT网络定义、调用TensorRT生成器、序列化和反序列化，以及如何向引擎提供数据和执行推理；同时使用C++或Python API。

<h2 class="nv_color"> 示例支持指南 </h2>
本示例支持指南概述了GitHub和产品包中包含的所有受支持的NVIDIA TensorRT 8.4.1示例。TensorRT样本特别有助于推荐、机器理解、字符识别、图像分类和目标检测等领域。

<h1 class="nv_color"> 优化的框架 </h1>

---
<h2 class="nv_color"> 容器发布说明 </h2>
TensorRT容器是用于TensorRT开发的易于使用的容器。该容器允许构建、修改和执行TensorRT样本。这些发行说明提供了22.06及更早版本的关键功能、容器中包含的打包软件、软件增强和改进以及已知问题的列表。TensorRT容器每月发布一次，为您提供最新的NVIDIA深度学习软件库和发送到上游的GitHub代码贡献。这些库和贡献都经过了测试、调优和优化。

<h1 class="nv_color"> 工具 </h1>

---
<h2 class="nv_color"> ONNX GraphSurgeon API参考 </h2>
ONNX GraphSurgeon提供了一种创建和修改ONNX模型的方便方法。

<h2 class="nv_color"> Polygraphy API参考 </h2>
Polygraphy是一个工具包，旨在帮助在各种框架中运行和调试深度学习模型。

<h2 class="nv_color"> PyTorch量化工具包用户指南 </h2>
Pytork Quantization是一个工具包，用于通过模拟量化训练和评估Pytork模型。量化可以自动或手动添加到模型中，允许调整模型的准确性和性能。量化模型可以导出到ONNX并导入到即将发布的TensorRT版本中。


<h2 class="nv_color"> TensorFlow量化工具包用户指南 </h2>
NVIDIA TensorFlow量化工具包提供了一个简单的API来量化给定的Keras模型。最初，在目标数据集上训练网络，直到完全收敛。量化步骤包括在预训练网络中插入Q/DQ节点，以模拟训练期间的量化。然后对网络进行几次重新训练，以在称为微调的步骤中恢复精度。

<h1 class="nv_color"> 许可证 </h1>

---
<h2 class="nv_color"> NVIDIA软件开发工具包许可协议 </h2>

本文件是针对NVIDIA TensorRT的NVIDIA软件开发工具包的许可协议。本文档包含NVIDIA TensorRT的特定许可条款和条件。接受本协议即表示您同意遵守适用于本协议所含特定产品的所有条款和条件。
<h1 class="nv_color"> 档案 </h1>

---
<h2 class="nv_color"> 文件归档 </h2>
本归档文件提供了对先前发布的NVIDIA TensorRT文档版本的访问。





1. 前言
    1.1. 手册结构
    1.2. 示例
    1.3. Complementary GPU Features
    1.4. Complementary Software
    1.5. ONNX
    1.6. Code Analysis Tools
    1.7. API Versioning
    1.8. Deprecation Policy
    1.9. 支持
    1.10. How Do I Report A Bug?

2. TensorRT’s Capabilities
    2.1. C++ and Python APIs
    2.2. The Programming Model
        2.2.1. The Build Phase
        2.2.2. The Runtime Phase
    2.3. Plugins
    2.4. Types and Precision
    2.5. Quantization
    2.6. Tensors and Data Formats
    2.7. Dynamic Shapes
    2.8. DLA
    2.9. Updating Weights
    2.10. trtexec
    2.11. Polygraphy


3. C++ API
    3.1. The Build Phase
        3.1.1. Creating a Network Definition
        3.1.2. Importing a Model using the ONNX Parser
        3.1.3. Building an Engine
    3.2. Deserializing a Plan
    3.3. Performing Inference


4. Python API 
    4.1. The Build Phase
        4.1.1. Creating a Network Definition in Python
        4.1.2. Importing a Model using the ONNX Parser
        4.1.3. Building an Engine
    4.2. Deserializing a Plan
    4.3. Performing Inference


5. TensorRT 的工作机制
    5.1. Object Lifetimes
    5.2. Error Handling and Logging
    5.3. Memory
        5.3.1. The Build Phase
        5.3.2. The Runtime Phase
    5.4. Threading
    5.5. Determinism


6. Advanced Topics
    6.1. The Timing Cache
    6.2. Refitting An Engine
    6.3. Algorithm Selection and Reproducible Builds
    6.4. Creating A Network Definition From Scratch
        6.4.1. C++
        6.4.2. Python
    6.5. Reduced Precision
        6.5.1. Network-level Control of Precision
        6.5.2. Layer-level Control of Precision
        6.5.3. Enabling TF32 Inference Using C++
    6.6. I/O Formats
    6.7. Compatibility of Serialized Engines
    6.8. Explicit vs Implicit Batch
    6.9. Sparsity
    6.10. Empty Tensors
    6.11. Reusing Input Buffers
    6.12. Engine Inspector


7. Working With INT8 
    7.1. Introduction to Quantization
        7.1.1. Quantization Workflows
        7.1.2. Explicit vs Implicit Quantization
        7.1.3. Per-Tensor and Per-Channel Quantization
    7.2. Setting Dynamic Range
    7.3. Post-Training Quantization using Calibration
        7.3.1. INT8 Calibration Using C++
        7.3.2. Calibration Using Python
    7.4. Explicit Quantization
        7.4.1. Quantized Weights
        7.4.2. ONNX Support
        7.4.3. TensorRT Processing Of Q/DQ Networks
        7.4.4. Q/DQ Layer-Placement Recommendations
        7.4.5. Q/DQ Limitations
        7.4.6. QAT Networks Using TensorFlow
        7.4.7. QAT Networks Using PyTorch
    7.5. INT8 Rounding Modes


8. Working With Dynamic Shapes
    8.1. Specifying Runtime Dimensions
    8.2. Optimization Profiles
        8.2.1. Bindings For Multiple Optimization Profiles
    8.3. Layer Extensions For Dynamic Shapes
    8.4. Restrictions For Dynamic Shapes
    8.5. Execution Tensors vs. Shape Tensors
        8.5.1. Formal Inference Rules
    8.6. Shape Tensor I/O (Advanced)
    8.7. INT8 Calibration With Dynamic Shapes


9. Extending TensorRT With Custom Layers
    9.1. Adding Custom Layers Using The C++ API
        9.1.1. Example: Adding A Custom Layer With Dynamic Shape Support Using C++
        9.1.2. Example: Adding A Custom Layer With INT8 I/O Support Using C++
    9.2. Adding Custom Layers Using The Python API
        9.2.1. Example: Adding A Custom Layer To A TensorRT Network Using Python
    9.3. Using Custom Layers When Importing A Model With A Parser
    9.4. Plugin API Description
        9.4.1. Migrating Plugins From TensorRT 6.x Or 7.x To TensorRT 8.x.x
        9.4.2. IPluginV2 API Description
        9.4.3. IPluginCreator API Description
    9.5. Best Practices For Custom Layers Plugin


10. Working With Loops
    10.1. Defining A Loop
    10.2. Formal Semantics
    10.3. Nested Loops
    10.4. Limitations
    10.5. Replacing IRNNv2Layer With Loops


11. Working With Conditionals
    11.1. Defining A Conditional
    11.2. Conditional Execution
    11.3. Nesting and Loops
    11.4. Limitations
    11.5. Conditional Examples
        11.5.1. Simple If-Conditional
        11.5.2. Exporting from PyTorch


12. Working With DLA
    12.1. Running On DLA During TensorRT Inference
        12.1.1. Example: sampleMNIST With DLA
        12.1.2. Example: Enable DLA Mode For A Layer During Network Creation
    12.2. DLA Supported Layers
    12.3. GPU Fallback Mode
    12.4. I/O Formats on DLA
    12.5. DLA Standalone Mode
    12.6. Customizing DLA Memory Pools


13. Performance Best Practices
    13.1. Measuring Performance
        13.1.1. Wall-clock Timing
        13.1.2. CUDA Events
        13.1.3. Built-In TensorRT Profiling
        13.1.4. CUDA Profiling Tools
        13.1.5. Tracking Memory
    13.2. Optimizing TensorRT Performance
        13.2.1. Batching
        13.2.2. Streaming
        13.2.3. CUDA Graphs
        13.2.4. Enabling Fusion
            13.2.4.1. Layer Fusion
            13.2.4.2. Types Of Fusions
            13.2.4.3. PointWise Fusion
            13.2.4.4. Q/DQ Fusion
        13.2.5. Limiting Compute Resources
    13.3. Optimizing Layer Performance
    13.4. Optimizing for Tensor Cores
    13.5. Optimizing Plugins
    13.6. Optimizing Python Performance
    13.7. Improving Model Accuracy


14. Troubleshooting
    14.1. FAQs
    14.2. Understanding Error Messages
    14.3. Code Analysis Tools
        14.3.1. Compiler Sanitizers
            14.3.1.1. Issues With dlopen And Address Sanitizer
            14.3.1.2. Issues With dlopen And Thread Sanitizer
            14.3.1.3. Issues With CUDA And Address Sanitizer
            14.3.1.4. Issues With Undefined Behavior Sanitizer
        14.3.2. Valgrind
        14.3.3. Compute Sanitizer









