---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Pytorch Geometric Environment"
subtitle: ""
summary: "traps of pytorch, cuda, gcc version conflicts"
authors: []
tags: ["pytorch, pytorch_sparse"]
categories: ["graph data mining"]
date: 2020-10-07T00:00:00+08:00
lastmod: 2020-10-07T00:00:00+08:00
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

本地 GPU 配 pytorch_geometric 被 GCC version 坑过一次了，这次在系里服务器(NVIDIA Quadro RTX 8000)又从头搞了一次，这里记录一下，毕竟以后还要经常和 geometric 打交道（。

### PyG Version Update 
因为使用到新的transformer和WikiCS数据集进行PyG版本更新，感谢[qz](https://sxkdz.github.io/)分享的更新脚本。以下指令存成文件，chmod + x，再执行即可在当下环境中更新。

```ssh
#!/bin/bash
TORCH=$(python -c "import torch; print(torch.__version__)")
CUDA=$(python -c "import torch; version = torch.version.cuda.replace('.', ''); print(f'cu{version}')")
pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html --upgrade
pip install torch-sparse -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html --upgrade
pip install torch-cluster -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html --upgrade
pip install torch-spline-conv -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html --upgrade
pip install torch-geometric --upgrade
```

### torch_sparse

在虚拟环境下安装"torch_sparse" 出现 GNU 版本不支持问题

```ssh
/usr/local/cuda/include/crt/host_config.h:138:2: error: #error -- unsupported GNU version! gcc versions later than 8 are not supported!
  138 | #error -- unsupported GNU version! gcc versions later than 8 are not supported!
      |  ^~~~~
error: command '/usr/local/cuda/bin/nvcc' failed with exit status 1
```

查看 CUDA 和 gcc version

```ssh
cat /usr/local/cuda/version.txt
CUDA Version 10.1.243

gcc -v
gcc version 9.3.0 (Ubuntu 9.3.0-10ubuntu2)
```

As already pointed out, nvcc depends on gcc 8.0. It is possible to configure nvcc to use the correct version of gcc without passing any compiler parameters by adding softlinks to the bin directory created with the nvcc install.

网上给的 solution: basically adding a softlink to the correct version of gcc from this directory:

```ssh
sudo ln -s /usr/bin/gcc-8.0 /usr/local/cuda/bin/gcc
```

(ref: https://stackoverflow.com/questions/6622454/cuda-incompatible-with-my-gcc-version)

### pytorch 和 torch_sparse 调用的 CUDA 版本不一致

安装 pytorch 1.6 时注意 CUDA 版本选 10.1，因为 torch_sparse 只支持到 10.1

```ssh
pip install torch==1.6.0+cu101 torchvision==0.7.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
```

### 修正以后的各种 version

```ssh
pytorch 1.6
CUDA Version 10.1.243
gcc version 8.4.0 (Ubuntu 8.4.0-3ubuntu2)
```

### 然后按照 torch-geometric 的文档安装其他相关 package 即可

```ssh
pip install torch-scatter==latest+cu101 -f https://pytorch-geometric.com/whl/torch-1.6.0.html
pip install torch-sparse==latest+cu101 -f https://pytorch-geometric.com/whl/torch-1.6.0.html
pip install torch-cluster==latest+cu101 -f https://pytorch-geometric.com/whl/torch-1.6.0.html
pip install torch-spline-conv==latest+cu101 -f https://pytorch-geometric.com/whl/torch-1.6.0.html
pip install torch-geometric
```

### 参考资料

https://pytorch.org/ Pytorch 选安装版本

https://pytorch-geometric.readthedocs.io/en/latest/notes/installation.html Installation torch-geometric via Binarie
