When we want to prepare a Linux server for a project or service, it is better to install tools for our own convenience.

I use many tools to do my work, but the following are the most used.

- __Ohmyzsh__
	> Its like bash, but has very good built-in plugins for git, docker and more
- __Astronvim__
	>A very complete and comprehensive and useful editor for editing files.
		It is like vim, but it has more features.
		To use Astronvim you must have nvim installed.
- __Tmux__
	> To manage screens and split the page and save the session you are working on.

## OhMyZSH

### Install zsh

OhMyZSH is actually a plugin for zsh itself.

So we need to install zsh first to use it.

```bash
sudo apt update
sudo apt install zsh
```

Then install ohmyzsh
> Visit [website](https://ohmyz.sh/)

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Astronvim

### Install nvim

Astronvim like OhMyZsh that is a zsh plugin is actually a plugin for nvim itself.
So install it at first.

Installing nvim is very easy because it is available in the main Ubuntu repository. 

```bash
sudo apt update 
sudo apt install nvim
```

after install nvim, we must to install __Astronvim__ plugin.
> For more information about installing Astronvim, visit [this](https://github.com/neovim/neovim/wiki/Installing-Neovim) link.

```bash
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim.appimage
chmod u+x nvim.appimage
./nvim.appimage
```

If the `./nvim.appimage` command fails, try:

```bash
./nvim.appimage --appimage-extract
./squashfs-root/AppRun --version

# Optional: exposing nvim globally.
sudo mv squashfs-root /
sudo ln -s /squashfs-root/AppRun /usr/bin/nvim
nvim
```

If you want use `vim` in your bash as nvim, open `~/.zshrc` file and put end of the file:

```bash
# ~/.zshrc
...
alias vim=nvim
...
```

## Tmux
In new version of Ubuntu, tmux by default installed.
But if you think you do not have that, run this command:

```bash
sudo apt install tmux
```

So our system was ready.