From https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/

```
echo "alias config='/usr/bin/git --git-dir=$HOME/.config/ --work-tree=$HOME'" >> $HOME/.bashrc
source ~/.bashrc
echo ".config" >> .gitignore
git clone --bare git@github.com:rohitgr7/dotfiles.git .config/
config checkout
config config --local status.showUntrackedFiles no
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
