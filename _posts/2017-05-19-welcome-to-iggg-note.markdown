---
layout: post
title:  IGGG Note の使い方
date:   2017-05-19 22:01:14 +0900
tags: introduction
author: matsubara0507
---

# IGGG Note にようこそ！

この記事はこのサイトの部員向けの説明記事です。

## IGGG Note は何に使うべきか

基本的には部内向け、特に初心者向けの(頑張って調べればわかるような)簡単な記事を作成してください。
ただ、部内向けと言っても公開されています。
その点は気を付けて書いてください。

## 記事を書くために必要なこと

IGGG Note は GitHub の[パブリックリポジトリ](https://github.com/IGGG/iggg-note)で管理されているので、GitHub のアカウントが最低限必要です。

GitHub のアカウントを作るには、[公式サイト](https://github.com/)にアクセスして、`Sign Up` 押して必要なことがら(希望のアカウントやメールアドレスなど)を入力すればできるはずです。

## 記事を書く

記事を書くには2つの方法があります。

1. [リポジトリをクローンしてローカル環境で書く方法](#1-リポジトリをクローンしてローカル環境で書く)
2. [GitHub Web UI を使って GitHub の Web サイトから直接書く方法](#2-github-web-ui-を使って-github-の-web-サイトから直接書く)

どのような記事を書くべきかは、[README](https://github.com/IGGG/iggg-note/blob/master/README.md) に少し書いてある。

### 1. リポジトリをクローンしてローカル環境で書く

前者の場合、ある程度 Git が分かる前提で書きます。

1. リポジトリをクローン
    - リポジトリの書き込み権限が無い場合は slack で声をかけるか
    - フォークしてから行う
2. `staging` ブランチから新しくブランチを作成
    - ブランチ名は `post/kiji-no-namae`
3. `/_post/` 以下に記事のマークダウンファイルを作成
    - ファイル名は `YYYY-MM-DD-kiji-no-namae.markdown` にしてください
    - [ヘッダーについて](#ヘッダーについて)は後述するが既にあるマークダウンを参照すればわかるかな
4. 記事を[マークダウン形式](https://guides.github.com/features/mastering-markdown/)で書く
5. 記事が書けたらコミットしてプッシュ
6. プルリクエストを作成する
    - base ブランチは `staging` にすること
7. IGGG部員に見てもらって、誤字などの問題が無ければマージする
8. ステージング環境にアクセスして確認する
    - slack の github-pages チャネルの topic 参照
    - 反映されるには少し時間がかかる
9. 問題が無ければ `master` ブランチへのプルリクを作成
    - 問題があれば 4 に戻る
10. 7.同様に確認してもらったらマージして完成

###  2. GitHub Web UI を使って GitHub の Web サイトから直接書く

少し丁寧に書く

#### 0. リポジトリにアクセスる

[ココ](https://github.com/IGGG/iggg-note)

#### 1. 新しいブランチを作る

ブランチを `staging` にします([ココ](https://github.com/IGGG/iggg-note/tree/staging)にアクセスでもいい)。
そしたら、branch のボタンを押して新しいブランチ名を入力して、新しいブランチを作る。
このとき名前は **`post/kiji-no-namae` のように `post/` 以下にする**。

![](/images/welcome-to-iggg-note/create-branch.jpg)

#### 2. 記事を書く

`/_post` ディレクトリに移動し、`Create new file` をクリックして記事用のファイルを作成する。

![](/images/welcome-to-iggg-note/create-post.jpg)

そしたら、Web エディタが開くので、[マークダウン形式](https://guides.github.com/features/mastering-markdown/)で記事を書く。
このとき、ファイル名は `YYYY-MM-DD-kiji-no-namae.markdown` としてください(拡張子は `.md` でもいいはず)。

![](/images/welcome-to-iggg-note/write-markdown.jpg)

そしたら、このページの下の方に行き、コミットする。

![](/images/welcome-to-iggg-note/commit-new-file.jpg)

ちなみに、コミットした後に編集したい場合は、`_post/` 以下の編集したいファイルをクリックして、鉛筆のマークを押す。
そしたら、前と同じようにエディタが開くので編集する。

![](/images/welcome-to-iggg-note/edit-post.jpg)

既にあるマークダウンを参考にしながら書いてほしい。
[ヘッダーについて](#ヘッダーについて)は後述する。

#### 3. staging にプルリクエストを作る

記事が書けたらプルリクエストを作る。

リポジトリのページの `Pull request` と書かれたタブを押し、右側の `New pull request` を押す。

![](/images/welcome-to-iggg-note/create-pr.jpg)

**ブランチ名に注意してください。**

- `base` ブランチ(左)には `IGGG/iggg-note` の `staging` ブランチ
- `compare` ブランチ(右)には `IGGG/iggg-note` の自分が作成したブランチ

プルリクのタイトルには記事のタイトルでも書いて(正直なんでもいい)、下の `Create pull request` を押す。

そしたら、IGGG部員の何人かに見てもらって、問題が無ければマージします(IGGGの誰かが)。

問題があった場合は、再度編集しなおしてください(プルリクを作る必要は基本的に無い)。

マージされるとステージング環境に反映されます(少し時間がかかる)。
slack の github-pages チャネルの topic 参照するとステージング環境の URL が分かるはずです。

#### 4. master にプルリクエストを作る

ステージング環境に問題が無ければ、今度は `master` ブランチへのプルリクを作る。
ちなみに、問題があったら、3の編集からやり直してください(ファイルを作り直す必要は無いが、プルリクは作り直す)、

プルリクの作り方は 3. と同じである(**ブランチ名だけ気を付けて**)。

問題が無ければ 3. 同様にマージするので、それで完成。

### 3. ちなみに....

このボタンを押すと...

![](/images/welcome-to-iggg-note/new-post-button.jpg)

新しいファイルを作るページに飛ぶ

![](/images/welcome-to-iggg-note/edit-page.jpg)

ので、2-2 を行う。
ただ、**まだブランチを作ってないので**

![](/images/welcome-to-iggg-note/commit-with-branch.jpg)

赤い部分を設定して、ブランチを作ってコミットするようにする。

## ヘッダーについて

以下の形式

```markdown
---
layout: post
title:  IGGG Note の使い方
date:   2017-05-19 22:01:14 +0900
tags: introduction
author: matsubara0507
---
```

- `layout`: 基本的に `post` と書いておいて
    - Jekyll のビルドの設定だから  
- `title`: 記事のタイトル
- `date`: 書いた日付
    - 厳密である必要は無い
- `tags`: 記事のタグ
    - 空白区切りで複数選択できる
- `author`: 記事を書いたひとの GitHub アカウント名

## Q&A

その他、書き方について。
随時、追記していく。

さらに質問があれば slack で聞くか、Issue を立ててください。

### 画像を使うには？？

画像は `/images/` 以下にマークダウンと同じ名前のディレクトリを作って、その中に置いてください。
たとえば、`2017-05-19-kiji-no-namae.markdown` というファイル名で記事を書いた場合には、 `/images/kiji-no-namae/hoge.jpg` という感じに画像を置く。

方法1の場合は普通にコミットすればよい。
が、方法2の場合は、少し手間である。
画像をアップロードすることは可能だが、新しくディレクトリを作ることができない。

なので、どうしても方法2で画像を使いたい場合は、`Create new file` `/images/kiji-no-namae/blank` みたいな一時的なファイルを作成(作成時にファイル名に `/` を含ませるとディレクトリができる)し、それから画像をアップロードする。

アップロードは、`Upload files` というボタンを押せばよい。

## おしまい

みんなつかってくれるといいなぁ。
