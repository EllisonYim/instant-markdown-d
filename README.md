!nstant-markdown-d
================
> 由于原 repo 作者已经没有 merge 和维护了，所以暂时 fork 在自己的 repo 中, 欢迎 contribute。

New Feature
-----------
* GFM 更新了最新的样式
* 优化了一下 markdown-it 关于 <> 的问题
* 支持 yaml 字段解析
* 优化项目本身的 css
* 让 chrome 单独打开固定窗口大小

Installation
------------

Install instant-markdown-d server
```
git clone https://github.com/yantze/instant-markdown-d ~/.local/instant-markdown-d
ln -s ~/.local/instant-markdown-d ~/.bin/instant-markdown-d
```

Install instant-markdown-d vim plugin by Vim Plugin Manager
```
Plug 'suan/vim-instant-markdown'
```

Start to preview md file, run command in vim
```
:InstantMarkdownPreview
```

By default, `port` is 8090

Run with Command
----------------
```
# listen 8090 port
instant-markdown-d

# display content
cat README.md| curl -X PUT -T - http://localhost:8090
echo "## Hlo > abc" | curl -X PUT -T - http://localhost:8090

# close the web page
curl -X DELETE http://localhost:8090
```

Environment variables
---------------------

* `INSTANT_MARKDOWN_OPEN_TO_THE_WORLD=1` - by default, listening `0.0.0.0:8090`

* `INSTANT_MARKDOWN_ALLOW_UNSAFE_CONTENT=1` - by default, scripts are blocked.


* `INSTANT_MARKDOWN_BLOCK_EXTERNAL=1` - by default, external resources such as
  images, stylesheets, frames and plugins are *allowed*.
