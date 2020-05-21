---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "A Method to Predict the Performance and Storage of Executing Contract for Ethereum Consortium-Blockchain"
authors:
  [
    "[Huijuan Zhang]",
    "Admin",
    "[Chengxin Jin]",
    "[Hejie Cui](https://hejiecui.com/)",
  ]
date: 2018-06-22T00:00:00+08:00
doi: "10.1145/3366423.3380108"

# Schedule page publish date (NOT publication's date).
publishDate: 2018-06-22T00:00:00-00:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "International Conference on Blockchain 2020"
publication_short: "ICBC"

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

tags: ["Blockchain", "Ethereum", "Contract", "Performance", "Storage"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
  - name: Springer
    url: https://link.springer.com/chapter/10.1007/978-3-319-94478-4_5
    # icon_pack: fas
    # icon: terminal
# - name: The Hacker News
#   url: https://thehackernews.com/2020/04/deanonymize-device-biometrics.html
# icon_pack: fab
# icon: hacker-news

url_pdf: files/papers/icbc.pdf
url_code:
url_dataset:
url_poster:
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
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

![attack_scenario](attack_scenario.png)

As the fundamental technology of Bitcoin, blockchain enables people to deal with trust problems in network. Ethereum, as a well-known public blockchain, is favored by large companies and organizations for its excellent account model and Turing-complete smart contracts, and is widely used to develop consortium-blockchain. However, the performance and storage of executing contract gradually degrade as the transaction volume increases. Meanwhile, compared with public blockchains, companies need a more accurate estimation of prospective performance and storage based on business scale for decisions making or early warnings. In this paper, a prediction model derived from the core structure of Ethereum’s “World State” is proposed. The proposed model predicts the performance and storage of executing contract based on transaction volume. The comparison between the experimental and predicted data reveals that this model can perform a relative accurate prediction of the prospective system’s performance and storage.

![overview](evilscan_overview.png)
