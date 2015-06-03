+++
categories = []
date = "2015-06-03T20:39:23+09:00"
description = "Pull request と WIP を利用したワークフロー"
keywords = ["Pull request", "WIP"]
title = "Pull request + WIP ワークフロー"
slug = "pull-request-workflow"

+++

Pull request(以下 PR) ベースの開発のススメ

1. タスクを共有するために Issue を作成する
1. `git checkout -b [ブランチ名]` で作業用ブランチを作成する
1. `git commit --allow-empty` で PR 用の空コミットを作成する
1. 作業用ブランチをリモートに Push する
1. ブラウザ上から Push したブランチの PR を作成する
1. 作業用ブランチでコミットする
1. リモートに Push する前にコミットを整理する
`git rebase -i [派生元のブランチ名]` 派生元のブランチ名が master なら `git rebase -i master`
1. リモートのブランチを上書きするので強制 Push
1. __終了/解決/閉じる__ ことができる Issue の番号を PR のコメントに記載する  
Pull request のブランチをマージすると Issue を自動的に close します。  
__マージ先はデフォルトブランチのときだけ自動的に close されます。__  
Issue を close させることができるメッセージは [ヘルプ][help1] に詳細が載っています。

[help1]: https://help.github.com/articles/closing-issues-via-commit-messages/#keywords-for-closing-issues
