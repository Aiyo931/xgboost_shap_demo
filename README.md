# 🚦 Traffic Status Prediction & SHAP Explanation

本项目展示了如何构建一个基于 XGBoost 的交通状态预测模型，并使用 SHAP 工具实现模型可解释性分析。

---

## 📌 项目亮点

- 使用 **XGBoostClassifier** 对交通是否拥堵进行分类预测
- 引入 **SHAP（SHapley Additive exPlanations）** 工具解释模型的每个预测结果
- 自动生成单个样本的 **Waterfall 图** 和全局 **Beeswarm 图**
- 支持封装为模块结构，方便复用和 GitHub 展示

---

## 📁 项目结构

```
traffic_shap_explainer/
├── data/
│   └── traffic_sample.csv              # 示例交通数据
├── model/
│   ├── train_classifier.py             # 模型训练函数（XGBoost）
│   ├── shap_explainer.py               # SHAP 分析器
├── notebooks/
│   └── traffic_explainer_demo.ipynb    # Notebook 示例演示
├── report/
│   └── sample_5_waterfall.png          # 输出解释图示例
├── README.md
└── requirements.txt
```

---

## 📊 示例输出

### 分类报告（Classification Report）

| 类别 | 准确率（Precision） | 召回率（Recall） | F1-score |
|------|----------------------|------------------|----------|
| 通畅 | 0.99                 | 0.98             | 0.99     |
| 拥堵 | 0.99                 | 1.00             | 0.99     |

### SHAP Beeswarm 图

- 红点代表特征值高，蓝点代表低
- 点的位置表示它对预测的“推动力”

### SHAP Waterfall 图

- 展示每个特征如何“推动”或“拉低”模型预测值

---

## 🚀 使用说明

### 安装依赖

```bash
pip install -r requirements.txt
```

### 运行 Notebook 演示

```bash
jupyter notebook notebooks/traffic_explainer_demo.ipynb
```

或运行模型训练和解释脚本：

```bash
python model/train_classifier.py
```

---

## 📮 适用场景

- 城市交通分析、红绿灯策略优化
- 模型部署前可视化解释汇报
- 交通大模型训练前特征重要性评估

---

## 🤝 联系作者

欢迎在 GitHub issue 区留言交流模型部署、优化、智能交通项目。
