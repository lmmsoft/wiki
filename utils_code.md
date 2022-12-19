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

## 更多代码行数工具
- https://zhuanlan.zhihu.com/p/259663572
- Statistic IDEA 插件
- cloc
- 依赖 git 仓库的 gitstats, 有很详细的各种维度的统计图表📈，很牛逼
- 杠精工具之 find 命令
```
find . -name "*.java" -or -name "*.xml" -print | xargs wc -l
```

# 统计markdown里有多少字的工具
- https://github.com/spencerwooo/cwim
用法
1. 下载工具
2. rename to cwim
3. move to /usr/bin 失败，root用户也不行，于是移到 ~/目录
4. 运行 ```lmm333@mingmingdeMacBook-Pro 晨间日记_backup % ~/cwim .```

样例输出：
```
 2022-08/22-08-04 周四 第100篇晨间日记.md                         | 72        | 45          | 727    | 2 mins
 话题集锦.md                                                      | 122       | 83          | 397    | 1 mins
 SUM                                                              | 13685     | 8846        | 120301 | 481 mins
------------------------------------------------------------------+-----------+-------------+--------+--------------
```
