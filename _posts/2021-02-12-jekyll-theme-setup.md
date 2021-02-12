---
layout: post
title:  "Jekyll Theme Setup (Windows)"
subtitle: "Why I start to blog? Why I use Jekyll? What is Jekyll? How to setup Jekyll theme?"
date:   2021-02-12 12:26:46 +0800
modified: 
categories: ""
tags: [Jekyll, Github]
---

## Why I start to blog?

去年2020年對我來說是個思想轉變很大的一年，開始覺得只專注一種程式語言是不夠的，因此產生一個念頭、一個聲音，不斷地出現：**我應該多接觸不同程式語言，找到適合自己的程式語言。**

思考並問自己：
- 過去我在寫Android時，常常感到不足的部分是什麼？
- 最令我害怕、不熟悉的部分是什麼？

答案是網頁相關的部分。

2020年11月我開始學習React.js，從很多人推薦好入門又很新的框架開始歸零學習。學習面對它、接受它、處理它、放下它。每天規律的學習，有一天突然喚起了我初入職場前有的一樣的感覺，就是**我更喜歡邏輯思考與動手實踐過程中的樂趣，所以寫什麼程式我都想嘗試**。

2021年開始覺得寫程式以外，
- 還有什麼值得我去分享、紀錄的體驗或經驗呢？
- 我現在可以做、我能做的第一步是什麼？

答案是紀錄我每一個階段的學習經驗，給未來的自己有個回顧的筆記，或是能夠給迷茫的新手一點點參考那就更好了。
<br><br>


## Why I use Jekyll?

自從著手發想建立自己的個人部落格，我搜尋到**jyt0532分享寫了一年技術文章的心得**，發現他使用的Jekyll主題簡潔明瞭我也很喜歡。

因為想把心力花在分享技術、心得與體驗上，所以當我發現可以用Github架站，加上可以練習網頁語法時，就覺得很適合我這個新手來練習。
<br><br>


## What is Jekyll?

1. Simple
    - 不需要: 資料庫、開發評論、更新版本
    - 只需要關心: 文章內容
2. Static
    - 靜態網頁
    - 提供了Markdown、Liquid、HTML、CSS
3. Blog-aware
    - 提供了Permalinks、categories、pages、posts、custom layouts
<br><br>


## How to setup Jekyll theme?

<p class="message">
  環境: Windows 8.1<br>
  安裝: Ruby+Devkit、RubyGems、Jekyll<br>
  (摸索了很久，因為網路上很多都是MAC的安裝教學)<br>
</p>

### 安裝3步驟

1.<a href="https://rubyinstaller.org/downloads/">Ruby+Devkit</a>
  - 下載選最新的穩定版
  - 接者安裝MSYS2
  - 驗證安裝成功
    `ruby -v` 版本: 2.7.2-1 (x64)

(在Terminal打以下指令)
{% highlight ruby %}
ruby -v
{% endhighlight %}

2.<a href="https://rubygems.org/pages/download">RubyGems</a>
  - 下載ZIP並解壓縮
  - 安裝
    `ruby setup.rb`
  - 更新至最新版
    `gem update --system`
  - 驗證安裝成功
    `gem -v` 版本: 3.2.9

(在Terminal打以下指令)
{% highlight ruby %}
cd rubygems-3.2.9
ruby setup.rb
gem update --system
gem -v
{% endhighlight %}

3.Jekyll和Bundler
  - 使用RubyGems安裝Jekyll
    `gem install`
  - 使用RubyGems安裝Bundler
    `gem install bundler`
  - 驗證安裝成功
    `jekyll -v` 版本: 4.2.0、`bundler -v` 版本: 2.2.9

(在Terminal打以下指令)
{% highlight ruby %}
gem install jekyll bundler
jekyll -v
bundler -v
{% endhighlight %}

### 產生一個新的Jekyll預設部落格

新生成一個myblog的部落格，進入生成的資料夾中，啟動一個開發Server。瀏覽網址: <a href="http://localhost:4000/">http://localhost:4000/</a>

(在Terminal打以下指令)
{% highlight ruby %}
jekyll new myblog
cd myblog
jekyll serve
{% endhighlight %}
<br><br>


## 下一篇
再來分享怎麼套用至主題吧！
<br><br>

## Reference
- 寫技術部落格的啟發文章 (<a href="https://www.jyt0532.com/2017/11/23/why-blog/">jyt0532 寫一年技術文章的心得</a>)
- Jekyll主題 (<a href="https://github.com/poole/hyde">Poole/Hyde</a>)
- Jekyll開始使用(英文/中文) (<a href="https://jekyllrb.com/docs/">Quickstart</a> / <a href="http://jekyllcn.com/docs/quickstart/">快速指南</a>)
- 更多Jekyll主題 (<a href="http://jekyllthemes.org/">Jekyll Themes</a>)
- Windows安裝教學 (<a href="https://reurl.cc/g8Q12b">windows安装jekyll</a>)
- Gem vs Bundle (<a href="https://reurl.cc/dVeA28">Rails — bundle install 和 gem install 的差別</a>)