存放 brew 使用方法和基于 brew的工具使用方法

# brew 安装
## Link
- https://github.com/pyenv/pyenv#installation
- https://brew.sh/

## install 
- /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

## China
- <del>https://zhuanlan.zhihu.com/p/341831809</del>
- https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/ 清华镜像源，自带教程，兼容苹果M1， 非常棒，一次成功！

# brew 工具

## 7z 压缩
To compress a .txt file into .7z format on Mac OS, you can use the 7z command line tool. Here are the steps:

1. Install 7z on Mac. You can install it using Homebrew with the command:
```bash
brew install p7zip
```
2. Open the Terminal app on your Mac.
3. Navigate to the directory containing your a.txt file. You can use cd to change directories:
```bash 
cd /path/to/file
```
4. Run the 7z command to compress a.txt into a.7z:
```bash
7z a a.7z a.txt
```
This will create a compressed a.7z file containing a.txt.

5. To decompress a.7z back into a.txt, run:
```bash 
7z x a.7z
```
This will extract a.txt from a.7z.
So in summary, the two commands you need are:
```bash
7z a filename.7z files_to_compress  # Compress into .7z 
7z x filename.7z  # Decompress .7z file
```
