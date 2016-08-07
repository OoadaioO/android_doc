1. 安装git，在github上创建GithubPages创库（bbssyyuui.github.io），clone到本地
2. 安装Ruby环境：RubyInstaller，添加环境变量（D:\Ruby23-x64\bin）
3. 安装和配置jekyll
    a. 添加源镜像（淘宝）
       gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/
       查看源列表： gem sources -l
    b. 安装jekyll
        gem install Jekyll，查看版本：jekyll --version
    c. 安装其他Markdown解析库 
       gem install rdiscount kramdown
    