# Ubuntu 22.04 (Jammy Jellyfish)をベースイメージとして使用
FROM ubuntu:22.04

# 環境変数を設定して、apt-get実行時の対話型プロンプトを抑制
ENV DEBIAN_FRONTEND=noninteractive

# 必要なパッケージをインストール
# ここにインストールしたいGUIアプリケーションを追加してください
RUN apt-get update && apt-get install -y --no-install-recommends \
    xfce4-terminal \
    # その他必要なツール (例: git, curl, build-essentialなど)
    git \
    curl \
    build-essential \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# DEBIAN_FRONTENDをリセット
ENV DEBIAN_FRONTEND=dialog
