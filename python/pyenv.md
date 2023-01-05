# pyenv
- 官方地址 https://github.com/pyenv/pyenv#installation
- 建议使用 brew install pyenv 安装
- 定期更新，想安装python的话
```
brew upgrade pyenv
```

## 配置自动生效
```
pyenv init

# Load pyenv automatically by appending
# the following to
~/.zprofile (for login shells)
and ~/.zshrc (for interactive shells) :

export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"

# Restart your shell for the changes to take effect.
```

```
For Zsh:

echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```

## 安装新版本

```
pyenv install -l
pyenv install 3.10.4
```

## 选择版本

```
pyenv shell <version> -- select just for current shell session
pyenv local <version> -- automatically select whenever you are in the current directory (or its subdirectories)
pyenv global <version> -- select globally for your user account

pyenv global 3.10.4
```

# pyenv-virtualenv
- 官方文档
  - https://github.com/pyenv/pyenv-virtualenv
- mac安装
```
brew install pyenv-virtualenv
```

- After installation, you'll still need to do Pyenv shell setup steps then add
```
eval "$(pyenv virtualenv-init -)"
```

- 使用
```
# To create a virtualenv for the Python version used with pyenv, run pyenv virtualenv, specifying the Python version you want and the name of the virtualenv directory. For example,
$ pyenv virtualenv 2.7.10 my-virtual-env-2.7.10

Create virtualenv from current version
$ pyenv version
3.4.3 (set by /home/yyuu/.pyenv/version)
$ pyenv virtualenv venv34

pyenv activate <name>
pyenv deactivate

# list all virtualenv
$ pyenv virtualenvs
```
