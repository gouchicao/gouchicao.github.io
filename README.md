# 狗吃草 AI＋
> 提供基于人工智能的基础工具和实践指南

## 站点搭建
* 安装软件
```bash
brew install ruby
gem install jekyll bundler
```

* 建站
```bash
jekyll new gouchicao.github.io
cd gouchicao.github.io
bundle install
```

* 编辑配置文件
```bash
nano Gemfile
```
```
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
```

* 运行
```bash
bundle exec jekyll serve
```
[http://127.0.0.1:4000/](http://127.0.0.1:4000/)

## 参考资料
[将纯文本转换为静态博客网站](http://jekyllcn.com)
[jekyll](https://github.com/jekyll/jekyll)
