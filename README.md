# dotfiles
My ~~fedora~~ void sway rice.


# Void
## First steps
update system
sudo xbps-install -Su

## Install Packages
sudo xbps install sway wdisplays kanshi emacs kitty neovim flatpak chromium cups cups-browsed foomatic-db foomatic-db-nonfree brother-brlaser system-config-printer ripgrep fd git vscode vlc libreoffice lxappearance foomatic-db-engine thunderbird pipewire wireplumber zsh waybar grimshot blueman find fd gcc curl unzip lutris gimp protonvpn-cli libcupsfilters

## Audio Setup
mkdir -p /etc/pipewire/pipewire.conf.d
sudo ln -svf /usr/share/examples/wireplumber/10-wireplumber.conf /etc/pipewire/pipewire.conf.d/
sudo ln -svf /usr/share/examples/pipewire/20-pipewire-pulse.conf /etc/pipewire/pipewire.conf.d/
sudo ln -svf /usr/share/applications/pipewire.desktop /etc/xdg/autostart

## Printing Setup
sudo ln -s /etc/sv/cupsd /var/service/
sudo reboot

### To add printers 
http://localhost:631/

## Doom Emacs
Launch Emacs with emacsclient -c -a emacs
Delete .emacs.d

git clone --depth 1 https://github.com/doomemacs/doomemacs ~/.config/emacs
~/.config/emacs/bin/doom install

## Lazyvim
mv ~/.config/nvim{,.bak}

git clone https://github.com/LazyVim/starter ~/.config/nvim

rm -rf ~/.config/nvim/.git

## Oh-My-Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

## Nerd Fonts
https://www.nerdfonts.com/

Download what you want.
Unzip in ~/.local/share/fonts

Delete the zip files

## Flatpak
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo

Scroll though and find the ones you need.
