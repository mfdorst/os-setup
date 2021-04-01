# Install packages
```
sudo apt install zsh emacs-nox git hub
```

# Install Oh-My-Zsh
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

# Install starship prompt
```
curl -fsSL https://starship.rs/install.sh | bash
```

Add the following line to the end of `~/.zshrc`
```
eval "$(starship init zsh)"
```

# Install Doom Emacs
```
git clone --depth 1 https://github.com/hlissner/doom-emacs ~/.emacs.d
~/.emacs.d/bin/doom install
```

# Install rustup
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

# Install rust stable
```
rustup update stable
```

# Install exa
```
cargo install exa
```

# Install alacritty

## Dependencies
```
sudo apt install cmake pkg-config libfreetype6-dev libfontconfig1-dev libxcb-xfixes0-dev python3
```

## Install
```
cargo install alacritty
```

# Set default terminal to alacritty
```
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator $(which alacritty) 50
```

`Ctl+Alt+T` should now open alacritty.

# Generate ssh keys
```
ssh-keygen -t ed25519 -C "m@mdorst.net"
```

`ed25519` is a newer signature scheme. If the system doesn't support it, use `rsa` instead.

# Add ssh key to github

Navigate to `github.com/settings/keys/new` and paste in your public key from `~/.ssh/id_ed25519.pub`.

