## How to setup babel with `babel-cli`

Create `.babelrc` file with

```
{
    "presets": ["es2015"]
}
```

Install cli and presets

```
npm install babel-cli babel-preset-es2015 --save-dev
```

Run!

```
./node_modules/.bin/babel-node main.js
# or npm start
```
