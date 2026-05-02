# pytorch
# LSTM 人类活动识别 (HAR) 项目

## 项目简介

使用 PyTorch 构建 LSTM 模型，对 UCI Human Activity Recognition 数据集进行时间序列分类。
这是面试 AESIR "AI智能老龄专家" 岗位前的实操练习项目。

## 快速开始

```bash
# 1. 下载数据集（自动下载）
python download_data.py

# 2. 训练模型
python train.py

# 3. 查看训练结果
# 模型会自动保存到 models/ 目录
# 训练曲线图会保存到 outputs/ 目录
```

## 项目结构

```
har_lstm/
├── README.md           # 本文件
├── download_data.py    # 下载UCI HAR数据集
├── dataset.py          # 数据加载与预处理（Dataset类）
├── model.py            # LSTM模型定义
├── train.py            # 训练主脚本
├── evaluate.py         # 模型评估与可视化
├── data/               # 数据集目录（自动创建）
├── models/             # 模型保存目录
└── outputs/            # 输出图表目录
```

## 学到了什么（面试要点）

1. **数据加载**：自定义 Dataset + DataLoader，滑动窗口切分时间序列
2. **模型定义**：nn.Module + LSTM层 + 全连接分类头
3. **训练循环**：前向传播→计算损失→反向传播→更新参数→验证
4. **评估**：准确率、混淆矩阵、分类报告
5. **与岗位关联**：活动识别→跌倒检测，时间序列→可穿戴设备数据
