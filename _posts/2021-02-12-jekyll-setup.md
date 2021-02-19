---
layout: post
title:  "Windows Jekyll 安裝設定"
subtitle: "什麼是Jekyll？
          如何設定？
          安裝步驟？
          如何建立一個預設部落格？"
date:   2021-02-12 12:26:46 +0800
modified: 
categories: "部落格"
tags: [Jekyll, Github]
---

# Outline
- [What is Jekyll?](#what-is-jekyll)
- [How to setup Jekyll theme?](#how-to-setup-jekyll-theme)
  - [安裝3步驟](#安裝3步驟)
  - [產生一個預設部落格](#產生一個預設部落格)
- [下一篇](#下一篇)
- [Reference](#Reference)
<br><br>
<br><br>

## What is Jekyll?

- Jekyll是一個將文字轉換成靜態部落格網站的工具。
- 可以跟Github Pages連結在一起。

Jekyll特性:
1. Simple
    - 不需要: 資料庫、開發評論、更新版本
    - 只需要關心: 文章內容
2. Static
    - 靜態網頁
    - 使用Liquid模板式語言
    - 內建Markdown、HTML、CSS
3. Blog-aware
    - 提供部落格所需的Permalinks、categories、pages、posts、custom layouts
<br><br>


## How to setup Jekyll theme?

<p class="message">
  環境: Windows 8.1<br>
  安裝: Ruby+Devkit、RubyGems、Jekyll<br>
  (摸索了很久，因為網路上很多都是MAC的安裝教學)<br>
</p>

### 安裝3步驟
  **SOP: 先閱讀步驟與指令介紹，可直接複製指令區的指令(Windows)，最後查看Terminal中畫面截圖**

1.<a href="https://rubyinstaller.org/downloads/">Ruby+Devkit</a>
  - 下載選最新的穩定版
  - 接者安裝MSYS2
  - 驗證安裝成功
    `ruby -v` 版本: 2.7.2-1 (x64)

![ruby installer for windows](/assets/images/jekyll-setup-ruby-installer-for-windows.jpg)

(在Terminal打以下指令)
{% highlight ruby %}
ruby -v
{% endhighlight %}

(畫面截圖)
  - 驗證Ruby版本號
![ruby version verify](/assets/images/jekyll-setup-ruby-ver.jpg)


2.<a href="https://rubygems.org/pages/download">RubyGems</a>
  - 下載ZIP並解壓縮
  - 進入解壓縮檔的目錄下，安裝RubyGems
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

(畫面截圖)
  - 開始安裝
![ruby gems install start](/assets/images/jekyll-setup-rubygems-install-start.jpg)
  - 安裝成功，版本: 3.2.9 (2021-02-08)
![ruby gems install success](/assets/images/jekyll-setup-rubygems-install-done.jpg)
  - 更新至最新版，版本: 3.2.10 (2021-02-15)
![ruby gems update version](/assets/images/jekyll-setup-rubygems-update.jpg)
  - 驗證RubyGems版本號
![ruby gems version verify](/assets/images/jekyll-setup-rubygems-ver.jpg)


3.Jekyll和Bundler
  - 使用RubyGems安裝Jekyll
    `gem install`
  - 使用RubyGems安裝Bundler
    `gem install bundler`
  - 驗證安裝成功
    `jekyll -v` 版本: 4.2.0、`bundler -v` 版本: 2.2.10

(在Terminal打以下指令)
{% highlight ruby %}
gem install jekyll bundler
jekyll -v
bundler -v
{% endhighlight %}

(畫面截圖)
  - 同時安裝Jekyll和Bundler，再驗證兩者的版本號
![ruby gems version verify](/assets/images/jekyll-setup-jekyll-and-bundler-install.jpg)


### 產生一個預設部落格

- 新生成一個myblog的部落格，進入生成的資料夾中，啟動一個開發Server。
- 瀏覽網址: <a href="http://localhost:4000/">http://localhost:4000/</a>

(在Terminal打以下指令)
{% highlight ruby %}
jekyll new myblog
cd myblog
jekyll serve
{% endhighlight %}

(畫面截圖)
  - 產生部落格
![jekyll new blog](/assets/images/jekyll-setup-jekyll-myblog-new.jpg)
  - 啟動開發中Local端的Server
![jekyll new blog](/assets/images/jekyll-setup-jekyll-myblog-serve.jpg)
  - 瀏覽Local端的Server
![jekyll default posts page](/assets/images/jekyll-setup-jekyll-default-blog-posts.jpg)
![jekyll default about page](/assets/images/jekyll-setup-jekyll-default-blog-about.jpg)

## 下一篇
再來分享怎麼套用至主題吧！
<br><br>

## Reference
- <a href="https://docs.shopify.com/themes/liquid-basics">Liquid</a>
- <a herf="https://daringfireball.net/projects/markdown/">Markdown</a>
- <a href="https://jekyllrb.com/docs/">Quickstart 英文</a> / <a href="http://jekyllcn.com/docs/quickstart/">快速指南 中文</a>
- <a href="http://jekyllthemes.org/">Jekyll Themes</a>
- <a href="https://reurl.cc/g8Q12b">windows安装jekyll</a>
- <a href="https://reurl.cc/dVeA28">Rails — bundle install 和 gem install 的差別</a>