---
title:        "install jekyll"
description:  "ubuntu jekyll 安装"
image:        "http://placehold.it/400x200"
author:       "Merafour"
---

最直接的方法就是运行快速指南中的命令：
~~~
gem install jekyll
~~~
这个时候会提示：
~~~
Command 'gem' not found, but can be installed with:
sudo apt install ruby
~~~
按照提示安装ruby，我习惯上会使用 apt-get:
~~~
sudo apt-get install ruby -y
~~~
安装完了之后在运行命令 "sudo gem install jekyll"。
但是我发现运行改名了出错了，
~~~
Building native extensions. This could take a while...
ERROR:  Error installing jekyll:
        ERROR: Failed to build gem native extension.

    current directory: /var/lib/gems/2.5.0/gems/http_parser.rb-0.6.0/ext/ruby_http_parser
/usr/bin/ruby2.5 -r ./siteconf20190130-2958-1gptzf5.rb extconf.rb
mkmf.rb can't find header files for ruby at /usr/lib/ruby/include/ruby.h
~~~
所以我就直接运行 jekyll，结果提示：
~~~
Command 'jekyll' not found, but can be installed with:
sudo apt install jekyll
~~~
到这里我发现居然可以直接安装。
然后运行 "jekyll -v"输出："jekyll 3.1.6"说明安装成功。

参考：https://www.jekyll.com.cn/docs/quickstart/
