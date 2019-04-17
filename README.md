[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/steemit/steem-js/blob/master/LICENSE)
[![Steem.js channel on steemit.chat](https://img.shields.io/badge/chat-steemit.chat-1c56a4.svg)](https://steemit.chat/channel/steemjs)

P5K8d1jmRUrraGqxQSHJxVaZ2RbkpeSUzrqFkmY7WkfTT1gSZgxr   
5JXL23cyxtYw7vkwKnyPsWHPAnM54iz1TBPUq6P632vYBmBL5PE

## 打包流程：  
### 1、clone该项目  
### 2、安装node8.7 npm5.4.2 环境  
### 3、npm安装依赖：  
```html
npm install webpack@1.13.2 webpack-visualizer-plugin@0.1.5 should@11.1.0 mocha@3.0.2 mocha-make-stub@2.3.2 babel-cli@6.16.0 babel-eslint@7.1.1 babel-loader@6.2.5 babel-polyfill@6.23.0 babel-preset-es2015@6.16.0 babel-preset-es2017@6.16.0 babel-register@6.14.0 bluebird@3.4.6 eslint@3.5.0 eslint-plugin-import@1.15.0 eslint-plugin-jsx-a11y@2.2.2 eslint-plugin-react@6.2.1 json-loader@0.5.4  
```
并全局安装(npm install * -g)  
```html
npm install @steemit/rpc-auth@1.1.1 bigi@1.4.2 bluebird@3.4.6 browserify-aes@1.0.6 bs58@4.0.0 buffer@5.0.6 bytebuffer@5.0.1 create-hash@1.1.2 create-hmac@1.1.4 cross-env@5.0.0 cross-fetch@1.1.1 debug@2.6.8 detect-node@2.0.3 ecurve@1.0.5 lodash@4.16.4 retry@0.12.0 secure-random@1.1.1 ws@3.3.2  
```
并全局安装(npm install * -g)  
### 4、打包：
webpack   
打包压缩后的js库文件在disk文件夹中  

# Steem.js
Steem.js the JavaScript API for Steem blockchain

# Documentation

- [Install](https://github.com/steemit/steem-js/tree/master/doc#install)
- [Browser](https://github.com/steemit/steem-js/tree/master/doc#browser)
- [Config](https://github.com/steemit/steem-js/tree/master/doc#config)
- [Database API](https://github.com/steemit/steem-js/tree/master/doc#api)
    - [Subscriptions](https://github.com/steemit/steem-js/tree/master/doc#subscriptions)
    - [Tags](https://github.com/steemit/steem-js/tree/master/doc#tags)
    - [Blocks and transactions](https://github.com/steemit/steem-js/tree/master/doc#blocks-and-transactions)
    - [Globals](https://github.com/steemit/steem-js/tree/master/doc#globals)
    - [Keys](https://github.com/steemit/steem-js/tree/master/doc#keys)
    - [Accounts](https://github.com/steemit/steem-js/tree/master/doc#accounts)
    - [Market](https://github.com/steemit/steem-js/tree/master/doc#market)
    - [Authority / validation](https://github.com/steemit/steem-js/tree/master/doc#authority--validation)
    - [Votes](https://github.com/steemit/steem-js/tree/master/doc#votes)
    - [Content](https://github.com/steemit/steem-js/tree/master/doc#content)
    - [Witnesses](https://github.com/steemit/steem-js/tree/master/doc#witnesses)
- [Login API](https://github.com/steemit/steem-js/tree/master/doc#login)
- [Follow API](https://github.com/steemit/steem-js/tree/master/doc#follow-api)
- [Broadcast API](https://github.com/steemit/steem-js/tree/master/doc#broadcast-api)
- [Broadcast](https://github.com/steemit/steem-js/tree/master/doc#broadcast)
- [Auth](https://github.com/steemit/steem-js/tree/master/doc#auth)


Here is full documentation:
https://github.com/steemit/steem-js/tree/master/doc

## Browser
```html
<script src="./steem.min.js"></script>
<script>
steem.api.getAccounts(['ned', 'dan'], function(err, response){
    console.log(err, response);
});
</script>
```

## CDN
https://cdn.steemjs.com/lib/latest/steem.min.js<br/>
```html
<script src="//cdn.steemjs.com/lib/latest/steem.min.js"></script>
```

## Webpack
[Please have a look at the webpack usage example.](https://github.com/steemit/steem-js/blob/master/examples/webpack-example)

## Server
## Install
```
$ npm install steem --save
```

## RPC Servers
https://api.steemit.com By Default<br/>
https://node.steem.ws<br/>
https://this.piston.rocks<br/>

## Examples
### Broadcast Vote
```js
var steem = require('steem');

var wif = steem.auth.toWif(username, password, 'posting');
steem.broadcast.vote(wif, voter, author, permlink, weight, function(err, result) {
	console.log(err, result);
});
```

### Get Accounts
```js
steem.api.getAccounts(['ned', 'dan'], function(err, result) {
	console.log(err, result);
});
```

### Get State
```js
steem.api.getState('/trends/funny', function(err, result) {
	console.log(err, result);
});
```

### Reputation Formatter
```js
var reputation = steem.formatter.reputation(user.reputation);
console.log(reputation);
```

## Contributions
Patches are welcome! Contributors are listed in the package.json file. Please run the tests before opening a pull request and make sure that you are passing all of them. If you would like to contribute, but don't know what to work on, check the issues list or on Steemit Chat channel #steemjs https://steemit.chat/channel/steemjs.

## Issues
When you find issues, please report them!

## License
MIT
