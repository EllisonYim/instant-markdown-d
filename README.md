!nstant-markdown-d
================

New Feature
-----------

* Updated the latest styles
* Updated the markdown-it parse `<>` problem
* Remove meta header
* Updated css in index.html
* Popup a simple chrome window to display markdown on macOS


Installation
------------

Install another-instant-markdown-d
```sh
npm install -g another-instant-markdown-d
```

Install instant-markdown-d vim plugin by Vim Plugin Manager
```
Plug 'suan/vim-instant-markdown'
```

Start to preview md file, run command in vim
```
:InstantMarkdownPreview
```

Or use a map:
```
map <leader>rp :InstantMarkdownPreview<CR>
```

Run with Command
----------------
```sh
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
