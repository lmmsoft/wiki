# 记录各种小工具

## 代码行数统计工具 cloc
- 安装
```
npm install -g cloc              # cloc
sudo apt install cloc            # Debian, Ubuntu
sudo yum install cloc            # Red Hat, Fedora
sudo dnf install cloc            # Fedora 22 or later
sudo pacman -S cloc              # Arch
sudo emerge -av dev-util/cloc    # Gentoo dev-util/cloc - Gentoo Packages
sudo apk add cloc                # Alpine Linux
doas pkg_add cloc                # OpenBSD
sudo pkg install cloc            # FreeBSD
sudo port install cloc           # macOS with MacPorts
brew install cloc                # macOS with Homebrew
choco install cloc               # Windows with Chocolatey
scoop install cloc               # Windows with Scoop
```

- 使用
```
cloc .
cloc --help
```
- 样例输出, 以gclx-contract 为例
```
       9 text files.
       7 unique files.
       4 files ignored.

github.com/AlDanial/cloc v 1.94  T=0.03 s (268.0 files/s, 578033.6 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
JSON                             2              0              0          14741
JavaScript                       3             22             24            132
Solidity                         1             18              1             89
Markdown                         1             29              0             44
-------------------------------------------------------------------------------
SUM:                             7             69             25          15006
-------------------------------------------------------------------------------
```

- 参考 https://zhuanlan.zhihu.com/p/492841214
