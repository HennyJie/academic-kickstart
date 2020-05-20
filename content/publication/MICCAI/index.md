---

# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Pulmonary Vessel Segmentation based on Orthogonal Fused U-Net++ of Chest CT Images"
authors:
["[Hejie Cui](https://hejiecui.com/)", "[Xinglong Liu]", "[Ning Huang]"]
date: 2019-10-18T00:00:00+08:00
doi: "10.1007/978-3-030-32226-7_33"

# Schedule page publish date (NOT publication's date).

publishDate: 2019-10-18T00:00:00+08:00

# Publication type.

# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;

# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;

# 7 = Thesis; 8 = Patent

publication_types: ["1"]

# Publication name and optional abbreviated publication name.

publication: "International Conference on Medical Image Computing and Computer-Assisted Intervention 2019"
publication_short: "MICCAI"

# abstract: "

# Along with the benefits of Internet of Things (IoT) come potential privacy risks, since billions of the connected devices are granted to sense information about their users, communicating to other parties over the Internet. Of particular interest to the adversary is the user identity, which, once obtained, can be used for many vicious attacks subsequently. \n

# While the exposure of a particular type of physical biometrics or device IDs is extensively studied, the compound leakage interwoven by both sides remains unknown to users in IoT-rich environments. \n

# In this work, we explore the feasibility of the compound identity leakage across cyber-physical spaces and unveil that co-located smart device IDs (e.g.,

# smartphone MAC addresses) and physical biometrics (e.g., facial/vocal samples) are side channels to each other. Based on the side channels in combination, our presented approach enables an attacker to automatically compromise users' biometrics and device IDs in tandem. \n

# We show that our method is robust to cross-modal mismatch and various observation noise in the wild, comprehensively profiling victims with nearly zero analysis effort from the attacker. \n

# Two real-world experiments on different biometrics and WiFi MAC addresses validate the new type of privacy leakage. We show that in extreme cases, the presented approach can compromise more than 70% device IDs and harvests multiple biometric clusters of 94% purity at the same time. \n

# ![](evilscan_overview.png)\n

# "

# Summary. An optional shortened abstract.

# summary: "In this work, we explore the feasibility of the compound identity leakage across cyber-physical spaces and unveil that co-located smart device IDs (e.g., smartphone MAC addresses) and physical biometrics (e.g., facial/vocal samples) are side channels to each other. Based on the side channels in combination, our presented approach enables an attacker to automatically compromise users' biometrics and device IDs in tandem.

# We show that our method is robust to cross-modal mismatch and various observation noise in the wild, comprehensively profiling victims with nearly zero analysis effort from the attacker. "

tags: ["Pulmonary Vessel Segmentation", "U-Net++", "2.5D CNN"]
categories: []
featured: true

# Custom links (optional).

# Uncomment and edit lines below to show custom links.

links:

- name: Springer
  url: https://link.springer.com/chapter/10.1007/978-3-030-32226-7_33
  # icon_pack: fas
  # icon: terminal

# - name: The Hacker News

# url: https://thehackernews.com/2020/04/deanonymize-device-biometrics.html

# icon_pack: fab

# icon: hacker-news

url_pdf: files/papers/miccai.pdf
url_code:
url_dataset:
url_poster: files/papers/poster.pdf
url_project:
url_slides:
url_source:
url_video:

# Featured image

# To use, add an image named `featured.jpg/png` to your page's folder.

# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.

image:
caption: ""
focal_point: ""
preview_only: true

# Associated Projects (optional).

# Associate this publication with one or more of your projects.

# Simply enter your project's folder or file name without extension.

# E.g. `internal-project` references `content/project/internal-project/index.md`.

# Otherwise, set `projects: []`.

projects: []

# Slides (optional).

# Associate this publication with Markdown slides.

# Simply enter your slide deck's filename without extension.

# E.g. `slides: "example"` references `content/slides/example/index.md`.

# Otherwise, set `slides: ""`.

## slides: ""

![attack_scenario](attack_scenario.png)

Pulmonary vessel segmentation is important for clinical di- agnosis of pulmonary diseases, while is also challenging due to the com- plicated structure. In this work, we present an effective framework and refinement process of pulmonary vessel segmentation from chest com- puted tomographic (CT) images. The key to our approach is a 2.5D seg- mentation network applied from three orthogonal axes, which presents a robust and fully automated pulmonary vessel segmentation result with lower network complexity and memory usage compared to 3D networks. The slice radius is introduced to convolve the adjacent information of the center slice and the multi-planar fusion optimizes the presentation of intra and inter slice features. Besides, the tree-like structure of pul- monary vessel is extracted in the post-processing process, which is used for segmentation refining and pruning. In the evaluation experiments, three fusion methods are tested and the most promising one is compared with the state-of-the-art 2D and 3D structures on 300 cases of lung im- ages randomly selected from LIDC dataset. Our method outperforms other network structures by a large margin and achieves by far the high- est average DICE score of 0.9272 and a precision of 0.9310, as per our knowledge from the pulmonary vessel segmentation models available in literature.

![overview](evilscan_overview.png)
