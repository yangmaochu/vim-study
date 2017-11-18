# vim-instant-markdown

## 安装

第一步：安装instant-markdown-d

```
npm -g install instant-markdown-d
```

第二步：在_.vimrc_中增加插件配置：

```
filetype plugin on
Plugin 'suan/vim-instant-markdown'
```

第三步：配置markdown文件类型的vim加载配置

```
cp ~/.vim/bundle/vim-instant-markdown/after/ftplugin/markdown/instant-markdown.vim ~/.vim/after/ftplugin/markdown/
```

## 配置（.vimrc）

### g:instant\_markdown\_slow

```
let g:instant\_markdown\_slow=?
* ?=0：默认值，实时更新预览页面的内容
* ?=1：在以下三种情况下更新预览页面的内容：
  1. 长时间没有按键输入
  2. 离开插入模式
  3. 保存文件
```

### g:instant\_markdown\_autostart

```
let g:instant\_markdown\_autostart=?
* ?=0：打开Markdown文件时不打开预览页面,手工启动的命令为：:InstantMarkdownPreview
* ?=1：默认值，打开Markdown文件的同时打开预览页面
```

