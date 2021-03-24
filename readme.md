# devcontainer-atcoder

VSCodeの拡張機能 [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
で簡単にAtCoder用の環境構築ができます。  
C++環境構築が難しい or めんどくさい人用

## セットアップ

### Visual Studio Code インストール

<https://code.visualstudio.com/> からVisual Studio Codeをインストールしてください。

### Remote - Containers インストール

TODO 画像用意

1. Visual Studio Codeの拡張機能タブをクリック  
2. [Remote - Containers]("https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers")をインストール

### Dockerインストール

[Install Docker Engine](https://docs.docker.com/engine/install/)

#### CentOS, Debian, Fedora, Raspbian, Ubuntuの場合

```bash
# Docker インストール
$ curl -fsSL https://get.docker.com -o get-docker.sh
$ sudo sh get-docker.sh
# sudoなしでも使えるようにdockerグループにユーザー追加
$ sudo sudo usermod -aG docker $USER
```

再起動する

```bash
# 正しくインストールされているか確認
$ docker run hello-world
```

#### Windowsの場合

<https://hub.docker.com/editions/community/docker-ce-desktop-windows/> からDocker Desktop for Windowsをインストールしてください。

#### Macの場合

<https://hub.docker.com/editions/community/docker-ce-desktop-mac/> から Docker Desktop for Macをインストールしてください。

### Download ZIP

TODO 画像用意

1. Codeをクリック
2. Download ZIPをクリック
3. 適当な場所に解凍

### コンテナに入る

TODO 画像用意

1. 右下をクリック
2. Remote-Containers: Open Folder in Container を選択
3. 解凍したフォルダを選択

## 使い方

### 実行 (Shift+F5)

1. コマンドパレットを開く(Ctrl+Shift+P)
2. CMake: Run Without Debugging(デバッグなしで実行)を選択

### expander.py

expander.pyを使用して、AtCoder以外のオンラインジャッジに提出できるコードを生成できます。

1. コマンドパレットを開く(Ctrl+Shift+P)
2. Tasks: Run Task(タスクの実行)を選択
3. expander.pyを選択

よく使うのでショートカットキーを登録すると吉

## 最後に

環境構築苦労してる人向けに作ったけど、Dockerできる人なら環境構築苦労しない気がする...
