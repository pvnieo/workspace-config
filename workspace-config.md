# Workspace-config

## Install Z-shell

 - install Terminator
 ```
 sudo add-apt-repository ppa:gnome-terminator
 sudo apt-get update
 sudo apt-get install terminator
 ```
 - install terminator-themes (molokai)
 ```
 sudo apt install python-requests
 mkdir -p $HOME/.config/terminator/plugins
 wget https://git.io/v5Zww -O $HOME"/.config/terminator/plugins/terminator-themes.py"
 activate plugin from settings
 ```
 - copy on selection + no titlebar (profiles/general)
 - scrollback 5000 - diseble scrollbar (profiles/scrolling)
 - reuse profil + font (global)
 - in layout make sure windows use default

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
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
 - zsh-autosuggestion
 ```
 git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
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
 - fzf history search
 ```
 git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
 ```
  - change `.zshrc` with the file in this folder
  - run this command
  ```
  zsh
chsh -s $(which zsh)
```
  - configure internal terminal at vscode
  ```
git clone https://github.com/ryanoasis/nerd-fonts.git --depth 1
cd nerd-fonts
sudo ./install.sh
  ```
then add this to `settings.json`:
```json
    "files.autoSave": "afterDelay",
    "workbench.colorTheme": "Dracula",
    "workbench.iconTheme": "material-icon-theme",
    "editor.fontFamily": "Fira Code",
    "editor.fontLigatures": true,
    "terminal.integrated.shell.linux": "/bin/zsh",
    "terminal.integrated.shell.osx": "/bin/zsh",
    "terminal.integrated.fontFamily": "MesloLGLDZ Nerd Font",
    "python.testing.pytestEnabled": true,
    "python.pythonPath": "/usr/bin/python3.8",
    "kite.showWelcomeNotificationOnStartup": false,
    "python.linting.pylintArgs": [
        "--extension-pkg-whitelist=cv2",
        "--max-line-length=130",
        "--ignore=E24,W503,E203",
    ],
    "python.linting.flake8Args": [
        "--max-line-length=130",
        "--ignore=E24,W503,E203",
    ],
    "python.formatting.provider": "black",
    "python.linting.flake8Enabled": true,
    "python.linting.mypyEnabled": true,
```
## Install VSCode and its configuration

 - [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
 - Install Kite: 
 `bash -c "$(wget -q -O - https://linux.kite.com/dls/linux/current)"`
 - Install Firacode & setup:
 `sudo apt install fonts-firacode`
 [https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions](https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions)
 - Extensions: `Dracula / Material themes` - `Material Icons` -  `Bracket Pair Colorizer` - `Code Linting` - `Code Spell Checker` - `Python for VSCode` - `autoDocstring` - `Trailing Spaces` - `GitLens` - `Markdown Preview Enhanced` - `Remote Development` - `Code Runner` - `Git File History` - `Peacock` - enable `pytest` - `Python Test Explorer for Visual Studio Code`

## Install Jupyter and its extensions

 - Install Jupyter
 `pip3 install jupyter`
 - Install Jupyter widgets
 ```
 pip install ipywidgets
jupyter nbextension enable --py widgetsnbextension
```
 - Install Jupyter extensions and enable extensions: `Collapsible Headings`  - `Hinterland` - `Autopep8` - `Code Prettify`
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
 
 ## Configure i3
  - copy folders: flags - i3 - styles (with typeface) and  i3xrocks to `~/.config/regolith`
  - change fonts icon of workspace and i3xrocks in `styles/i3-wm`
  - change fonts in `styles/typeface`
  - add i3xrocks in `styles/i3xrocks`
  - add new font to `~/.config/regolith/Xresources`
  - add `back-forth` and startup actions to `i3/config`
  - add new files (i3-wm - typeface - theme- i3xrocks) to `~/.Xresources-regolith`
