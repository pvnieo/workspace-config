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
 - Setup Theme
 ```
 vi .zshrc
 ZSH_THEME="agnoster"
 ```
 - Syntax Highlighting
 ```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git "$HOME/.zsh-syntax-highlighting" --depth 1
echo "source $HOME/.zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> "$HOME/.zshrc"
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
jt -t grade3 -fs 95 -tfs 11 -nfs 115 -cellw 88% -T
 ```
