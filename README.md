# FPGA-AudioProcessingSystem

2024 全国大学生集成电路创新创业大赛获奖项目。  
基于紫光同创 FPGA 的实时音频处理系统。

本仓库为项目的软件侧实现，由本人负责主要算法与上位机相关代码工程，不包含 FPGA 上板工程与硬件设计文件。

---

# Overview

FPGA-AudioProcessingSystem 面向实时语音与音频信号处理场景，围绕：

- 音频去噪
- 人声处理
- 音乐分离
- 音频分类
- 声纹与人物画像分析

构建了一套基于 FPGA + 上位机协同架构的实时音频处理系统。

项目结合：

- FPGA 音频采集与传输
- 数字信号处理（DSP）
- 深度学习音频分类
- 实时频谱分析与可视化

实现对音频流的实时处理与分析。

---

# Competition Background

语音处理技术广泛应用于：

- 手机通信
- 视频会议
- 金融安全
- 刑侦分析
- 智能语音交互
- 实时监测系统

本赛题要求基于紫光同创 FPGA，实现多种实时音频信号处理功能，并完成：

- 实时音频效果展示
- 音频频谱可视化
- 实时分类与识别
- 系统延迟分析

---

# Implemented Functions

## Audio Denoising

通过 FPGA 音频采集与数字滤波，实现：

- 环境噪声抑制
- 基础语音增强
- 实时音频输出

支持通过：

- 扬声器
- 耳机

实时播放处理结果。

---

## Vocal and Music Separation

实现：

- 音乐与人声分离
- 主人声提取
- 背景伴奏抑制

用于：

- 音频分析
- 人声增强
- 后续分类与识别任务

---

## Real-time Audio Visualization

系统支持：

- 时域波形显示
- 实时频谱分析
- 音频处理前后对比展示

用于观察：

- 去噪效果
- 频域变化
- 声音特征结构

---

## Audio Portrait Analysis

支持实时音频人物画像分析，包括：

- 性别识别
- 年龄估计
- 情绪分析

系统采用 FPGA 进行音频采集与传输，并在上位机完成进一步推理分析。

---

## Audio Classification

基于卷积神经网络（CNN）的实时音频分类模块。

支持识别包括但不限于：

- 爆炸
- 尖叫
- 唤醒词
- 环境事件

实现流程：

```text
Audio Input
    ↓
FPGA Signal Acquisition
    ↓
Feature Extraction
    ↓
CNN Classification
    ↓
Real-time Visualization
```

---

# System Architecture

```text
Microphone / Audio Source
            ↓
        FPGA采集
            ↓
   音频预处理与传输
            ↓
        上位机系统
            ↓
 ┌─────────────────┐
 │ 音频去噪         │
 │ 音乐人声分离     │
 │ 频谱分析         │
 │ CNN音频分类      │
 │ 人物画像分析     │
 └─────────────────┘
            ↓
      实时结果展示
```

---

# Technical Stack

## FPGA Side

- 紫光同创 FPGA
- 实时音频采集
- PCIe / Ethernet 数据传输

---

## Software Side

- Python
- NumPy
- SciPy
- PyTorch / TensorFlow
- Librosa
- Matplotlib

---

# Repository Structure

```text
FPGA-AudioProcessingSystem/
│
├── audio_processing/        # 音频处理模块
├── classification/          # CNN音频分类
├── visualization/           # 频谱与波形可视化
├── portrait_analysis/       # 人物画像分析
├── datasets/                # 测试音频与数据集
├── models/                  # 训练模型
├── demo/                    # 演示文件
├── requirements.txt
└── README.md
```

---

# Features

- Real-time audio denoising
- Vocal/music separation
- Audio spectrum visualization
- CNN-based sound classification
- Audio portrait analysis
- FPGA + PC collaborative architecture
- Real-time processing pipeline

---

# Notes

## Current Repository Scope

本仓库仅包含：

- 软件实现
- 上位机算法工程
- 音频分析与深度学习部分

不包含：

- FPGA 上板工程
- Verilog/VHDL 硬件代码
- PCB 与硬件设计文件

---

# Future Work

- FPGA 侧 CNN 推理加速
- 低延迟实时流式推理
- 多通道音频输入
- Transformer 音频建模
- 声纹识别系统
- 端侧部署优化

---

# Acknowledgement

- 紫光同创
- 全国大学生集成电路创新创业大赛
- Open-source audio processing community

---

## FPGA-AudioProcessingSystem

Real-time audio intelligence powered by FPGA and deep learning.
