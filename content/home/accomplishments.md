+++

# Accomplishments widget.

widget = "accomplishments" # See https://sourcethemes.com/academic/docs/page-builder/
headless = true # This file represents a page section.
active = true # Activate this widget? true/false
weight = 50 # Order that this section will appear.

# title = "Accomplish&shy;ments"

title = "Projects"
subtitle = ""

# Date format

# Refer to https://sourcethemes.com/academic/docs/customization/#date-format

date_format = "Jan 2006"

# Accomplishments.

# Add/remove as many `[[item]]` blocks below as you like.

# `title`, `organization` and `date_start` are the required parameters.

# Leave other parameters empty if not required.

# Begin/end multi-line descriptions with 3 quotes `"""`.

[[item]]
organization = "CSI @ Emory University, directed by Prof.Eugene Agichtein"
#organization_url = "https://www.cs.emory.edu/home/"
title = "COVID-19 Search"
url = ""
# certificate_url = "https://www.coursera.org"
date_start = "2020-05-01"
date_end = ""
description = """
* Target: given a topic related to COVID-19, produce a ranked list of documents from a collection of biomedical literature articles per topic ordered by decreasing likelihood that the document matches the information need (still going on).
"""

[[item]]
organization = "CSI @ Emory University, CS570 Data Mining"
#organization_url = "https://www.cs.emory.edu/home/"
title = "Mining of Potential Influencing Factors for COVID19 Spread"
url = ""
# certificate_url = "https://www.coursera.org"
date_start = "2020-04-15"
date_end = "2020-04-30"
description = """
* Use GAM model to check whether environment factors have influence on spread of coronavirus.
* Use SIR model to check whether non-pharmaceutical intervention can help to prevent the spread of coronaviru.
* Fit a Recurrent Neural Network (RNN) model to predict the daily new confirmed cases of tomorrow based on government response and the daily new confirmed cases of today.
"""

[[item]]
organization = "CSI @ Emory University, CS557 Artificial Intelligence"
#organization_url = "https://www.cs.emory.edu/home/"
title = "Automatic Commit Messages Generation from Diffs"
url = ""
# certificate_url = "https://www.coursera.org"
date_start = "2019-10-30"
date_end = "2019-12-18"
description = """
* A hybrid method: TF-IDF ranking method improved with a Seq2Seq model based on pointer generator network.
* TF-IDF part: given a diff string, find the most similar diff and get its comment as candidates.
* Generate model part: use pointer generator network to predict the next word in the target sequence, re-rank the top 10 matching results from the IR method by the possibility matrix obtained from Seq2Seq model.
"""

[[item]]
organization = "Rollins School @ Emory University, directed by Prof.Tianwei Yu"
#organization_url = "https://www.sph.emory.edu/"
title = "DCOL for Nonlinear Distance Calculation Applied to PCA and T-SNE"
url = ""
# certificate_url = "https://www.coursera.org"
date_start = "2017-11-15"
date_end = "2018-03-01"
description = """
* Proposed a new kernel dimension reduction method based on DCOL(Distance Based on Conditional Ordered List), which could reveal strong nonlinear dependencies in the data.
* Adopted squares instead of absolute values and made a transformation on DCOL matrix to make the kernel have a new property.
* Compared the dimension reduction result of the new method with kernel PCA, PCA and T-SNE, and found that the information consistence was increased by introducing the new non-linear distance.
"""

[[item]]
organization = "Computer Vision Lab @ Tongji University, directed by Prof.Lin Zhang"
#organization_url = "https://sse.tongji.edu.cn/En/Default"
title = "Detection and Distance Measurement of Speed Bumps"
url = ""
# certificate_url = "https://www.coursera.org"
date_start = "2018-05-01"
date_end = "2018-07-01"
description = """
* Developed an integral speeds bumps detection and distance measurement system for no-man sweeper vehicles by using Python programming.
* Utilized Yolo v3 net to detect the speed bumps and obtain the position and size of bounding box.
* Detected the speed bumps in the video and outputted the distance between the detected bump and the bracket in real time, optimized the model by redefining the distance calculation.
"""
  
[[item]]
organization = "AI Healthcare Lab @ Tongji University, directed by Prof.Jianwei Lu"
#organization_url = "http://www.tj-ilab.cn/"
title = "Anomaly Detection Framework using Machine Learning Methods"
url = ""
# certificate_url = "https://www.coursera.org"
date_start = "2018-03-01"
date_end = "2018-06-18"
description = """
* Established a new framework for anomaly (CPU, Memory, IO) detection and stress testing, which can forecast potential failures and pressure spills based on performance data.
* Collected random injection failure and normal data by using Clear Water platform, trained the classical set KDDCUP99 and data collected in true environment through machine learning classifiers (SVM, Random Forest, NN, etc.).
* Contrasted the precision, recall rates and F1 score of different classifiers, disovered the highest accuracy (0.997) with using NN methods.
"""

+++
