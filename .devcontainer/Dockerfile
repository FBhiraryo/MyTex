# Codespacesのベースイメージとして、Universal Image を使用
FROM mcr.microsoft.com/devcontainers/universal:latest

# TeX Live のフルバージョンと latexmk をインストールする
# texlive-full は非常に容量が大きいですが、日本語環境のパッケージ不足を防ぐために使用します。
RUN sudo apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && sudo apt-get -y install --no-install-recommends \
        # TeX Live のパッケージをここで指定
        texlive-full \
        latexmk \
    && sudo apt-get clean \
    && sudo rm -rf /var/lib/apt/lists/*