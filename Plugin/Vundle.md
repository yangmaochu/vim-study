# 插件管理：Vundle

利用Vundle可以实现vim插件的统一管理，包含下载、更新等，插件可以来源于GitHub、远程git仓库和本地git仓库。

## 安装

```
>git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

## 配置(.vimrc)

### 不启用插件的初始配置
```
set nocompatible              " 去除VI一致性
filetype off                  " 关闭文件类型检测
set rtp+=~/.vim/bundle/Vundle.vim    " 设置runtime path
call vundle#begin()
Plugin `VundleVim/Vundle.vim`

" 安装插件的命令放在vundle#begin和vundle#end之间

call vundle#end() 
filetype plugin indent on    " 加载vim自带和插件相应的语法和文件类型相关脚本
```

### 增加插件

#### [Github](https://github.com)上的插件

* 格式：Plugin `用户名/插件仓库名`
* 例子：Plugin `tpope/vim-fugitive`

#### [vim-scripts](http://vim-scripts.org/vim/scripts.html)上的插件

* 格式：Plugin `插件名称`
* 例子：Plugin `L9`

#### 由Git支持但不再github上的插件仓库

* 格式：Plugin `git clone 后面的地址`
* 例子：Plugin `git://git.wincent.com/command-t.git`

#### 本地的Git仓库(例如自己的插件)

* 格式：Plugin `file:///+本地插件仓库绝对路径`
* 例子：Plugin `file:///home/gmarik/path/to/plugin`

## 常用命令

命令均是在vim的命令行模式执行：

* :PluginList       - 列出所有已配置的插件
* :PluginInstall     - 安装插件,追加 `!` 用以更新或使用 :PluginUpdate
* :PluginSearch foo - 搜索 foo ; 追加 `!` 清除本地缓存
* :PluginClean      - 清除未使用插件,需要确认; 追加 `!` 自动批准移除未使用插件

