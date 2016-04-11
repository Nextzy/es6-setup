## How to setup babel with webpack

Insatll dependencies

```
npm install webpack babel-core babel-preset-es2015 --save
```

Create `webpack.config.js` file with following code:

```js
module.exports = {
    entry: './main.js',
    output: {
        path: __dirname + '/dist',
        filename: 'main.js'
    },
    module: {
        loaders: [
            {
                test: /\.js$/,
                exclude: /node_modules/,
                loader: 'babel',
                query: {
                    presets: ['es2015']
                }
            }
        ]
    }
}
```

Run webapck command

```
node_modules/.bin/webpack
# or npm run webpack
```
