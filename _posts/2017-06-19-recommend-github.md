---
layout: post
title: GitHubのすゝめ
date: 2017-06-19 12:00:00 +0900
tags: GitHub introduction
author: matsubara0507
---

# GitHub をはじめよう

**GitHub はいいぞ。**

ということで、GitHub と、ついでに Git について簡単に紹介します。
とはいうものの、一から全部説明してはすごい文量になるので、ある程度(ほとんど)は解説記事へのリンクすることで説明を省きます。

## GitHub is 何 ?

[GitHub](https://github.com/) とは，後述するバージョン管理システム Git のためのホスティング Web サービスである。
自分のソースコード群(リポジトリ)を Web 上にアップロードして、公開・管理などができるようになる。
同種のサービスに、[Bitbucket](https://bitbucket.org/) や [GitLab.com](https://about.gitlab.com/gitlab-com/) がある。

(個人的な意見だが、GitHub はもはやプログラマにとっての名刺代わりになりつつあると思うので、是非アカウントを作って有効活用してほしい。)

### お金は？

Git ではソースコードを含むバージョン管理したいデータ群を **リポジトリ** と言う。
GitHub のようなホスティングサービスでは、リポジトリは外部へ公開するパブリックリポジトリと公開しないプライベートリポジトリの2種類ある。
そして、GitHub の場合は **パブリックリポジトリだけなら無料でいくつでも作ることが出来る**。

- 参照 : [Pricing - Git hosting software and tools](https://github.com/pricing)

プライベートリポジトリを使いたい場合は、月額7ドル(800円弱)払う必要がある。
正直なところ、前述した Bitbucket や GitLab であれば、プライベートリポジトリでさえも無料なため、金銭的にはそれらの方が優れている。
しかし、多くの OSS(オープンソースソフトウェア) が GitHub で管理されており、多くのエンジニアが利用しているため、最低限パブリックリポジトリは GitHub の方がいいだろう。

### 学生であれば...!

2つもアカウント作るのめんどくさいな、と思っても大丈夫！
なんと GitHub には GitHub Education というものが存在し、これに申請することで学生(大学生・大学院生を含む)であればプライベートリポジトリを無料で作れるようになる(他にも特典はある)。

- 参照 : [Learn to Code with GitHub - GitHub Education](https://education.github.com/)

一度申請すると、2年間有効になり、2年後もまだ学生であれば再度申請できる(らしい)。

ちなみに、弊サークルも、コレの組織アカウント版で申請している。

## Git is 何 ?

Git とは([リーナス](https://en.wikipedia.org/wiki/Linus_Torvalds)様)が作った、バージョン管理システムである。
バージョン管理システムとは、名前の通り、ソースコードを含むデータのバージョンを管理するためのプログラムである。

ソースコードや Word のテキストをコピーして前の状態(バージョン)を管理した経験はあるだろうか？
それらの(泥臭い)作業を、うまいこと管理できるようなコマンド群が Git である。

詳しくは以下の資料を参考にすると良い。

- [デザイナのためのGit入門](https://www.slideshare.net/dsuket/git-16343460)
- [こわくない Git](https://www.slideshare.net/kotas/git-15276118)

また、もっと詳しくなりたい場合は 「[実用 Git](https://www.oreilly.co.jp/books/9784873114408/)」とという本を読むと良いだろう。

コマンドをたたくのには慣れて欲しいが、苦手な人はまず [SourceTree](https://ja.atlassian.com/software/sourcetree) という GUI の Git クライアントを使ってみると良いだろう。
少し古いが以下の記事が参考になる。

- [Gitを視覚的に操作できる「SourceTree」のインストール方法](https://nelog.jp/sourcetree)

## GitHub に登録

どうやって GitHub に登録するか。

[ココ](https://github.com/join)からアカウントを作成できる。

よくある Webサービスと同じで、必要なのは email アドレスだけ。
Username は後から変えれない、ユーザーの識別子になる。

直感的な操作でアカウントの作成はできると思うが、不安なら以下を参照してください。

- [GitHubアカウント作成とリポジトリの作成手順 - Qiita](http://qiita.com/kooohei/items/361da3c9dbb6e0c7946b)

ちなみに、ここで email アドレスに大学から支給されてるアドレスを使うと、後述する GitHub Education の申請が多少楽になる。
もちろん、ほんのちょっとの手間でなんとでもなるので、好きなアドレスを使えばよい。

### GitHub Education の申請

以下の記事を参考に進めてください。

- [無料でGitHubのprivateリポジトリを作る方法 - Qiita](http://qiita.com/mtfum/items/d8c06c9a28ce04d3043a)

まぁまぁ古いので齟齬があるかもしれない。

肝になるのは、学生であることの証明。
証明するためには大学から支給されてる email アドレス(`ac.jp` などで終わるやつ)が必要である。
前述したとおり、そのアドレスで GitHub アカウントを登録していれば、特別なことをしなくても良い。
もし、別のアドレスで登録した場合は、[ココ](https://github.com/settings/emails) から大学のアドレスを追加してください。

ちなみに

> 個人アカウントを作成すると5つのprivateリポジトリを作成できるPlanに加入することになり、利用期限は2年間となります。

とあるが、2016/5/11 に料金プランの変更があり、これによってプライベートリポジトリを無制限に作れるようになっている。

- 参照 : [Introducing unlimited private repositories · GitHub](https://github.com/blog/2164-introducing-unlimited-private-repositories)

## 更に詳しく

使い方とかは以下を参考にしてください(丸投げ)。

- [GitHub 入門 - Qiita](http://qiita.com/ay3/items/8d758ebde41d256a32dc)
- [世界一優しいGitHubの使い方入門講座｜TECH::NOTE｜プログラミングをはじめる全ての人に](https://tech-camp.in/note/4938/)

正直、最初っから上記のリンクに飛ばしても良かった(笑)

## おしまい

あと、2段階認証をしといた方がいいと思うよ。
それと、GitHub アカウント作って、Slack に投げてくれれば、弊サークルの組織アカウントのメンバーに招待するよ。
