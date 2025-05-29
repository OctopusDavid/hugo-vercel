---
title: "Audiblez_有声书转换"
date: 2025-05-28T09:33:52+08:00
lastmod: 2025-05-28T09:33:52+08:00
draft: true
keywords: []
description: ""
tags: [效率工具，有声书]
categories: [工具]
author: ""

# Uncomment to pin article to front page
# weight: 1
# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: false
autoCollapseToc: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: false

# Uncomment to add to the homepage's dropdown menu; weight = order of article
# menu:
#   main:
#     parent: "docs"
#     weight: 1
---

<!--more-->

Audiblez这是一款什么软件 ？



###### ChatGPT said:

Audiblez 是一款开源免费工具，能够将 `.epub` 格式的电子书快速转换为 `.m4b` 格式的高质量有声书。它使用 Kokoro-82M 语音合成模型，生成自然流畅的朗读效果，支持多种语言，包括中文、英文、日文等。[GitHub+6Abab Tools+6掌中宝分享+6](https://ababtools.com/?post=5222&utm_source=chatgpt.com)[Abab Tools+5Remeins+5掌中宝分享+5](https://remeins.com/index/item/6818a8909833a?utm_source=chatgpt.com)

------

### 🔧 主要功能与特点

- **多语言支持**：支持中文、英文、日语、法语、葡萄牙语等多种语言。
- **多种语音选择**：提供多种自然逼真的语音选项，如中文的 `zf_xiaobei`、`zm_yunyang` 等。
- **高效转换**：在支持 CUDA 的 GPU 上，转换速度可达约 600 字符/秒；在 CPU 上也能实现约 60 字符/秒的速度。
- **图形界面支持**：除了命令行工具外，还提供简洁易用的图形用户界面（GUI），方便非技术用户操作。
- **播放速度调节**：支持 0.5 至 2.0 倍速的朗读速度调节。
- **章节选择功能**：允许用户选择性地转换特定章节，无需处理整本书。
- **多平台兼容**：兼容 Windows、macOS 和 Linux 系统。[掌中宝分享+1GitHub+1](https://ziyuan.run/777?utm_source=chatgpt.com)[AishareNet+1GitHub+1](https://www.aisharenet.com/audiblez/?utm_source=chatgpt.com)

------

### 🚀 安装与使用指南

#### 1. 安装依赖

- **Ubuntu/Debian**：

  ```
  bash复制编辑sudo apt install ffmpeg espeak-ng
  pip install audiblez:contentReference[oaicite:33]{index=33}
  ```

- **macOS**：

  ```
  bash复制编辑brew install ffmpeg espeak-ng
  pip install audiblez:contentReference[oaicite:38]{index=38}
  ```

- **Windows**：

  1. 打开终端，创建并进入新文件夹：

     ```
     bash复制编辑mkdir audiblez
     cd audiblez
     ```

  2. 创建并激活虚拟环境：[掌中宝分享](https://ziyuan.run/777?utm_source=chatgpt.com)

     ```
     bash复制编辑python -m venv venv
     .\venv\Scripts\Activate.ps1
     ```

  3. 安装依赖：[掌中宝分享](https://ziyuan.run/777?utm_source=chatgpt.com)

     ```
     bash
     
     
     复制编辑
     pip install audiblez pillow wxpython
     ```

#### 2. 下载必要的模型文件

```
bash复制编辑wget https://github.com/thewh1teagle/kokoro-onnx/releases/download/model-files/kokoro-v0_19.onnx
wget https://github.com/thewh1teagle/kokoro-onnx/releases/download/model-files/voices.json:contentReference[oaicite:54]{index=54}
```

#### 3. 转换电子书为有声书

```
bash


复制编辑
audiblez book.epub -l zh -v zf_xiaobei:contentReference[oaicite:57]{index=57}
```

- `-l`：指定语言代码（如 `zh` 表示中文）。
- `-v`：指定语音名称（如 `zf_xiaobei`）。

转换完成后，会在同一目录下生成多个 `.wav` 文件，最终合并为一个 `.m4b` 文件，可使用 VLC 或其他有声书播放器播放。[Zhihu Column+7AishareNet+7GitHub+7](https://www.aisharenet.com/audiblez/?utm_source=chatgpt.com)

------

### 🖥️ 图形界面（GUI）使用

安装 GUI 所需依赖：[GitHub](https://github.com/santinic/audiblez?utm_source=chatgpt.com)

```
bash


复制编辑
pip install audiblez pillow wxpython:contentReference[oaicite:73]{index=73}
```

启动 GUI：

```
bash


复制编辑
audiblez-ui:contentReference[oaicite:79]{index=79}
```

------

### ⚙️ 高级功能

- **调整朗读速度**：

  ```
  bash
  
  
  复制编辑
  audiblez book.epub -v zf_xiaobei -s 1.5:contentReference[oaicite:82]{index=82}
  ```

其中 `-s` 参数用于设置朗读速度，范围为 0.5 至 2.0。

- **启用 GPU 加速**：

  ```
  bash
  
  
  复制编辑
  audiblez book.epub -v zf_xiaobei --cuda:contentReference[oaicite:88]{index=88}
  ```

使用 `--cuda` 参数可启用 GPU 加速，提高转换速度。

------

### 📚 相关资源

- GitHub 项目地址：[GitHub](https://github.com/santinic/audiblez?utm_source=chatgpt.com)
- Kokoro 语音模型：[GitHub](https://github.com/santinic/audiblez?utm_source=chatgpt.com)
- 详细语音列表及试听：[GitHub](https://github.com/santinic/audiblez?utm_source=chatgpt.com)

------

如果您需要进一步的帮助，例如如何在特定平台上安装 Audiblez，或如何选择适合的语音模型，请随时提问！



##### You said:

Kokoro-82M 是开源的吗？



###### ChatGPT said:

是的，**Kokoro-82M** 是一款开源的文本转语音（TTS）模型，采用 Apache 2.0 许可证发布，允许在个人和商业项目中免费使用和修改。该模型由开发者 @hexgrad 发布，拥有 8200 万参数，尽管体积较小，但在语音质量和效率方面表现出色，甚至超过了一些参数量更大的模型，如 MetaVoice（12 亿参数）和 XTTS（4.67 亿参数） 。[Hugging Face+8Medium+8Kokoro TTS+8](https://medium.com/@r3cheese/kokoro-82m-a-cutting-edge-tts-model-350-mb-4a849094e38a?utm_source=chatgpt.com)[Replicate+7Kokoro TTS+7GitHub+7](https://kokorotts.net/models/Kokoro/Kokoro-82m?utm_source=chatgpt.com)

### ✅ 开源许可与使用权利

- **许可证**：Apache 2.0（商业友好型） 。
- **用途**：可用于商业部署、产品集成、研究项目和个人应用，无需支付授权费用。
- **模型权重**：可从 Hugging Face 下载，支持本地部署 。[GitHub](https://github.com/hexgrad/kokoro?utm_source=chatgpt.com)[Medium+1GitHub+1](https://medium.com/@r3cheese/kokoro-82m-a-cutting-edge-tts-model-350-mb-4a849094e38a?utm_source=chatgpt.com)

### 🧠 技术架构与性能优势

- **架构基础**：基于 StyleTTS 2 和 ISTFTNet，采用仅解码器结构，无需扩散或编码器发布 。
- **多语言支持**：支持多种语言，包括英语、中文、日语、法语、葡萄牙语等 。
- **部署灵活性**：可在 CPU 或 GPU 上运行，支持 ONNX 格式，适用于边缘设备和低功耗系统 。[Hugging Face+2Medium+2Medium+2](https://medium.com/@r3cheese/kokoro-82m-a-cutting-edge-tts-model-350-mb-4a849094e38a?utm_source=chatgpt.com)

### 🚀 获取与使用方式

- **模型下载**：可从 Hugging Face 获取模型权重和相关文件。

- **推理库**：提供 Python 推理库 `kokoro`，可通过 pip 安装：[Medium](https://medium.com/@r3cheese/kokoro-82m-a-cutting-edge-tts-model-350-mb-4a849094e38a?utm_source=chatgpt.com)[GitHub](https://github.com/hexgrad/kokoro?utm_source=chatgpt.com)

  ```
  bash
  
  
  复制编辑
  pip install kokoro
  ```



- **示例代码**：官方提供了在 Google Colab 上运行的示例，便于快速上手 。[GitHub](https://github.com/hexgrad/kokoro?utm_source=chatgpt.com)

### 🔗 相关资源

- **模型主页**：[Hugging Face - Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M)
- **GitHub 仓库**：[hexgrad/kokoro](https://github.com/hexgrad/kokoro)
- **在线演示**：[Hugging Face Spaces - Kokoro-TTS](https://huggingface.co/spaces/hexgrad/Kokoro-TTS)[GitHub+7Hugging Face+7Medium+7](https://huggingface.co/hexgrad/Kokoro-82M?utm_source=chatgpt.com)[Medium+3GitHub+3Hugging Face+3](https://github.com/hexgrad/kokoro?utm_source=chatgpt.com)[Analytics Vidhya+3Medium+3Hugging Face+3](https://medium.com/@simeon.emanuilov/kokoro-82m-building-production-ready-tts-with-82m-parameters-unfoldai-98e36ff286b9?utm_source=chatgpt.com)

如果您需要进一步的帮助，例如如何在特定平台上部署 Kokoro-82M，或如何集成到现有应用中，请随时提问！



##### You said:

与edge-tts相比中文语音效果怎么样



###### ChatGPT said:

在中文语音效果方面，**Kokoro-82M** 和 **edge-tts（微软 Edge TTS，也就是 Azure TTS）** 各有优劣：

------

### 🎤 中文语音效果对比

| 对比维度       | Kokoro-82M                              | Edge-TTS（微软语音）                         |
| -------------- | --------------------------------------- | -------------------------------------------- |
| **语音自然度** | 高，自然但略带合成感                    | 非常高，接近真人朗读，情感表达优秀           |
| **语调控制**   | 一般，有基本的语调，但不如 Edge 灵活    | 强，可调节语速、语调、情感、停顿等参数       |
| **多语种能力** | 支持中文、英文、日文等                  | 多语种极强，尤其中文和多音字处理表现极好     |
| **声音种类**   | 有多种音色（如 zf_xiaobei、zm_yunyang） | 官方提供几十种中文声音，包括男声、女声、小孩 |
| **部署方式**   | 本地部署，支持 ONNX，隐私强             | 云端调用（需联网），依赖微软服务器           |
| **许可证**     | 开源 Apache 2.0，可商用                 | 免费额度有，超出需付费，商用需申请授权       |
| **生成速度**   | 快，支持 GPU 加速                       | 非常快，微软云强大                           |
| **情感表达**   | 中等，有轻微语调变化                    | 强，可模拟生气、开心、沉稳等语气             |



------

### ✅ 建议使用场景

- **推荐使用 Kokoro-82M 的情况**：
  - 希望**完全本地运行**，无网络依赖
  - 需要免费、**无需 API 授权**的商用解决方案
  - 有一定开发能力，愿意调试环境与参数
- **推荐使用 edge-tts 的情况**：
  - 对**语音自然度要求极高**
  - 希望快速部署、无需训练模型
  - 有一定预算或能接受调用微软 API（有免费额度）

------

### 🎧 示例对比（简要评价）

假设朗读一段中文文章：

- **Kokoro-82M**：语速自然，断句基本准确，但略有“机器感”，语调不如人类自然。
- **Edge-TTS（zh-CN-XiaoxiaoNeural）**：几乎可以以假乱真，语调变化丰富，断句、停顿处理得非常像真人播音。

------

### 总结

- 如果你追求极致的中文语音自然度：**Edge-TTS 更胜一筹**
- 如果你追求开源、隐私、免费商用、灵活可控：**Kokoro-82M 是非常出色的选择**

是否想我帮你生成一段同样文本，分别用这两种 TTS 演示对比？



##### You said:

Audiblez是不是要强大的显卡性能才可以运行？



###### ChatGPT said:

不一定，**Audiblez 不强制依赖高性能显卡（GPU）**，但是否使用 GPU 会影响生成速度。下面是它对硬件的要求与运行效率的说明：

------

### ✅ **是否必须要 GPU？**

**不是必须。Audiblez 可在 CPU-only 的环境下运行。**

- 如果你只有普通电脑（没有独显）：可以正常运行，但语音合成速度较慢；
- 如果你有支持 CUDA 的 NVIDIA 显卡：可以开启 `--cuda` 模式，大幅提速；

------

### 🚀 **性能对比：GPU vs CPU**

| 硬件类型                             | 每秒处理字符数（大致）           | 是否推荐     |
| ------------------------------------ | -------------------------------- | ------------ |
| **CPU（普通笔电）**                  | ~60 字符/秒                      | ✔️ 可用，但慢 |
| **NVIDIA GPU（如 RTX 3060 及以上）** | ~600 字符/秒                     | ✅ 推荐       |
| **无 GPU 的服务器**                  | 慢，适合小规模处理               | ✔️ 凑合用     |
| **MacBook M 系芯片**                 | 可以使用，但目前不支持 CUDA 加速 | ✔️ 可用       |



------

### 🛠️ 使用 GPU 加速（可选）

如果你有 NVIDIA 显卡 + 正确的 CUDA 驱动，可在命令行加参数启用加速：

```
bash


CopyEdit
audiblez yourbook.epub --cuda
```

> 💡 注意：首次运行会下载 Kokoro-82M 模型，建议在网络环境良好下操作。

------

### 📦 建议配置

最低推荐（仅 CPU）：

- 双核 CPU（i5、Ryzen3 等）
- 8GB 内存
- 安装 Python + ffmpeg + espeak-ng

推荐配置（带 GPU）：

- NVIDIA RTX 2060 或以上
- CUDA 11.x 驱动
- Python >= 3.8
- 至少 16GB 内存（并非强制）

------

### 总结

- 没有 GPU 也可以运行 Audiblez，只是速度较慢；
- 有显卡（尤其是 NVIDIA GPU）能大大提升转换效率；
- 不适合在性能极低的设备（如树莓派）上跑大部头电子书。

是否需要我帮你写一个能自动检测系统是否支持 CUDA 加速的 Python 脚本？



##### You said:

Audiblez我可不可以改一下做成桌面端商用？



###### ChatGPT said:

可以，**你完全可以在遵守开源协议的前提下，将 Audiblez 改造成桌面端应用并进行商业化**，因为它的核心依赖（包括 Kokoro-82M 和 Audiblez 本身）都使用了**宽松的 Apache 2.0 开源协议**。

------

### ✅ 商用可行性分析

| 项目              | 是否允许商用 | 许可证类型   | 商用限制说明                      |
| ----------------- | ------------ | ------------ | --------------------------------- |
| **Audiblez**      | ✔️ 可以       | Apache 2.0   | 可修改、发布、收费，无需署名      |
| **Kokoro-82M**    | ✔️ 可以       | Apache 2.0   | 同样可用于商业产品                |
| **Python 依赖库** | ✔️ 多数可用   | 常见开源协议 | wxPython、ffmpeg 等需注意打包方式 |



------

### 💡 商用改造建议

#### 1. **打包为桌面应用（跨平台 GUI）**

可使用以下方式将 Audiblez 改造成 GUI 软件：

- 用 **PyInstaller** 或 **cx_Freeze** 打包为 `.exe` / `.app`
- 保留 GUI（Audiblez 已提供 `audiblez-ui` 界面，可拓展）
- 可选重写 GUI：用 PyQt / Electron / Flutter 重构界面

#### 2. **增加功能来提升商业价值**

可考虑添加：

- 拖拽支持
- 多语音试听功能
- 用户输入关键词自动分章节
- 内置 TTS 试听播放器
- 云同步（付费会员功能）

#### 3. **设置付费机制（例如）**

- 免费版：限制每次转换章节数、语音类型
- 专业版：提供完整转换、更多语音包
- 企业版：批量转换 + 高速多线程

#### 4. **注意事项**

- 音频文件生成过程涉及 `ffmpeg`，注意遵循 LGPL 许可或将其作为外部依赖
- GUI 使用的 `wxPython` 可以商用，但需要确认二进制打包合规性
- 商用发布前建议在**关于页中附带开源组件说明**

------

### 📦 商用变体案例设想

你可以把它包装成：

> “一键将电子书变成听书”的本地 AI 桌面软件
>  适合阅读障碍人群、视力不便者、播客制作者、内容再创作人士

**名称建议**：

- ReadToVoice Pro
- AI 朗读精灵
- 本地智能听书工坊

------

### ✅ 总结

你完全可以基于 Audiblez 进行**改造、打包和商用**，这是开源工具的价值之一。只要你：

- 遵守 Apache 2.0 协议（即不违反其商标、专利等条款）
- 避免直接使用作者的商标或 logo 进行误导性宣传

就可以合法推出自己的产品。

------

如果你想，我可以：

- 帮你设计一套产品 UI 思路
- 帮你写一个 PyInstaller 打包脚本
- 帮你添加功能（如播放试听、配置管理界面）

你打算做 Windows 桌面端还是多平台版本？



##### You said:

Kokoro-82M哪里可以试听？



###### ChatGPT said:

你可以在以下几个地方试听 **Kokoro-82M** 的语音效果（包括中文）：

------

### 🔊 1. **在线试听地址（最推荐）**

#### ✅ Hugging Face 官方 Demo：

- 地址：https://huggingface.co/spaces/hexgrad/Kokoro-TTS
- 操作：在页面下方输入文本，选择语音（如 `zh_yunyang` 或 `zf_xiaobei`），点击“Submit”试听。

📌 **支持多语言**，包括中文、英文、日文等，部分中文语音如：

- `zf_xiaobei`（女声）
- `zm_yunyang`（男声）
- `zm_huiwei`（温柔女声）

------

### 🔊 2. **Kokoro 官方网站**

- 地址：https://kokorotts.net/models/Kokoro/Kokoro-82m
- 页面中也有几个官方提供的示例音频（支持中英日等语种）

------

### 🔊 3. **第三方博客试听演示（轻量加载）**

- 示例：Mike Esto 的博客对比了多种硬件下的语音效果，附带播放链接：
  - 地址：https://mikeesto.com/posts/kokoro-82m-pi/

------

### 💻 4. **本地部署试听（适合开发者）**

如果你想自己部署来生成音频试听，可以：

```
bash


CopyEdit
pip install kokoro
```

然后运行以下 Python 示例：

```
pythonCopyEditfrom kokoro import TTS

tts = TTS()
tts.tts_to_file("今天天气真好，我们一起去郊游吧。", "test.wav", speaker="zf_xiaobei", language="zh")
```

> 输出为本地 WAV 文件，可用任何播放器打开试听。

------

需要我帮你从在线演示生成几个试听音频并提供链接吗？
