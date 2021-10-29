## Install Nvim

mkdir -p $HOME/tools/ && cd $HOME/tools/
wget https://github.com/neovim/neovim/releases/download/nightly/nvim-linux64.tar.gz
tar zxvf nvim-linux64.tar.gz

export PATH=$HOME/tools/nvim-linux64/bin:$PATH

## Configure file

$HOME/.config/nvim/init.vim

## Plugin manager

### install vim-plug

curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

### Edit init.vim

```
call plug#begin('~/.local/share/nvim/plugged')

Plug 'davidhalter/jedi-vim'

call plug#end()
```

所有 plugin install 命令都放在两个 call 之间。

### 使用 vim-plugin

打开 nvim 执行以下命令

- Install plugins	:PluginIntall
- Update plugins	:PluginUpdate
- Remove plugins	:PluginClean

  首先注释掉 init.vim 中的 plugin install 命令，打开 nvim 执行 :PluginClean 来卸载插件

- Check plugin status	:PluginStatus
- Upgrade vim-plug itself	:PluginUpgrade

## 安装依赖

pip install pynvim

pip install jedi

pip install yapf





