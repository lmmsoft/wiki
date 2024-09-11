# mac_os_install_x86_python

## 背景
- 背景：工作中有各项目，比较陈旧，需要 python3.6 + 一堆旧版本的依赖 + 我用的是 MacM3 笔记本
- 问题：在arm架构下，使用 pyenv，只能安装 python3.6.15版本，但是numpy/matplotlib/pandas 等依赖无法安装，折腾半天未果
- 结论：经过调研，同事是在 mac M1 的机器上，安装了 x86 的 python3.6.8，然后顺利安装依赖

## 安装过程
- 参考教程《Pyenv Quick Guide: Handling Dual Arch Python (ARM/x86) on Apple Silicon》
- https://or-levi.medium.com/python-management-on-apple-silicon-arm-x86-with-pyenv-f786cf8a48f8

> % pyenv install 3.6.8
Installing at /Users/loumingming/.pyenv/versions/3.6.8_x86
