1. 前言
    1.1. 指南结构
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


9.  Extending TensorRT With Custom Layers
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









