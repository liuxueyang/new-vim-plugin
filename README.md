## Update on [2017-04-10 Mon 18:28:39]

- disable neocomplete

## Update on [2016-09-15 Thu 07:33]

- remove YouCompleteMe plugin.
- Add neocomplete plugin.

## Update on [2016-09-14 Wed 14:14]

```
git submodule foreach --recursive git pull origin master
```

[YouCompleteme plugin](https://github.com/Valloric/YouCompleteMe)

```
git submodule update --init --recursive
./install.py --clang-completer
```

## Install

- Backup your own configuration. Clone this repository into 
`~/.vim` then start vim.

- run `:PlugInstall`, then wait for a long time to complete
`YouCompleteMe` plugin to finish installation. If your network
is slow, maybe you have to wait longer... Because it has many
dependencies. Or you can disable this plugin at first in the
vimrc

- Then run the following command:

```
    cd ~/.vim/plugged/
    git submodule update --init vim-powerline/
    git submodule update --init vim-instant-markdown/
```

Because maybe the `vim-plug` plugin manager can not install these
two plugins properly.

- To make that vim-instant-markdown plugin working on your 
system. refer to [this] (https://github.com/suan/vim-instant-markdown)

- For Mac OS X, in order to use `bits/stdc++.h` header file. Make
sure you `brew install gcc48`, then in the `~/.vim/plugged/YouCompleteMe/third_party/ycmd/cpp/ycm/.ycm_extra_conf.py`
file, add these three lines:

```python
'-I/usr/local/include/c++/4.8.5/x86_64-apple-darwin15.2.0/',
'-I/usr/local/Cellar/gcc48/4.8.5/include/c++/4.8.5/x86_64-apple-darwin15.2.0/',
'-I/usr/local/Cellar/gcc/5.3.0/include/c++/5.3.0/x86_64-apple-darwin15.0.0/',
```

to the `flags` array variable. Then plugin `YouCompleteMe` will not 
show error for the `bits/stdc++.h` header file. *However*, on Linux
systems, you don't have to. ;-)

### ScreenShot
![Gvim](./gvim.png)

![mvim](./mvim.png)

Enjoy. ;-)

