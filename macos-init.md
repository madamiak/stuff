# MacOS init
```
xcode-select --install
sh -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install --cask google-chrome
brew install --cask iterm2 # run and add permissions, configure hotkey window, set as default profile, set font, turn on natural text editing
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
git clone https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
echo ZSH_THEME="powerlevel10k/powerlevel10k" >> ~/.zshrc
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
echo "plugins=(
    # other plugins...
    zsh-autosuggestions
)" >> ~/.zshrc
brew install svn
brew install --cask homebrew/cask-fonts/font-source-code-pro-for-powerline
echo 'source ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
curl -s "https://get.sdkman.io" | bash
echo source "$HOME/.sdkman/bin/sdkman-init.sh" >> ~/.zshrc
sdk install java
brew install intellij-idea
brew install --cask jetbrains-toolbox
brew install --cask rectangle # run and add permissions
brew install --cask alfred # run and add permissions & configure
brew install nvm
echo "export NVM_DIR="$HOME/.nvm"
    [ -s "$(brew --prefix)/opt/nvm/nvm.sh" ] && . "$(brew --prefix)/opt/nvm/nvm.sh" # This loads nvm
    [ -s "$(brew --prefix)/opt/nvm/etc/bash_completion.d/nvm" ] && . "$(brew --prefix)/opt/nvm/etc/bash_completion.d/nvm" # This loads nvm bash_completion" >> ~/.zshrc
nvm install --lts
# set Keyboard -> (Key Repeat: fast, Delay Until Repeat: short)
# disable cmd+shift+a -> Keyboard -> Shortcuts -> Services -> Search man Page Index in Terminal | https://stackoverflow.com/questions/64551974/best-way-to-fix-no-manual-entry-for-byte-type-a-when-try-to-seek-kotlin-byte
```
