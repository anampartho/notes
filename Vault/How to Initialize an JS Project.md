07-12-2023 01:12 PM

Status: #idea
Tags: #node #npm #yarn

# How to Initialize an JS Project

We can initialize a [[JavaScript]] project by using both `npm` or `yarn`.

## Prerequisite

[[Install Node.js]]

## Using [[npm]]

We can run `npm init` and follow the prompts or run `npm init -y` so that we can get default values. Running `npm init -y` will create a `package.json` file:

```json
{
  "name": "npminit", // This is the name of the folder
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```


## Using yarn

First we need to [[Install Yarn]]. Then run `yarn init -2`. This will create a few files and folders:

```bash
.
├── .gitignore
├── .pnp.cjs
├── .yarn
│   └── install-state.gz
├── README.md
├── package.json
└── yarn.lock
```

The `package.json` contains the following content:

```json
{
  "name": "ts",
  "packageManager": "yarn@4.0.2"
}
```

---
# References

1. [yarn init](https://yarnpkg.com/cli/init)