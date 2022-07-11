# 摘要

本 NVIDIA TensorRT 8.4.1安装指南提供了安装要求、 TensorRT 包中包含的内容列表以及安装 TensorRT 的分步说明。

确保您熟悉 [NVIDIA TensorRT](https://docs.nvidia.com/deeplearning/tensorrt/release-notes/index.html) 发行说明的最新功能和已知问题。

有关以前发布的 TensorRT 安装文档，请参见 [TensorRT 归档](https://docs.nvidia.com/deeplearning/tensorrt/archives/index.html)。

# 1. 概述
NVIDIA TensorRT 的核心是一个 C++ 库，有助于对 NVIDIA 图形处理单元(GPU)进行高性能推理。TensorRT 采用训练过的网络，该网络由一个网络定义和一组经过训练的参数组成，并生成高度优化的运行时引擎，为该网络执行推理过程。

TensorRT 提供了 C++ 和 Python 两种 API，通过网络定义 API 表达深度学习模型，或者是 TensorRT 通过解析器加载预定义模型，在在 NVIDIA GPU 上优化并运行他们。TensorRT 采用图优化、层融合等优化方案，同时利用各种高度优化的内核集合找到该模型的最快实现。TensorRT 还提供了一个运行时，您可以使用该运行时在从 NVIDIA Kepler 架构开始的所有 NVIDIA GPU 上执行该网络。

TensorRT 在NVIDIA Pascal、 NVIDIA Volta、 NVIDIA Turing、 NVIDIA Ampere 等架构上还支持了高效的混合精度功能。

# 2. 准备开始
确保您熟悉以下安装要求和注意事项。

从 TensorRT 版本8.4.1开始，zip 包中包含的对 Windows 的 Python 支持已经可以投入生产使用。

如果您正在使用 TensorRT Python API，而 PyCUDA 尚未安装到您的系统上，请参阅安装 PyCUDA。如果在使用 PyCUDA 时遇到任何问题，您可能需要自己重新编译它。有关详细信息，请参阅在 Linux 上安装 PyCUDA。

确保您熟悉 NVIDIA TensorRT 发行说明。

验证您是否安装了 NVIDIA CUDA 工具包。支持以下版本:
- 10.2
- 11.0 --> 11.7

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
## 4.4. RPM安装
## 4.5. pip 文件安装
这个章包含从独立的 pip [wheel 文件](https://pip.pypa.io/en/stable/reference/pip_wheel/) 安装 TensorRT 的说明.


Note: While the TensorRT packages also contain pip wheel files, those wheel files require the rest of the .deb or .rpm packages to be installed and will not work alone. The standalone pip-installable TensorRT wheel files differ in that they are fully self-contained and installable without any prior TensorRT installation or use of .deb or .rpm files.

The pip-installable nvidia-tensorrt Python wheel files only support Python versions 3.6 to 3.10 and CUDA 11.x at this time and will not work with other Python or CUDA versions. Only the Linux operating system and x86_64 CPU architecture is currently supported. These wheel files are expected to work on CentOS 7 or newer and Ubuntu 18.04 or newer.

Note: If you do not have root access, you are running outside a Python virtual environment, or for any other reason you would prefer a user installation, then append --user to any of the pip commands provided.
Before you begin

First install the nvidia-pyindex package, which is required in order to set up your pip installation to fetch additional Python modules from the NGC™ PyPI repo.
If your pip and setuptools Python modules are outdated, then use the following command to upgrade these Python modules. If these Python modules are outdated, then the commands that follow later in this section may fail.

python3 -m pip install --upgrade setuptools pip

Now, you can install the nvidia-pyindex module.

python3 -m pip install nvidia-pyindex

If your project is using a requirements.txt file, then you can add the following line to your requirements.txt file as an alternative to installing the nvidia-pyindex package.

--extra-index-url https://pypi.ngc.nvidia.com

Procedure

    Install the TensorRT Python wheel.

    python3 -m pip install --upgrade nvidia-tensorrt

    The preceding pip command will pull in all the required CUDA libraries and cuDNN in Python wheel format because they are dependencies of the TensorRT Python wheel. Also, it will upgrade nvidia-tensorrt to the latest version if you had a previous version installed.
    If you receive an error message in the form of a Python exception similar to the error message below, then either the nvidia-pyindex package was not set up properly, or you might be using a Python version other than 3.6 to 3.10.

    ##################################################################
    The package you are trying to install is only a placeholder project on PyPI.org repository.
    This package is hosted on NVIDIA Python Package Index.

    This package can be installed as:
    ```
    $ pip install nvidia-pyindex
    $ pip install nvidia-tensorrt
    ```
    ##################################################################

    To verify that your installation is working, use the following Python commands to:
        Import the tensorrt Python module.
        Confirm that the correct version of TensorRT has been installed.
        Create a Builder object to verify that your CUDA installation is working.

    python3
    >>> import tensorrt
    >>> print(tensorrt.__version__)
    >>> assert tensorrt.Builder(tensorrt.Logger())

    If the final Python command fails with an error message similar to the error message below, then you may not have the NVIDIA driver installed or the NVIDIA driver may not be working properly. If you are running inside a container, then try starting from one of the nvidia/cuda:x.y-base-<os> containers.

    [TensorRT] ERROR: CUDA initialization failure with error 100. Please check your CUDA installation: ...

    If the preceding Python commands worked, then you should now be able to run any of the TensorRT Python samples to further confirm that your TensorRT installation is working. For more information about TensorRT samples, refer to the NVIDIA TensorRT Sample Support Guide.


## 4.6. Tar文件安装
## 4.7. Zip文件安装
## 4.8. 附加安装方法
# 5. 更新 TensorRT
# 6. 卸载 TensorRT




