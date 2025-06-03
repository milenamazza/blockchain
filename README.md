# **Detecting Illicit Bitcoin Transactions with Graph Neural Networks**  

This project leverages **Graph Neural Networks (GNNs)** to identify suspicious transactions in Bitcoin’s blockchain using the **Elliptic++ dataset**, an enhanced version of the Elliptic dataset that includes wallet interactions for deeper fraud detection.  

---

## **📌 Project Highlights**  

### **🔍 Problem Statement**  
Blockchain transactions are pseudonymous but not anonymous. While all transactions are public, detecting illicit activity (e.g., money laundering, darknet markets) remains challenging due to:  
✔ **Complex transaction patterns**  
✔ **Heavy class imbalance** (few illicit transactions)  
✔ **Dynamic network structure**  

### **🛠️ Our Approach**  
We implemented and compared **three GNN architectures**:  
1. **GraphSAGE (SAGEConv)** – Efficient neighborhood aggregation  
2. **Graph Attention Network (GATConv)** – Learns node importance dynamically  
3. **Transformer-based GNN** – Captures long-range dependencies  

### **⚙️ Key Steps**  
1. **Data Preprocessing**  
   - Standardization & normalization  
   - PCA for dimensionality reduction  
   - Handling class imbalance via weighted loss  

2. **Model Training & Evaluation**  
   - **Balanced accuracy & F1-score** (due to class imbalance)  
   - Early stopping to prevent overfitting  

3. **Network Analysis**  
   - Transaction & wallet graph metrics  
   - Temporal behavior patterns  

---

## **🚀 Results**  

| **Model**       | **Balanced Accuracy (Transactions)** | **Balanced Accuracy (Wallets)** |
|----------------|----------------------------------|-----------------------------|
| **GraphSAGE**  | 91.29%                          | 87.92%                      |
| **GAT**        | 56.91%                          | 51.82%                      |
| **Transformer**| **92.51%** ✅                   | **89.16%** ✅               |

### **🔑 Key Findings**  
✔ **Transformer GNN performed best** due to its ability to capture complex relationships.  
✔ **Preprocessing (PCA + standardization) significantly improved results.**  
✔ **Wallet classification is harder** than transaction classification (lower accuracy).  
✔ **Illicit transactions show stronger feature correlations** than legal ones.  

---

## **📂 Repository Structure**  
The repository contains:  
- **`00_GNN/`** – Code for model training (`GNN.ipynb`) and results analysis (`Risultati.ipynb`).  
- **`Analisi/`** – Social network and statistical analysis of the dataset.  
- **`docs/`** – Full project report (`Blockchain.pdf`).  

---
The project doesn't contain some of the original file because they're over than 100 MB.

## **👥 Contributors**  
- Benedetta Bottari  
- Claudia Brunetti  
- Milena Mazza  

📜 **License:** MIT  
📄 **Full Report:** [`docs/Blockchain.pdf`]
