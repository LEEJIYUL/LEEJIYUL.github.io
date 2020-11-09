---
layout: post
title: Mac-Gem-FilePermissionError
image: 8.jpg
date: 2020-11-10 00:30:20 +0200
tags: [Ruby, github]
categories: Ruby
---

ユルです
今日は自分がgithubブログ立ち上げの時、発生したGem::FilePermissionErrorエラーの時解決方法について投稿します。
それでは早速スタートします。

MacでRubyのパッケージマネジャーであるGemを利用して設置を進む中次のようなエラーに出会いました。
{% highlight ruby %}
    $ gem install bundler
    ERROR: While executing gem ... (Gem::FilePermissionError)
        You don't have write permissions for the /Library/Ruby/Gems/2.3.0 directory.
{% endhighlight %}
結論から言うと、システムがRubyを利用している為、権限がなくGem設置ができなかったという事が分かりました。
sudoを使ってroot権限で実行しても設置が可能だそうですが、セキュリティーの為オススメはしないという資料を見たので、今回はrbenvを利用してエラーを解決しました。

####　問題解決方法
***
まず`brew`を使ってrbenvを設置します。
{% highlight ruby %}
    brew update
    brew install rbenv ruby-bulid
{% endhighlight %}
rbenvが設置できているか確認します。
{% highlight ruby %}
rbenv versions
{% endhighlight %}
私の場合現在Rubyが`system`Rubyを使っていることを分かりました。
{% highlight ruby %}
    *　system (set by /Users/idong-uk/.rbenv/version)
{% endhighlight %}
rbenvで管理されるRubyを設置しなければなりませんでした。
設置可能なRubyバージョンは次のように確認できます。
{% highlight ruby %}
    rbenv istall -l
{% endhighlight %}
次のようにリストが出てきますが、2.7.0ではなく、2.6.4 or 2.6.5で設置する事をオススメします（2.7.0以降のバージョンだと起動しなかったです。）
{% highlight ruby %}
2.6.4
2.6.5
2.7.0
以降省略
{% endhighlight %}
{% highlight ruby %}
rbenv install 2.6.5
{% endhighlight %}
次のようにログが出て設置完了になります。
{% highlight ruby %}
    ruby-build: using openssl from homebrew
    ...
    省略
    ...
    installing ruby-2.6.5...
    installed ruby-2.6.5 to /Users/idong-uk/.rbenv/version/2.6.5
{% endhighlight %}
もう一回rbenvでバージョンを確認します。
{% highlight ruby %}
    rbenv versions
{% endhighlight %}
まだ`system`になっていますが、新しく追加された2.6.5も見えます。
{% highlight ruby %}
    * system
      2.6.5 (set by /Users/idong-uk/Documents/git/leejiyul.github.io/.ruby-version)
{% endhighlight %}
最後に`rbenv　PATH`を追加する為に本人のshell flieを開いて次のコードを追加します。
私は`zsh`を使っているので、`.zshrc`に追加しました。
{% highlight ruby %}
    vim ~/.zshrc
{% endhighlight %}
{% highlight ruby %}
    [[ -d ~/.rbenv  ]] && \
        export PATH=${HOME}/.rbenv/bin:${PATH} && \
        eval "$(rbenv init -)"
{% endhighlight %}
コードを追加したら、`source`でコードを適用させます。
{% highlight ruby %}
    source ~/.zshrc
{% endhighlight %}
そして、再度に`gem install`を実行します。
{% highlight ruby %}
    gem install bundler
{% endhighlight %}
次のように正常に実行できます。
{% highlight ruby %}
    Fetching bundler-2.0.2.gem
    Successfully installed bundler-2.0.2
    parsing documentation for bundelr-2.0.2
    Installing ri documentation for bundler-2.0.2
    Done installing documentation for bundler after 2 seconds
    1gem installed
{% endhighlight %}

以上でGem::FilePermissionErrorエラーが発生した時の解決方法について調べて見ました。
簡単なエラーなので、この通り行うとすぐ解決できると思います。
それでは皆さん楽しいGithubを
