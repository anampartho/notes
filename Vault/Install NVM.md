05-12-2023 01:31 AM

Status: #idea
Tags: #nvm/install #nodejs 

# Install NVM

NVM is a version manager for [[Node.js]].

## Prerequisite

If you are on mac, [[zsh]] will be your default shell. Make sure `~/.zshrc` file is present. If not create it using: `touch ~/.zshrc`.

## Using the Install & Update script

To install or update NVM we can run the install script by executing one of the following commands:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

or

```bash
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

```ad-important
collapse: open
The version mentioned in the above commands **(v0.39.5)** can differ. Please make sure to check the **Installing and Updating** link in the reference for the updated version.

```

# Using Homebrew (Mac)

First [[Install Homebrew]] and run the following command:

```bash
brew install nvm
```

## Post install

1. If you have installed using the Using the Install & Update script, and you have `~/.zshrc` file present, you do not need to do anything. If it does not automatically add it, then you can add it manually to the `~/.zshrc` file:

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```

2. If you have installed Using Homebrew (Mac), then after installation, you'll see in the terminal that it mentions to add some code to the `~/.zshrc` file. Copy the code and add it to the `~/.zshrc` file.

![[brew-nvm-postinstall.png]]
---
# References
1. [Installing and Updating](https://github.com/nvm-sh/nvm#installation-and-update)