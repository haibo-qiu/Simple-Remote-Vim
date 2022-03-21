# Simple-Remote-Vim
My own vim configurations for remote coding in Python, heavily based on [vim-for-server](https://github.com/wklken/vim-for-server), are developed by incorporating few practical plugins and better python syntax highlight (```python.vim```). 

## Install
1. Backing up the original ```.vimrc``` 
    ```
    cp ~/.vimrc ~/.vimrc_backup
    ```
2. Using [Vundle](https://github.com/VundleVim/Vundle.vim) to manage vim plugins
    ```
    git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
    ```
3. Cloneing these dotfiles and putting them into right places
    ```
    git clone https://github.com/haibo-qiu/Simple-Remote-Vim
    cp Simple-Remote-Vim/.vimrc ~/.vimrc

    mkdir -p ~/.vim/after/syntax/
    cp Simple-Remote-Vim/python.vim ~/.vim/after/syntax/python.vim
    ```
    Note that ```python.vim``` is to highlight Python function properly.
    ![w_pvim](w_python.vim.png)
    ![wo_pvim](wo_python.vim.png)
4. Launching ```vim``` and running ```:PluginInstall``` to install plugins.

## Plugins
For basic configurations and mappings in ```.vimrc```, please refer to [this blog](https://vimjc.com/vimrc.html) for detailed explanations.

Several adopted plugins are introduced as follows:
1. [vim-syntastic/syntastic:](https://github.com/vim-syntastic/syntastic) make sure flake8 is installed (```pip install flake8```), and ```<F7>``` is for syntax checking. 
2. [tell-k/vim-autopep8:](https://github.com/tell-k/vim-autopep8) autopep8 is required (```pip install autopep8```), and ```<F8>``` is for autopep8 formatting. 
3. [preservim/nerdtree:](https://github.com/preservim/nerdtree) a file system explorer by ```<ctrl-n>```.
4. [preservim/nerdcommenter:](https://github.com/preservim/nerdcommenter) for visual black, ```,cc``` and  ```,cu``` are for commenting and uncommenting quickly.
5. [Xuyuanp/nerdtree-git-plugin:](https://github.com/Xuyuanp/nerdtree-git-plugin) show git status flags for nerdtree file explorer.
6. [vim-airline/vim-airline:](https://github.com/vim-airline/vim-airline) a nice statusline at the bottom of vim window.
7. [vim-airline/vim-airline-themes:](https://github.com/vim-airline/vim-airline-themes) various themes for airline. 
8. [ctrlpvim/ctrlp.vim:](https://github.com/ctrlpvim/ctrlp.vim) a fuzzy file finder with ```,p```.
9. [tpope/vim-fugitive:](https://github.com/tpope/vim-fugitive) use arbitrary Git commands in vim command line, e.g., ```:Git status -s```.
