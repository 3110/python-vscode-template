# Visual Studio Code 用 Python 開発環境

Windows 11 環境で [VS Code](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)，[Git for Windows](https://gitforwindows.org/)，[pyenv](https://github.com/pyenv-win/pyenv-win)，[pipenv](https://github.com/pypa/pipenv)，[flake8](https://github.com/pycqa/flake8)，[black](https://github.com/psf/black)を使用することを想定しています。

## 準備

### `pyenv`のインストール

[pyenv for Windows](https://github.com/pyenv-win/pyenv-win)をインストールします。

```bash
git clone https://github.com/pyenv-win/pyenv-win.git "$HOME/.pyenv"
```

環境変数`PYENV`，`PYENV_HOME`，`PYENV_ROOT`を設定します。環境変数`PATH`にもパスを追加します。

```bash
export PYENV=$HOME/.pyenv/pyenv-win
export PYENV_HOME=$PYENV
export PYENV_ROOT=$PYENV
export PATH=$PYENV/bin:$PYENV/shims:$PATH
```

### `pipenv`のインストール

```bash
pip install pipenv
```

環境変数`PIPENV_VENV_IN_PROJECT`を`true`に設定する。

```bash
export PIPENV_VENV_IN_PROJECT=true
```

## 開発環境の構築

`flake8`と`black`を使用する設定になっています。

```bash
git clone git@github.com:3110/python-vscode-template.git sample
cd sample
pipenv install -d
```
