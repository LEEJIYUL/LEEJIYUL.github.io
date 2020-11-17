---
layout: post
title: Python 基礎文法のまとめ(1)
image: 7.jpg
date: 2020-11-16 17:12:00 +0200
tags: [Python, coding]
categories: python
---

### Python 基礎文法のまとめ(1)

今日は復習する意味でPythonの基本文法をまとめました。

#### 演算子

> `print(1 +　1) # 2`
>
> `print(3 - 2) # 1`
>
> `print(5 * 2) # 10`
>
> `print(6 / 3) # 2`
>
> `print(2 ** 3) # 2^3 = 8`
>
> `print(5 % 3) # 余り 2 `
>
> `print(5 // 3) # 商は１ `
>
> `print(10 > 3) #True `
>
> `print(4 >= 7) #False `
>
> `print(10 < 3) #False `
>
> `print(5 <= 5) #True `
>
> `print(3 == 3) # 3 = 3 True `
>
> `print(3 + 4 == 7) # True`
>
> `print(1 != 3) # 1は３同じじゃない　！は否定 `
>
> `print((3 > 0) and (3 < 5)) # andは二つともTrueの場合返還 `
>
> `print((3 > 0) % (3 < 5)) # and`
>
> `print((3 > 0) or (3 > 5)) # orはどっちかがTrueの場合返還`
>
> `print((3 > 0) | (3 > 5)) # or`
>
> `print(5 > 4 > 3) # True`
>
> `print(5> 1> 4) # False`
>
> `print(2 + 3 * 3) # 15 `
>
> `print((2 + 4) * 3) # 18 `
>
> `number = 2 + 3 * 4 # 20`
>
> `number = number + 2 # 22`
>
> `number += 2 # 24`
>
> `number *= 2 # 48`
>
> `number -= 2 # 46`
>
> `number /= 2 # 23`
>
> `number %= 5 # 3`

#### 数字処理関数

> `print(abs(-5)) #絶対値 `
>
> `print(pow(4, 2)) # 4^2 = 4*4 = 16 `
>
> `print(max(5, 12)) # 12 maximum `
>
> `print(min(5, 12)) # 5 minimum `
>
> `print(round(3.14)) # 3 四捨五入 `
>
> `print(round(4.99)) # 5 `
>
> `print(floor(4.99)) # 4　上げ  `
>
> `print(ceil(3.14)) # 3 下げ `
>
> `print(sqrt(16)) # 4 平方根 `

#### ランダム関数

> `from random import*`
>
> `print(ramdom()) # 0.0 ~ 1.0 未満のランダム値 `
>
> `print(ramdom() * 10) # 0.0 ~ 10.0 未満のランダム値 `
>
> `print(int(ramdom) * 10) # 0 ~ 10 未満のランダム値 `
>
> `print(int(number() * 10) + 1) # 1 ~ 10 以下ランダム `
>
> `print(int(ramdom() + 45) + 1) # 1 ~ 45 以下 `
>
> `print(randrange(1, 46)) # 1 ~ 46 未満　ランダム値 `
>
> `print(randint(1, 45)) # 1 -45 以下　ランダム値 `

#### String

> `sentence = 'good' と sentence = "good" 同じ`
>
> `sentence = """this is long sentence`
>
> ​						`you do not need to change line and other things`
>
> ​						`just write here`
>
> ​						`"""`

#### Slicing

> `jiyul = "19941209"`
>
> `Print(Jiyul[3]) # 4 4番目要素`
>
> `Print(Jiyul[0:3]) # 199 0 ~ 3の前位置まで呼ぶ`
>
> `Print(jiyul[2:4]) # 94 2 ~ 4 前`
>
> `Print(Jiyul[:6]) #199412 最初 ~ 6 前`
>
> `Print(jiyul[5:]) # 209 5 ~ 最後 まで`
>
> `Print(jiyul[-7:]) # 9941209 逆から　しかし−1から数える`

#### String 処理関数

> `python = "Python is Amazing"`
>
> `Print(python.lower()) # stringを小文字で`
>
> `Print(python.upper()) # 大文字で`
>
> `Print(python[0].isupper()) # Stringの指定位置が大文字か小文字か（python[1].islower()）`
>
> `Print(Len(python)) # string length cheak`
>
> `Print(python.replace("Python", "Java")) # String変更　関数.replace("before", "after")`
>
> `Python.index("n") # nがどこにあるか確認できる`
>
> `Python.index("n", index + 1) 2つ目の　nの場所`
>
> `print(python.find("n")) # indexと同じ機能`
>
> `Print(python.find("Java")) # findでは指定した値がない場合−１がでる`
>
> `Print(python.index("Java")) # indexではエラーが発生して終了される`
>
> `Print(python.count("n")) # countは　関数の中に指定文字がいくつあるかカウンターしてくれる。`

#### String format

##### 方法１%s $d %c

> `Print("i am %d years old" % 2) #  %dを書いて、最後に % 値　を書く`
>
> `Print("i like $s " % "workout") # %sはstringタイプ入れる際`
>
> `Print("Apple start %c latter" % "A") # %cは一文字だけ`
>
> `Print("i like $s color and $s color" % ("red", "blue")) # 二つを入れる時`

しかし %sで全部使える。

##### 方法２ format()

> `print("i am {} years old".format(26)) # formatの値をプレースに入れる`
>
> `print("i like {}color and {}color".format("red", "blue"))`
>
> `print("i like {0}color and {1}color".format("red", "blue")) # 値の場所も指定できる`
>
> `print("i like {1}color and {0}color".format("red", "blue"))`

##### 方法３　pythonv3.6~可能

> `age = 26`
>
> `name = jiyul`
>
> `print(f"I am {name} and {age} years old") # fを前につける`

##### 方法４

> `print("My name is {name} and {age} years old".format(age = 26, name = "jiyul"))`

#### 脱出String

>  `print("good\nbad") #  \n行変更`
>
> `print('i said \\"hello\\" ') #\を前につける　” を文章で使える。`
>
> `Print("Red Apple\rpine") # pine apple \rは次の物を一番前に`
>
> `Print("Red\bbApple") # backspace 一文字削除`
>
> `Print("Red\tApple") # \t はTAP機能改行`
