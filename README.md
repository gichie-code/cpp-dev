# C++ 開発環境（Docker 利用）

このディレクトリは、Docker を用いた C++ 開発環境です。ローカルの `src/` ディレクトリで開発を行い、コンパイルや実行はコンテナ上で行います。

## 構成

- `Dockerfile`: 開発用の C++ コンテナを定義
- `docker-compose.yml`: コンテナを簡単に起動するための構成ファイル
- `src/`: 開発用のソースコードディレクトリ
- `.dockerignore`: Docker ビルド時に無視するファイル
- `.gitignore`: Git にコミットしないファイルを指定

## 使用方法

### ビルド

```bash
docker compose build
```

### コンパイルと実行

```bash
docker compose run --rm cpp-dev sh -c "g++ src/main.cpp -o main && ./main"
```

## ライセンス

MIT License
