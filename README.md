**DeFi Anomaly Detection – A Multi-Blockchain Approach**

📌 **Overview**
This project presents a multi-chain anomaly and fraud detection framework for Decentralized Finance (DeFi) transactions. By combining rule-based heuristics with advanced machine learning models, it detects unusual transaction patterns, protocol exploits, and fraudulent activities across multiple blockchain networks such as Ethereum and Binance Smart Chain.

We processed 55,000+ blockchain transactions from 23 DeFi protocols, engineered 400+ blockchain-specific features, and identified ~4% high-risk anomalies, enabling proactive detection and improving ecosystem security.

🎯** Objectives**

Cross-Chain Analysis: Aggregate and normalize transaction data from various blockchains.

Anomaly Detection: Identify deviations like flash loan attacks, rug pulls, and wash trading.

Fraud Identification: Detect malicious intent via transactional and behavioral forensics.

Hybrid Approach: Combine ML algorithms with domain-specific rules for robust detection.

Scalability: Design a flexible framework adaptable to evolving DeFi protocols.

🛠** Methodology**
1. Data Collection
Extracted on-chain data from protocols such as Uniswap, Sushiswap, Yearn Finance using The Graph Protocol.

Features included transaction amounts (in tokens & USD), token metadata, gas metrics, and blockchain attributes.

2. Feature Engineering
Built 414 DeFi-specific features covering liquidity flows, time-based patterns, and protocol interactions.

Applied normalization, one-hot encoding, and dimensionality reduction where necessary.

3. Models Implemented
Isolation Forest – Tree-based anomaly isolation.

Local Outlier Factor (LOF) – Density deviation-based detection.

DBSCAN – Density-based clustering for anomaly identification.

Autoencoder – Reconstruction-based detection trained on normal data.

Variational Autoencoder (VAE) – Probabilistic latent space modeling for anomalies.

LSTM – Temporal sequence modeling for transaction flows.

4. Detection Workflow
Models trained on normal transaction datasets.

Thresholds determined statistically (e.g., 99th percentile reconstruction error).

Anomalies cross-verified with historical fraud case patterns.

📊** Results **

Dataset Size: 55,696 transactions.

Anomalies Detected: ~2,405 (~4.3%) flagged as high-risk.

Key Indicators: TOKENIN/LASTPRICEUSD, TOKENOUT/LASTPRICEUSD, GASLIMIT.

Consistency: VAE anomaly rate (~4.3%) matched Isolation Forest (~5%).

Outcome: Reduced reliance on arbitrary thresholds with a data-driven approach.

📌** Limitations **

Framework is offline; real-time streaming detection is in development.

Limited detection of coordinated cross-chain attacks.

Static models require retraining to keep up with evolving fraud strategies.

🚀 **Future Scope**

Real-Time Monitoring: Integration with live transaction streams for instant alerts.

Self-Learning Models: Adaptive algorithms that evolve with new fraud patterns.

Regulatory Compliance: Risk reporting aligned with emerging DeFi regulations.

DeFi Insurance Integration: Real-time risk assessment for coverage adjustments.
        
⚙️ Installation & Usage

Prerequisites
Python 3.8+

pip or conda

Installation

bash
Copy
Edit
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install -r requirements.txt
Run the Detection Pipeline
bash
Copy
Edit
python src/run_pipeline.py --input data/transactions.csv --output results/anomalies.csv

📜** License **

This project is licensed under the MIT License – see the LICENSE file for details.
