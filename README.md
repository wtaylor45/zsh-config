# What is this repo?

This is my personal zsh configuration! It's mostly for me whenever I have to re-setup my zsh for whatever reason.

# Setup

## Hyper

[Hyper](https://hyper.is) is my terminal of choice. Install Hyper using [Homebrew](https://brew.sh/)

`brew cask install hyper`

I prefer to use the dracula theme, but you can use whatever you like. Install and automatically start using dracula by running `hyper i hyper-dracula`.

Copy the contents of this repo's `.hyper.js` and replace the contents of `~/.hyper.js`. Probably a good idea to make a backup.

## Install oh-my-zsh

Zsh is my preferred shell, which I think is best used with [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh).

**macOS Catalina+ comes with zsh preinstalled** Install Zsh with `brew install zsh` and set it as your default shell by executing `chsh -s /bin/zsh`.

Install oh-my-zsh with `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`.

## Replace the existing .zshrc with the config in the repo

Either remove `~/.zshrc` and replace it with the new `.zshrc`, or just copy and paste the contents from one to the other. It's probably a good idea to make a backup of your exsiting `.zshrc`.

This comes with all of the configuration needed to make the fancy stuff we setup below. The important things to note right now are it alias's two commands. `update` will run `source` on your `.zshrc` to update your config. `change` will open up `.zshrc` in VSCode.

## Spaceship theme

Install the [Spaceship](https://github.com/denysdovhan/spaceship-prompt) theme. Follow the instructions there, or run the following commands on macOS:

`git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"`
`ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"`

## Grab zsh-syntax-highlighting

[zsh-synrtax-lighting](https://github.com/zsh-users/zsh-syntax-highlighting) hgihglights commands as you type. Very useful to have. Follow the installation isntructions on the repo, or run the following:

```zsh
# Navigate to, or create if it doesn't exist
cd /usr/local/share/zsh
# Clone the zsh-syntax-highlighting repo
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
```

## Get the z command

Copy the contents of `z.sh` from the [z repo](https://github.com/rupa/z/blob/master/z.sh) into a new `z.sh` file in `/usr/local/etc/profile.d`. Again, create that directory if it doesn't exist already.

## Colorls

[Colorls](https://github.com/athityakumar/colorls#installation) is a great improvement to the default `ls` command. Follow the installation instructions on the repo. For step 2 when it comes time to pick a font, I tend to use FiraCode. Install FiraCode by running:

```sh
brew tap homebrew/cask-fonts
brew cask install font-firacode-nerd-font
```

`FuraCode Nerd Font` is the name of the font itself. That's already been set as the font in `./.hyper.js`. Feel free to use any nerd font you'd like, however.

The `l` & `ll` commands have already been configured in `.zshrc`. These emulate `ls` and `ls -l` but use colorls instead.

## And your done!

That's all that goes into this setup!