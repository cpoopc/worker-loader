# worker loader for webpack

## [fork from worker-loader](https://github.com/webpack/worker-loader)
在该项目基础上增加了url模式,返回处理后的url.该url可以作为worker的构造参数.弥补了该loader只能创建DedicateWorker的不足.

## Usage
npm install cpoopc-webworker  

* url模式
``` javascript
var workerUrl = require("worker?url!./workerFile.js")
var worker = new Worker(workerUrl)
var sharedWorker = new sharedWorker(workerUrl)
```
* 普通模式 (除了增加了url模式,其他都与原项目一致)
``` javascript
var MyWorker = require("worker!./file.js")
var worker = new MyWorker()
```
* inline模式
``` javascript
var MyWorker = require("worker?inline!./file.js")
```

## License

MIT (http://www.opensource.org/licenses/mit-license.php)
