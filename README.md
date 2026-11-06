# Titanic Survival Data Analysis (EDA)

## 1. 项目是什么？
这是一个基于经典 Kaggle Titanic 数据集的探索性数据分析（EDA）项目。使用 Python 的 Pandas 进行数据清洗、特征分析，并使用 Seaborn 和 Matplotlib 进行数据可视化。旨在探索影响乘客生存率的关键因素，为后续的机器学习建模提供数据洞察。

## 2. 数据从哪来？
数据来源于 Kaggle 网站数据集https://www.kaggle.com/datasets/ashishkumarjayswal/titanic-datasets/data
*(注：本项目使用的数据集包含 891 行，11 列特征)*

## 3. 项目里有什么？
- `notebooks/`：存放核心分析代码 `titanic_analysis.ipynb`，包含完整的清洗、分析与可视化流程。
- `reports/figures/`：存放分析过程中导出的所有可视化图表（如柱状图、箱线图、热力图等）。
- `requirements.txt`：项目所需的 Python 依赖库列表。

## 4. 怎么运行？
1. 克隆本仓库到本地：
   ```bash
   git clone <你的仓库链接>
   ```
2. 安装依赖环境：
   ```bash
   pip install -r requirements.txt
   ```
3. 启动 Jupyter Notebook 并打开分析文件：
   ```bash
   jupyter notebook notebooks/titanic_analysis.ipynb
   ```

🔍 主要发现 (Key Insights)

通过对数据的清洗与可视化分析，我们得出了以下核心结论：

1. 性别是影响生存的最强因素：女性生存率显著高于男性，符合“妇女儿童优先”的历史事实。
2. 社会阶层（舱位）影响显著：头等舱（Pclass 1）生存率最高，三等舱（Pclass 3）最低。此外，箱线图显示头等舱乘客整体年龄偏大，而三等舱以年轻人为主。
3. 家庭与票价特征：热力图显示，票价（Fare）与生存率呈一定正相关；同时，同行的父母/子女数（Parch）与兄弟姐妹/配偶数（SibSp）存在较强正相关，说明当时多为家庭结伴出行。
4. 数据清洗：处理了 Age 的缺失值（用中位数填补），剔除了严重缺失的 Cabin 特征。