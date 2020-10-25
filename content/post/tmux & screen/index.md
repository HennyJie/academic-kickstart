---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Tmux and Screen 常用指令"
subtitle: ""
summary: "frequent using command, multiple session ssh"
authors: []
tags: ["linux, ssh"]
categories: ["linux, memo"]
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

一些常用的screen和tmux指令，混入virtualenv指令，方便使用turing的时候查阅。

### screen
- 创建screen会话
```ssh
screen -S RunWork
```

- 运行作业与会话detach
```ssh
ctrl-a d
```

- 查看当前所有会话
```ssh
screen -ls
```

- 恢复一个已经detached的会话
```ssh
screen -r SessionID
```

- 更换窗口，默认窗口名: bash
```ssh
screen -x 窗口名(or SessionID)
```

- 杀死一个已经detached的对话
```ssh
screen -X -S SessionID quit
```


### tmux
- 创建会话
```ssh
tmux new -s semi-supervised
```

- 运行作业与会话detach
```ssh
ctrl-b d
```

- 查看当前所有会话
```ssh
ctrl-b s
```

- 恢复一个已经detached的会话
```ssh
tmux attach-session -t semi-supervised
```

### virtualenv
- 创建虚拟环境
```ssh
virtualenv -p python3 xxx_venv
```

- 进入虚拟环境
```ssh
source xxx_venv/bin/activate
```

- 退出虚拟环境
```ssh
deactivate
```