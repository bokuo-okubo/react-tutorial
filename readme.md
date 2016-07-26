# Create boiler plate React and Webpack with npm

## Step1: npm init


## Step2: install webpack

=> compile and shorten javascript.


## Step3: configure webpack.

=> create webpack.config.js


## Step4: touch index.html

check runnning the bundle.js


## Step5: setting up babel-loader

babel-loader, which is a transpiler jsx to js.
`npm install babel-loader babel-preset-es2015 babel-preset-react -S`


## Step6: create `.babelrc`

```
{
  "presets" : ["es2015", "react"]
}

```


## Step7: fix `webpack.config.js` for babel

like this.
```
var config = {
  entry: APP_DIR + '/index.jsx',
  output: {
    path: BUILD_DIR,
    filename: 'bundle.js'
  },
  module: {
    loaders: [
      {
        test: /\.jsx?$/,
        include: APP_DIR,
        exclude: /node_modules/,
        loader: 'babel',
        query: {
          cacheDirectory: true,
          presets: ['react','es2015']
        }
      }
    ]
  }
};
```


## Step8: install react, react-dom

`npm install react react-dom -S`


## Step9: use npm as a task runner for watch directory tasks.


fix as the code bellow into `package.json`.
```
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1",
  "develop": "webpack -d --watch",
  "build": "webpack -p"
},
```

and run `npm run watch`
