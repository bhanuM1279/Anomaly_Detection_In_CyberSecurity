# Anomaly_Detection_In_CyberSecurity




Random Forest — Supervised Baseline

Random Forest was evaluated as a supervised classification baseline. However, the BETH training partition contains 763,144 normal observations and zero anomaly observations. Therefore, the classifier has no examples from which to learn the anomaly class. As a result, it predicts the test observations as normal and achieves 0% anomaly recall. This demonstrates why supervised classification is unsuitable under the normal-only training setup used by this dataset
