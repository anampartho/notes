05-12-2023 01:19 AM

Status: #idea
Tags: #nodejs/install

# Install Node.js

## Using the pre-built package

Go to [https://nodejs.org/en/download](https://nodejs.org/en/download) and download the package based on your [[Operating System]] and install.

## Using Homebrew (Mac)

First [[Install Homebrew]] and use the following command:
```bash
brew install node
```

## Using NVM

First [[Install NVM]] in your [[Operating System]] and then use the following useful commands to select node versions:

```bash
// check version
node -v || node --version

// list locally installed versions of node
nvm ls

// list remove available versions of node
nvm ls-remote

// install specific version of node
nvm install 18.16.1

// set default version of node
nvm alias default 18.16.1

// switch version of node
nvm use 20.5.1

// install latest LTS version of node (Long Term Support)
nvm install --lts

// install latest stable version of node
nvm install stable
```

---
# References

1. [Useful NVM commands](https://gist.github.com/chranderson/b0a02781c232f170db634b40c97ff455)