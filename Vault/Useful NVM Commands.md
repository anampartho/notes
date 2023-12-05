05-12-2023 01:05 PM

Status: #idea
Tags: #nodejs #nvm 

# Useful NVM Commands

- Install latest version of node:

```bash
nvm install node # "node" is an alias for the latest version
```

- Install a specific version of node:

```bash
nvm install 14.7.0 # or 16.3.0, 12.22.1, etc
```

- Check available versions

```bash
nvm ls-remote
```

- Check installed versions

```bash
nvm ls
```

- Set default node version

```bash
nvm alias default node # or 18 or 16 or any specific version
```

- Use a specific version for the current terminal session

```bash
nvm use 16 # or "node" oe 17 etc.
```
---
# References
1. [Usage](https://github.com/nvm-sh/nvm#usage)