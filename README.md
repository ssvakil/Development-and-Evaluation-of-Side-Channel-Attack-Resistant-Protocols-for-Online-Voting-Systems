🔐 Side-Channel Leakage Evaluation Framework

This repository implements a simulation-based framework for evaluating side-channel resistance of cryptographic implementations under different countermeasures such as masking, blinding, and shuffling.

The framework supports statistical leakage analysis using:

Correlation Power Analysis (CPA)
Welch’s t-test (TVLA)
Mutual Information (MI)
Key ranking metrics
Confidence interval estimation
Heatmap-based leakage visualization
📌 Key Features
AES S-box-based leakage model
First-order Boolean masking simulation
Noise & blinding injection model
Trace generation under multiple attack scenarios
CPA-based key recovery evaluation
Standard TVLA (Welch’s t-test)
Mutual Information leakage estimation
Statistical confidence interval analysis
Automated PDF report generation
Correlation heatmap visualization
📊 Attack & Evaluation Methods
1. Correlation Power Analysis (CPA)

Evaluates statistical dependency between hypothetical power consumption and observed traces.

2. TVLA (Welch’s t-test)

Detects side-channel leakage by comparing two statistically different groups.

3. Mutual Information (MI)

Measures information leakage between traces and plaintexts.

4. Key Ranking Metric

Evaluates how close the correct key is to the top-ranked hypotheses.

🧪 Experimental Setup

The system evaluates multiple countermeasures:

No protection (baseline)
Masking
Blinding (noise injection)
Shuffling
Combined protections

Each scenario is tested across multiple trace sizes:

N = [200, 1000, 5000, 20000]
📂 Output Files

After execution, the following outputs are generated:

📄 PDF Reports
CPA.pdf → Correlation attack strength comparison
TVLA.pdf → Statistical leakage significance
MI.pdf → Information leakage analysis
📊 Heatmaps
CPA_heatmap_<scenario>_<N>.pdf
📑 Dataset
results_table.csv → Numerical summary of all experiments
🚀 How to Run
pip install numpy matplotlib scipy scikit-learn pandas
python main.py
📈 Example Results

The framework provides:

Attack success rate under different defenses
Leakage reduction comparison
Statistical significance of countermeasures
Visualization of correlation leakage patterns
⚠️ Limitations
Simulation-based leakage model (not hardware measured)
Simplified AES S-box abstraction
Does not include EM/power real acquisition
Designed for comparative security analysis, not certification
📚 Intended Use

This framework is intended for:

Academic research in side-channel analysis
Evaluation of cryptographic countermeasures
Educational purposes in cryptographic engineering
👨‍🔬 Future Work
Real power trace integration (ChipWhisperer)
Deep learning-based profiling attacks
Higher-order TVLA extensions
Hardware-in-the-loop validation
