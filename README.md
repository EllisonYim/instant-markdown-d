!nstant-markdown-d
================
instant-markdown-d is a small Node.js server that enables instant compilation and previewing of Markup files. A plugin can easily be written for any text editor to interface with it. One currently exists for Vim: https://github.com/suan/vim-instant-markdown

Installation
------------
- `git clone https://github.com/yantze/instant-markdown-d /path/to/dir`
- `ln -s /path/to/dir/instant-markdown-d /usr/local/bin/`

REST API
--------
| Action           | HTTP Method | Request URL               | Request Body |
|---------------------|-------------|---------------------------|--------------------|
| Refresh Markdown on page | PUT        | http://localhost:\<port\> | \<New Markdown file contents\> |
| Close Webpage    | DELETE      | http://localhost:\<port\> | |
By default, `<port>` is 8090

Environment variables
---------------------

* `INSTANT_MARKDOWN_OPEN_TO_THE_WORLD=1` - by default, listening `0.0.0.0:8090`

* `INSTANT_MARKDOWN_ALLOW_UNSAFE_CONTENT=1` - by default, scripts are blocked.
  Use this preference to allow scripts.

* `INSTANT_MARKDOWN_BLOCK_EXTERNAL=1` - by default, external resources such as
  images, stylesheets, frames and plugins are *allowed*. Use this setting to
  *block* such external content.
