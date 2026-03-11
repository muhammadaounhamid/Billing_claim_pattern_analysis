# Billing_claim_pattern_analysis
# Skilled Nursing Facility (SNF) Billing Anomaly Detector

## 📌 Project Overview
This repository contains a proprietary machine learning system designed for Skilled Nursing Facility (SNF) Management Companies. The system utilizes advanced anomaly detection algorithms (specifically Isolation Forests) to automatically audit and identify misalignments between clinical documentation and billing claims.

By analyzing historical treatment patterns, the model flags statistical outliers—such as low-acuity patients billed for intensive therapy hours—reducing audit risks, ensuring regulatory compliance, and optimizing revenue cycle management.

## ⚙️ System Architecture
- **Algorithm:** `scikit-learn` Isolation Forest
- **Data Preprocessing:** Standardized scaling for distance/density optimization
- **Visualization:** `seaborn` and `matplotlib` for clear, actionable auditor dashboards
- **Input:** Clinical features (Acuity Score, ADL Score, Comorbidities) and Billing features (Therapy Hours)

## 🚀 How It Works
1. **Data Ingestion:** The system ingests patient clinical data and billed therapy hours.
2. **Standardization:** Features are scaled to ensure clinical metrics and temporal metrics are evaluated evenly.
3. **Anomaly Scoring:** The Isolation Forest algorithm isolates instances that deviate from standard clinical pathways.
4. **Flagging & Visualization:** Claims falling outside the expected distribution are flagged for manual review and plotted on a scatter graph for immediate visual identification.

## 📊 Example Use Case
If a patient with a relatively minor injury (Acuity Score: 2) is billed as receiving eight hours of intensive therapy in a single day, the system recognizes that this pattern deviates from expected clinical treatment and identifies it as a potential anomaly requiring auditor review.

## 💻 Installation & Usage

### Prerequisites
Ensure you have Python 3.8+ installed along with the following libraries:
\`\`\`bash
pip install pandas numpy scikit-learn matplotlib seaborn
\`\`\`

### Running the Engine
1. Clone this repository to your local machine.
2. Ensure `snf_billing_data.csv` is in the root directory.
3. Execute the anomaly detector script:
\`\`\`bash
python snf_anomaly_detector.py
\`\`\`

### Output
The script will output a list of flagged Patient IDs to the terminal and generate a high-resolution scatter plot (`anomaly_visualization.png`) highlighting the exact claims requiring manual review.
