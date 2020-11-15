---
layout: post
title: Pythonを始める前に！Python開発環境セッティング（１）
image: 6.png
date: 2020-11-15 18:00:00 +0200
tags: [Python, coding]
categories: python
---

こんにちは！、エンジニアとして歩き始めたユルです！

21年4月の正式入社の前にエンジニアインターンを始めてからもう２週間経ちました！

最近は週３で会社でインターンして、残り四日はプログラミングの勉強に時間を尽す日々を送っています。

最初、配置されたチームがサバーサイドの方で、知識がほぼ０なので、学ぶ事に精一杯ですね笑笑

とりあえず、チームに少しでも役に立ちたいので、プロジェクトで主に使っている

##### Python、AWS EC2, Lambda, Docker, JSON 

そして、パソコンの基礎を勉強して行くつもりです。



##### まずはその第一歩はPythonの勉強です！

しかし、基礎文法から勉強してたら、モジュールとパッケージの概念で頭がゴチャゴチャなリました。

そこで一旦Pythonの全体的な概念を理解してから、本格的なコーディング勉強進む事にしました。

雑談が長くなったので、一旦ここで切ります！😬😁

私と同じようにPython初めての方は是非下の方参考してください。

---

### Pythonという言語を理解する為に

私がPythonという言語理解する為にやった事はまずこちら

公式ドキュメンテーションを読んで見た事です。

[Python Documentation](https://docs.python.org/ja/3/library/index.html)

こちらにはPythonの概要はもちろん、基本文法から関数、モジュール、Pythonをどんなプロジェクトに適用するかその方法など全ての情報がありまして、全体的な概念を頭で書く事ができました。自分が興味ある所から読んだら、いいと思います！

[Python guideline](https://www.python.org/dev/peps/pep-0008/)

こちらも！是非

---

### Python開発環境：Visual Studio Code (+仮想環境パッケージ設置）

#### Pythonダウンロード

上記のページでPythonの概念が掴めたら、早速開発環境を整えましょう！

[Python Download](https://www.python.org/downloads/)

<img width="1513" alt="pythonhm" src="https://user-images.githubusercontent.com/49433342/99180848-40fa5c00-276d-11eb-8707-d755f076c05b.png">

このサイトで一番最近バージョンのPythonをダウンロードしてください！

#### VSCodeダウンロード

[VSCodeダウンロード](https://code.visualstudio.com/download)

![VSCodehome](https://user-images.githubusercontent.com/49433342/99180889-a0586c00-276d-11eb-9ce7-ddd4b0a1d58e.jpg)

同じくここで一番最新のVSCodeをダウンロードしてください。

もしどんなコードIDEを使えば良いかと迷っていたら、VSCodeを強くオススメします。個人的にVisual Studioを長い時間開発してきたMS社が作ったエディタなので、使ってみる価値は十分あると思います。

#### VSCodeのShell Command設定

VS Codeを設置後最もオススメする設定はShellで使えるCodeコマンドを設置する事です。Codeコマンドを設置すると、ターミナルで現在フォルダ全体をVS Codeで実行する事がコマンド一つでできます。

[マックターミナルでCodeコマンド使う](https://code.visualstudio.com/docs/setup/mac)

> 1.Vs Codeを実行する
>
> 2.View → Command palete
>
> 3.shell commandを入力して、Install 'code' command in PATHを選択する
>
> 4.現在フォルダをVs Codeで実行 //　code .

ここからが私がこのページを書いた本当の理由です！😂私は最初VSCodeをインストールしてそのまま色んなパッケージを追加して、使ってました。そしたら、パッケージ同士でも不具合で色んな理由不明のエラー😭発生しました。

仮想環境でPythonの開発をするとそういう問題がなくなるのを知ったので、VSCodeを完全削除後再インストールしてこれからの手順で仮想環境を構築しました。（皆さんは私みたいに時間無駄にならないよう最初から仮想環境を使っていきましょう）

仮想環境を作る理由は次の記事で説明するので、是非参考してください

それでは雑談はここまでにします。



