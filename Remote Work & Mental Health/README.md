# 遠距工作對心理健康的影響

## 📖 專案簡介
本研究探討 **遠距工作是否對心理健康產生影響**，透過機器學習模型分析影響心理健康的關鍵因素。我們使用來自 **Kaggle** 的數據集，包含 **5000 筆觀測值與 20 個變數**，經過資料清理、探索式資料分析（EDA）、特徵工程及多個機器學習模型的比較，最終選擇 **CatBoost 模型** 進行解釋與優化。

## 🔥 研究動機
隨著 **遠距工作逐漸成為新常態**，其對員工心理健康的影響成為重要議題。我們希望透過數據分析找出關鍵變數，並建立預測模型，提供企業決策參考，以促進更健康的工作環境。

## 📊 數據集與研究方法
### **📂 資料來源**
- 數據集來自 [Kaggle](https://www.kaggle.com/datasets/iramshahzadi9/remote-work-and-mental-health)
- 包含 **5000 筆數據**，涵蓋 **個人背景、工作環境、心理健康評估** 等變數。

### **🔍 研究方法**
1. **探索式資料分析（EDA）**
   - 缺失值處理
   - 目標變數分佈分析
   - 數值型與類別型變數關聯性
   - 相關係數熱力圖
2. **特徵工程**
   - **Label Encoding**、**Target Encoding**
   - **SMOTE 方法** 解決資料不平衡問題
3. **機器學習模型建構**
   - 使用 **PyCaret** 自動篩選模型
   - 訓練 **CatBoost、LightGBM、Gradient Boosting** 等模型
   - 使用 **Accuracy、AUC、Recall、Precision、F1-score** 進行評估
4. **模型解釋性**
   - **SHAP** 分析特徵影響力
   - **特徵重要性分析**

## 🏆 研究結果
- **影響心理健康的關鍵因素**
  1. **每週工時**（Hours Worked Per Week）
  2. **視訊會議次數**（Number of Virtual Meetings）
  3. **地區**（Region）

- **最佳模型：CatBoost**
  | 模型 | Accuracy | AUC | Recall | Precision | F1 |
  |------|----------|------|--------|----------|----|
  | **CatBoost** | **0.7120** | **0.4810** | **0.9255** | **0.7500** | **0.8286** |
  | LightGBM | 0.7270 | 0.4906 | 0.9388 | 0.7567 | 0.8380 |
  | Gradient Boosting | 0.7230 | 0.4736 | 0.9481 | 0.7497 | 0.8373 |

- **SHAP 分析結果**
  - **地區、工時長度、視訊會議次數** 是影響心理健康的主要因素。
  - 視訊會議頻率過高，與心理健康問題呈 **正相關**。

## 🚀 未來展望
- **擴展數據**：增加不同產業、文化背景的數據樣本。
- **提升模型解釋性**：嘗試不同特徵工程技術，如 One-Hot Encoding、Embedding 等。
- **應用於企業健康管理**：提供更精準的員工心理健康評估工具。

## 🔧 技術與工具
- **Python**（pandas、numpy、matplotlib、seaborn）
- **機器學習**（PyCaret、CatBoost、LightGBM）
- **數據預處理**（SMOTE、Label Encoding、Target Encoding）
- **模型解釋性**（SHAP）

## 📂 專案結構

📂 遠距工作對心理健康的影響   
  
│── 📄 remote.ipynb # Jupyter Notebook (完整分析)   
│── 📄 remote_report.pdf # 研究報告 PDF 版本   
│── 📄 remote_briefreport.pdf # 簡報   
│── 📄 README.md # 本文件   


