# 在Thinkforce NPU40T平台上部署Stable Diffusion

本文档提供在Thinkforce NPU40T 上使用天数GPU部署[Stable Diffusion](https://github.com/CompVis/stable-diffusion) ComfyUI的详细说明。

## 目录
- [先决条件](#先决条件)
- [安装](#安装)
- [下载模型](#下载模型)
- [运行Stable Diffusion](#运行stable-diffusion)
- [故障排除](#故障排除)
- [参考文献](#参考文献)

## 先决条件

在开始之前，请确保你具备以下条件：

- 天数GPU
- 天数GPU驱动程序
- 天数GPU专用软件(pytorch)

## 安装

1. **克隆仓库**

    ```bash
    git clone https://github.com/comfyanonymous/ComfyUI.git
    cd ComfyUI
    ```

2. **创建并激活Python虚拟环境**

    建议创建一个虚拟环境以避免依赖冲突，已有环境可直接进入。

    ```bash
    conda create --name sdxl python=3.10
    conda activate sdxl
    ```

3. **安装所需的Python包**

    使用`pip`安装所需的依赖项：

    ```bash
    pip install -r requirements.txt
    ```

4. **安装天数专用的PyTorch**
   
    ```bash
    pip install path/to/yourfile.whl
    ```
## 下载模型

使用Stable Diffusion需要下载预训练模型权重。

1. **下载预训练模型**

    你可以从[Huggingface](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/tree/main)下载模型。
    例如 sd_xl_base_1.0.safetensors

3. **将模型移动到适当的目录**

    将下载的模型移动到 `models/checkpoints/` 下。

## 运行Stable Diffusion

一切设置完成后，你可以使用预训练模型生成图像。

1. **运行**

    运行server：

    ```bash
    python3 main.py --listen 0.0.0.0 --port 8188
    ```

2. **访问UI**

    局域网访问 ip:8188

## 故障排除


## 参考文献

---

如果你遇到任何问题，欢迎提出问题或贡献代码！
