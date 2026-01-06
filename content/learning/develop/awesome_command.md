## AI CLI tools

### Git コミットメッセージの提案

````
現在のリポジトリにADDした内容をGitコミットするためのメッセージを提案してください。
シンプルな英語で Conventional Commits の仕様に沿ってください。
コミットメッセージの構成はこちら
```
[要約のタイトル (50文字以内)]

[詳細な説明をここに記述します。1行目との間に空白行を設けます。本文の各行も72文字以内が目安です。]
```
````
<details>
<summary>変更内容の全てを対象にしたい時</summary>
````
現在のリポジトリの変更内容をGitコミットするためのメッセージを提案してください。
シンプルな英語で Conventional Commits の仕様に沿ってください。
コミットメッセージの構成はこちら
```
[要約のタイトル (50文字以内)]

[詳細な説明をここに記述します。1行目との間に空白行を設けます。本文の各行も72文字以内が目安です。]
```
````
</details>


## docker

### doker 一時的にコンテナを動かしたい時。（終了後はコンテナ削除）
```sh
docker run --rm --name exam -it -v $(pwd):/app node20-slim /bin/bash
```
<details>
<summary>説明</summary>

`docker run --rm --name <container> -it -v <host_dir>:<container_dir> <image_name>`

`node-slim`は`Debian:slim`がベースのOSイメージ

`-v`:ホストディレクトリをコンテナにマウントできる。
</details>

## ディスク使用量の確認方法

### `du` コマンド

```sh
# ホームディレクトリ内の容量を消費しているディレクトリの一覧（大きいサイズ順 25個）
du -h ~ 2>/dev/null | sort -hr | head -25
# 階層の深さを１つ
du -h -d 1 ~ 2>/dev/null | sort -hr
```

### `find` コマンド

```sh
# ホームディレクトリ以下で 100MB 以上のファイルを探す
find ~ -type f -size +100M -exec ls -lh {} + 2>/dev/null | sort -k 5 -hr | head -20
```

## 画像・動画

### `ffmpeg` コマンド
```sh
# 品質を75%に設定してWebP化
ffmpeg -i input.png -compression_level 6 -q:v 75 output.webp
```
<details>
<summary>説明</summary>

WebPへの変換: PNGと同じく透明度を保持でき、かつJPEGより高効率な圧縮が可能です。

使用ケース: Webページの画像ファイルとして使う

サイズの調整: まだ大きい場合は、`scale=1000:-1` などでリサイズを追加してください。（アスペクト比を維持して横幅1000ピクセルにリサイズ）

メタデータの削除: `-map_metadata -1` を追加すると、カメラ情報などの余計なデータを削除して数KB節約できます。
</details>
