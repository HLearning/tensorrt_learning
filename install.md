# 摘要

本 NVIDIA TensorRT 8.4.1安装指南提供了安装要求、 TensorRT 包中包含的内容列表以及安装 TensorRT 的分步说明。

确保您熟悉 [NVIDIA TensorRT](https://docs.nvidia.com/deeplearning/tensorrt/release-notes/index.html) 发行说明的最新功能和已知问题。

有关以前发布的 TensorRT 安装文档，请参见 [TensorRT 归档](https://docs.nvidia.com/deeplearning/tensorrt/archives/index.html)。

# 1. 概述
NVIDIA TensorRT 的核心是一个 C++ 库，它促进了对 NVIDIA 图形处理单元(GPU)的高性能推断。TensorRT 接受一个经过训练的网络，该网络由一个网络定义和一组经过训练的参数组成，并生成一个高度优化的运行时引擎，该引擎执行该网络的推理过程。

TensorRT 通过 C++ 和 Python 提供 API，帮助通过 网络定义 API 表达深度学习模型，或者通过允许 TensorRT 优化并在 NVIDIA GPU 上运行的解析器加载预定义模型。TensorRT 采用图优化、层融合以及其他优化，同时利用多种高度优化的内核集合找到该模型的最快实现。TensorRT 还提供了一个运行时，您可以使用该运行时在从 NVIDIA Kepler 一代开始的所有 NVIDIA GPU 上执行该网络。

TensorRT 还包括可选的 NVIDIA PascalTM、 NVIDIA VoltaTM、 NVIDIA TuringTM 和 NVIDIA Ampere Architecture 的高速混合精度功能。

# 2. 准备开始
# 3. 下载 TensorRT
确保您是 NVIDIA 开发者计划的成员。如果不是，请按照提示获得访问权限。

## 流程
1. 前往: https://developer.nvidia.com/tensorrt。
2. 单击 "GET STARTED"，然后单击 "Download Now"。
3. 选择您感兴趣的 TensorRT 版本。
4. 选中复选框以同意许可条款。
5. 单击要安装的软件包。开始下载。

# 4. 安装 TensorRT
## 4.1. Debian 安装
## 4.2. App Server 安装
## 4.3. 交叉编译安装
## 4.4. 转速安装
## 4.5. 管道轮档案安装
这个章包含从独立的 pip [wheel 文件](https://pip.pypa.io/en/stable/reference/pip_wheel/) 安装 TensorRT 的说明.


## 4.6. 焦油文件安装
## 4.7. 压缩文件安装
## 4.8. 附加安装方法
# 5. 更新 TensorRT
# 6. 卸载 TensorRT
