07-12-2023 01:40 PM

Status: #idea
Tags: #typescript/install

# Installing TypeScript in a Project

First we need to [[How to Initialize an JS Project|initialize the project]]. Then we will add a simple `ts` file under `src/index.ts`.

Then we will install [[TypeScript]]:

```bash
yarn add typescript --dev
```


Add a `dev` script on the `package.json`:

```json
{
	"name": "welcome-to-ts",
	"license": "NOLICENSE",
	"devDependencies": {
		"typescript": "^5.2.0"
	},
	"scripts": {
		"dev": "tsc --watch --preserveWatchOutput" // new
	}
}
```

Add a `tsconfig.json` file at the `root` folder of the project and add some basic rules:

```json
{
	"compilerOptions": {
		"outDir": "dist", // where to put the TS files
		"target": "ES2015", // JS language level (as a build target)
		"moduleResolution": "Node" // Find cjs modules in node_modules
	},
	"include": ["src"] // which files to compile
}
```

Now we can run the compiler using `yarn dev`. This will watch the `src/index.ts` file and compile that file on change.

---
# References

1. [[Install TypeScript#In a Project]]
