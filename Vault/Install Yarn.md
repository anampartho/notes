05-12-2023 01:21 PM

Status: #idea
Tags: #yarn #install #nodejs 

# Install Yarn

## 1. [[Install Corepack]]

## 2. Update global Yarn version

#### [[Node.js]] ^16.17 or >=18.6

```bash
corepack prepare yarn@stable --activate
```

#### [[Node.js]] <16.17 or <18.6

```bash
corepack prepare yarn@<version> --activate
```

## 3. Initialize

The following command will create some files, add them to your next commit.

```bash
yarn init -2
```

---
# References
1. [Installation V3](https://v3.yarnpkg.com/getting-started/install)