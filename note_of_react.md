# Create boiler plate React and Webpack with npm

## Step1
npm init

## Step2
install webpack
=> complie and shrten javascript.

## Step3
configure webpack.
=> create webpack.config.js

## Step4
touch index.html
check runnning the bundle.js

## Step5
setting up babel-loader which is a transpiler jsx to js
`npm install babel-loader babel-preset-es2015 babel-preset-react -S`

## Step6
create `.babelrc`
```
{
  "presets" : ["es2015", "react"]
}

```
## Step7

fix `webpack.config.js`
like this.
```
// Existing Code ....
var config = {
  // Existing Code ....
  module : {
    loaders : [
      {
        test : /\.jsx?/,
        include : APP_DIR,
        loader : 'babel'
      }
    ]
  }
}
```
## Step8
install react, react-dom
`npm install react react-dom -S`
