#!/bin/bash
# Simple setup.sh for configuring Ubuntu 14.04.2 LTS EC2 instance

# Ubuntu系统下安装ruby必要的库和编译环境
sudo apt-get update
sudo apt-get install -y build-essential openssl curl libcurl3-dev libreadline6 libreadline6-dev git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libxml2-dev libxslt-dev autoconf automake libtool imagemagick libmagickwand-dev libpcre3-dev libsqlite3-dev

# rbenv环境安装
git clone git://github.com/sstephenson/rbenv.git ~/.rbenv

## 插件：用来编译安装 ruby
git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build

## 插件：通过 gem 命令安装完 gem 后无需手动输入 rbenv rehash 命令
git clone git://github.com/sstephenson/rbenv-gem-rehash.git ~/.rbenv/plugins/rbenv-gem-rehash

## 插件：通过 rbenv update 命令来更新 rbenv 以及所有插件
git clone https://github.com/rkh/rbenv-update.git ~/.rbenv/plugins/rbenv-update

## 环境变量
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
source ~/.bashrc
type rbenv

## ruby环境安装，首先列出可安装的版本，然后选择后进行下载编译
# rbenv install -l
rbenv install 2.1.5

## 设置当前使用的ruby版本
rbenv global 2.1.5
rbenv rehash

## 修改gem源，提高下载速度
# gem sources --remove https://rubygems.org/
# gem sources -a http://ruby.taobao.org/
#####rbenv 环境安装结束，gems的安装，使用工程下的bundle install#######

# 安装Nginx服务器
sudo apt-get install nginx

# 安装memcached
sudo apt-get install memcached
