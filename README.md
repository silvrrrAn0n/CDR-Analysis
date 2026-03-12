# CDR-Analysis
Automated CDR forensic analysis and anomaly detection using Isolation Forest to identify high-risk callers and network fraud patterns

CDR Anomaly Detection
A machine learning tool to identify high-risk phone numbers from Call Detail Records (CDR) using Isolation Forest.


🚀 Overview
This project analyzes 170k+ call records to detect suspicious behavior (fraud, spam, or telemarketing) by combining heuristic scoring with unsupervised machine learning.
Dataset Source: https://zenodo.org/records/13254389
Target: Top 2% statistical outliers.



📊 Logic & Methodology
Feature Engineering: Aggregates raw logs into Total_Calls, Unique_Contacts, Night_Calls, and Avg_Duration.
Scaling: Uses StandardScaler to ensure volume doesn't overshadow frequency.
Detection: Trains an Isolation Forest (contamination=0.02) to isolate extreme behaviors.
Reporting: Generates a filtered list of "Suspicious" numbers for further forensic investigation.

📈 Results
The model successfully filters 173k+ normal records to identify exactly 3,535 high-risk leads, visualized through logarithmic scaling to handle dense data overlap.
