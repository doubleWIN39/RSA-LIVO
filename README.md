# RSA-LIVO
RSA-LIVO: Robust Semantic-Aided LiDAR-Inertial-Visual Odometry for Unstructured and Sensor-Degraded Environments

Authors: Yingying Lei， Naohiko Hanjima, Yoshinori Fujihira, Jun Dai
Status: Under Review

# Overview

State estimation in vegetation-dense and sensor-degraded environments degrades substantially under the static-world assumption, where wind-induced vegetation sway and dynamic occlusion introduce systematic non-rigid residuals that geometric methods cannot resolve. Existing semantic SLAM approaches often rely on heuristic dynamic-object removal or rigid environmental assumptions, which fail to generalize to complex terrains and result in information loss. Critically, existing methods apply semantic weights as a preprocessing step rather than propagating prediction uncertainty directly into the observation noise covariance, precluding principled Kalman gain modulation based on per-point segmentation reliability. To address these limitations, this article presents RSA-LIVO, a robust semantic-aided LiDAR-inertial-visual odometry framework designed for high-fidelity state estimation. The system introduces an Adaptive Covariance Inflation (ACI) strategy that leverages Dempster-Shafer evidence theory to quantify semantic uncertainty, which is then propagated directly into the observation covariance of an error-state iterated Kalman filter (ESIKF), under the assumption that camera and LiDAR evidence sources provide conditionally independent mass functions. This enables a measurement-aware, soft down-weighting mechanism for semi-static features, such as wind-blown vegetation. Furthermore, a Geometry-Semantic Bidirectional Supervision (GSBS) mechanism is developed as a geometric consistency gate to identify and suppress erroneous semantic guidance caused by motion blur or domain shifts. Extensive evaluations on M3DGR and RELLIS-3D datasets demonstrate that RSA-LIVO significantly outperforms state-of-the-art methods in challenging scenarios. On the M3DGR dataset, RSA-LIVO achieves a mean RMSE reduction of 53.2\% across geometrically degenerate and unstructured sequences, with improvements up to 75.1\% in severe motion-degradation scenarios. In structured dynamic environments, RMSE differences relative to the strongest baseline remain below 0.01 m, confirming that semantic weighting does not degrade nominal performance. In geometrically degenerate sequences, RSA-LIVO maintains a low RMSE of 2.65 m, while standard geometric baselines exceed 27 m. Runtime analysis demonstrates that semantic integration introduces an overhead of up to 9.8\% in large-scale point-cloud sequences, while reducing solver wall-time by up to 14.6\% in dynamic scenarios through early outlier rejection by the geometric consistency gate. These results validate the effectiveness of the proposed uncertainty-aware coupling for achieving consistent and robust localization in complex real-world measurement applications.

# System Architecture

# Repository Status
Welcome to the official repository for RSA LIVO.

Currently, the manuscript is under the final review process. To comply with the our lab's policies, the full source code, dataset configurations, and detailed run instructions are temporarily withheld until acceptance and publish.

The complete codebase will be made publicly available immediately upon the paper's acceptance. Thank you for your patience and interest in our work. Please check back soon!
