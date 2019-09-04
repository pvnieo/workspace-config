# Workspace-config

## Install Z-shell

 - Install oh-my-zsh
```
sudo apt-get update
sudo apt upgrade
sudo apt install zsh
sudo apt-get install powerline fonts-powerline
git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```
 - Install powerlevel9k
 ```
 git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
 ```
 - Download and install fonts
 ```
 https://github.com/powerline/fonts/blob/master/SourceCodePro/Source%20Code%20Pro%20for%20Powerline.otf
 https://github.com/Falkor/dotfiles/blob/master/fonts/SourceCodePro%2BPowerline%2BAwesome%2BRegular.ttf
 https://github.com/ryanoasis/nerd-fonts/blob/e9ec3ae4548e59eb9a6531f38370cb99ca591e16/patched-fonts/Meslo/L-DZ/complete/Meslo%20LG%20L%20DZ%20Regular%20Nerd%20Font%20Complete.otf (used)
 
 ```
 - Syntax Highlighting
 ```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git "$HOME/.zsh-syntax-highlighting" --depth 1
echo "source $HOME/.zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> "$HOME/.zshrc"
```
 - zsh-autosuggestion
 ```
 git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
 - zsh-history-substring-search
 ```
  git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
 ```
- change `.zshrc` with the file in this folder
 - install Thefuck
 ```
 sudo apt update
sudo apt install python3-dev python3-pip python3-setuptools
sudo pip3 install thefuck
 ```
 - colorls
 ```
 sudo apt install ruby-full
 sudo gem install colorls
 ```

## Install VSCode and its configuration

 - [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
 - Install Kite: 
 `bash -c "$(wget -q -O - https://linux.kite.com/dls/linux/current)"`
 - Install Firacode & setup:
 `sudo apt install fonts-firacode`
 [https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions](https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions)
 - Extensions: `Dracula / Material themes` - `Material Icons` -  `Bracket Pair Colorizer` - `Code Linting` - `Code Spell Checker` - `Python for VSCode` - `autoDocstring` - `Trailing Spaces` - `GitLens` - `Markdown Preview Enhanced` - `Remote Development` - `Code Runner`

## Install Jupyter and its extensions

 - Install Jupyter
 `pip3 install jupyter`
 - Install Jupyter widgets
 ```
 pip install ipywidgets
jupyter nbextension enable --py widgetsnbextension
```
 - Install Jupyter extensions and enable extensions: `Collapsible Headings`  - `Hinterland` - `Autopep8`
 ```
 pip3 install jupyter_contrib_nbextensions
 jupyter contrib nbextension install --user
 ```
 - Setup Jupyter Theme
 ```
pip3 install jupyterthemes
pip3 install --upgrade jupyterthemes
jt -t grade3 -fs 95 -tfs 11 -nfs 115 -cellw 88% -T -N
 ```
