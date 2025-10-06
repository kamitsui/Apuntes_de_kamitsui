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

## タグ情報

* タグをつけると、基点となるコミットを明確化につながります。
```sh
git tag -a v0.1.0-research-complete -m "Initial design review and research phase finalized. Ready for module implementation."
git push origin --tags # リモートリポジトリにタグもプッシュ
```

* 誤って付けたGitタグはローカルとリモートの両方とも削除する必要がある。
> 1. ローカルのタグを削除
> ```sh
> # タグの一覧を確認する
> git tag
> 
> # ローカルリポジトリからタグを削除する
> git tag -d <タグ名>
> 
> # 例
> git tag -d v1.0.0-mistake
> # Deleted tag 'v1.0.0-mistake' (was 12a34bc)
> ```
> 2. リモートのタグを削除
> ```sh
> # リモートリポジトリからタグを削除する
> git push origin --delete <タグ名>
> ```
> 3. 新しいタグを打ち直す
> > * 新しいコミットにタグを付ける場合
> > ```sh
> > git tag -a <正しいタグ名> -m "正しいメッセージ"
> > ```
> > * 過去のコミットIDにタグを付け直す場合
> > ```sh
> > git tag -a <正しいタグ名> <コミットID> -m "正しいメッセージ"
> > # git tag -a v1.0.0 abc1234 -m "Release v1.0.0"
> > ```
> 4. リモートにプッシュする
> ```sh
> git push origin --tags
> ```
