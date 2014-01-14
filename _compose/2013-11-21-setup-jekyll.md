## 简介


## 搭建环境（Windows）

### 安装Ruby

Jekyll是[Ruby](https://www.ruby-lang.org/en/)程序，需要安装Ruby，Ruby官网上建议Windows环境安装RubyInstaller

> If you’re on Windows, there’s a great project to help you install Ruby: [RubyInstaller](http://rubyinstaller.org/). It gives you everything you need to set up a full Ruby development environment on Windows.

在RubyInstaller的下载页面有很多版本的下载链接，如果不知道下载那个版本（x64和x86系统有分别的安装包），参考如下建议：

> If you don’t know what version to install and you’re getting started with Ruby, we recommend you use Ruby 1.9.3 installers. These provide a stable language and a extensive list of packages (gems) that are compatible and updated.

下载好 `rubyinstaller-1.9.3-p448.exe` 直接进行安装。

### 安装DevKit

> The DevKit is a toolkit that makes it easy to build and use native C/C++ extensions such as RDiscount and RedCloth for Ruby on Windows.

官网有说：

> Ruby 1.8.6 to 1.9.3: tdm-32-4.5.2

之前我们下载的RubyInstaller是1.9.3版本的，所以在这就下载4.5.2版本的[DevKit][^DevKit_4.5.2_Downlaod]，DevKit是个自解压包，解压后在解压的目录打开CMD，并执行已下安装命令


`ruby dk.rb init`
`ruby dk.rb install`

### Ruby初始配置


#### 设置gem的更新源

设置
`gem sources --remove http://rubygems.org/`
`gem sources -a http://ruby.taobao.org/`
查看是否正确
`gem sources -l`


#### 安装rdoc和bundler

rdoc是：
bundler是：

// 持续时间可能较久


## 安装Jekyll

// 持续时间可能较久

## 安装Python
//


## 创建Jekyll博客






## 参考链接
<a href="http://sinosmond.github.io/blog/2012/03/12/install-and-deploy-octopress-to-github-on-windows7-from-scratch/" target="_blank">在 Windows7 下从头开始安装部署 Octopress</a>




[^^DevKit_4.5.2_Downlaod]: https://github.com/downloads/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe