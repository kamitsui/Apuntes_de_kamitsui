# Git

## グローバルユーザー設定
```sh
git config --global --list
user.name=intra_name
user.email=intra_name@xxxx.yy.zz
```
> 例えば、42 Tokyo の課題しか開発プロジェクトをしていないケース。
> この場合は、42で使っている情報をグローバルユーザー設定するだけでＯＫ。

## プロジェクト専用のローカルユーザー設定
```sh
cd /path/to/your/company/project
git config user.name "Your Company Name"
git config user.email "your.company.email@example.com"
```
> 会社のプロジェクトを開発するケース。
> ちゃんと、所属会社で使っているメールやユーザー名をローカルユーザーに設定する。

> [!note]
> プロジェクト毎によって、ユーザー情報を使い分けてGitのログを残すことができる。
