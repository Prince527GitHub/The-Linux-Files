# Steam Deck

## Linux

### Decky
Decky Loader is a plugin loader for Steam Big Picture mode.
It only works on SteamOS and Bazzite.

It's very Useful for adding functions to steam.
Follow the guide on [Decky's Github](https://github.com/SteamDeckHomebrew/decky-loader) to install it.

#### Plugins
- Volume Mixer: Change the volume of apps
- Bluetooth: Quick connect for bluetooth
- Controller Tools: A controller menu
- TunnelDeck: Quick connect for VPNs
- System Toolbox: Settings for tweaking the deck
- ProtonDB Badges: Compatibility badges from [ProtonDB](https://www.protondb.com/) 
- SteamGridDB: Add art to games easily
- TabMaster: Hide tabs in the libary menu *(I hide "Great On Deck" and "Soundtracks")*
- CSS Loader: Modify the theme of Steam *(some may not exist)*
	- Custom Collection Layout
	- Deck  Store - Rounded
	- DeckyDownloadBar
	- DellyVolume
	- Desktop Rounded Games
	- Ducky's Wallpapers
	- No Game Count
	- No Game Shine
	- Round
	- Rounded Keyboard
	- Switch Like Home

### Distrobox
Distrobox is a tool to run linux containers which can allow you to install packages without modifying the read only system. 
It is preinstalled on SteamOS and Bazzite.

#### Urn
I've started getting into speedrunning and needed a timer so I use [Urn](https://github.com/paoloose/urn)
I tried installing it with fleek on Bazzite but no luck, so I use a distrobox.

First setup an archlinux distrobox:
```
distrobox create --name arch --image archlinux
distrobox enter arch
```

Now in the container we will setup [ame](https://getcryst.al/site/docs/amethyst/getting-started) *(an aur helper)*
```
sudo pacman -S --needed base-devel pacman-contrib cargo
git clone https://git.getcryst.al/crystal/pkgbuilds/ame
cd ame && makepkg -si
```

With that installed just use it to install Urn
```
ame install urn-git
distrobox-export --app urn
```

### Coding
I personnally install nodejs and python on my systems.

#### Nodejs
For nodejs I install [NVM](https://github.com/nvm-sh/nvm) and [PNPM](https://github.com/pnpm/pnpm).
So just follow the guides on their githubs.

Then just use NVM to manage nodejs.
```sh
nvm install --lts
nvm use --lts
```

#### Python
For python I install [PyENV](https://github.com/pyenv/pyenv).

Then just use PyENV to manage python.
```sh
pyenv install "INSERT VERSION"
python global "INSERT VERSION"
```

## SteamOS

## Bazzite

### Coding

#### Devbox
On Bazzite I install [Devbox](https://www.jetpack.io/devbox/) instead of using NVM or PyENV.

It's easy to install just open the konsole and type:
```
fleek add devbox
fleek apply
```

#### Visual Studio Code
Myself I don't like the VSCode flatpak so I use other distributions.

On Bazzite I use the nix package:
```
fleek add vscode
fleek apply
```

## Windows
