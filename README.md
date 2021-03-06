# cordova-FileUtil

This package makes it easy to use the "cordova-plugin-file" plug-in

[![NPM Version][npm-version-image]][npm-url]

[![NPM Install Size][npm-install-size-image]][npm-install-size-url]

[![NPM Downloads][npm-downloads-image]][npm-downloads-url]

```javascript
import {CordovaFileUtil} from "../../browser_modules/cordova-fileutil/cordovaFileUtil.js";


// get instance
const cordovaFileUtil = new CordovaFileUtil();

// get directory entry
const dirEntry = cordovaFileUtil.getDirEntry(cordova.file.dataDirectory, 'testFolder');

// get file entry
const fileEntry = cordovaFileUtil.getFileEntry('test.text', dirEntry);

// read file
const readData = cordovaFileUtil.read(fileEntry);

// write file
cordovaFileUtil.write(fileEntry, "test text");

// remove file
cordovaFileUtil.remove('test.text', dirEntry);

// remove directory
cordovaFileUtil.removeDir(dirEntry);
```



## Installation

**How to install from Frontle**

```shell
$ frontle install cordova-fileutil
```



**How to install from Web**

For typical web projects, copy and use the code at cordovaFileUtil.js in below repositorys

https://github.com/Artifriends-inc/cordova-FileUtil (cordovaFileUtil.js)



## Function

#### new CordovaFileUtil()

Get "CordovaFileUtil" object. only one object is created using a single-tone pattern

```javascript
// get instance
const cordovaFileUtil = new CordovaFileUtil();
```



#### cordovaFileUtil.getDirEntry(path, folderName, create = true)

Get folder entry, If the "create" option is true, a folder is created

```javascript
// get directory entry
const dirEntry = cordovaFileUtil.getDirEntry(cordova.file.dataDirectory, 'testFolder');
```



#### cordovaFileUtil.getFileEntry(fileName, dirEntry, create = true)

Get file entry, If the "create" option is true, a file is created

```javascript
// get file entry
const fileEntry = cordovaFileUtil.getFileEntry('test.text', dirEntry);
```



#### read(fileEntry)

Reads file data

```javascript
// read file
const readData = cordovaFileUtil.read(fileEntry);
```



#### write(fileEntry, writeData)

Write file data

```javascript
// write file
cordovaFileUtil.write(fileEntry, "test text");
```



#### remove(fileName, dirEntry)

Remove file

```javascript
// remove file
cordovaFileUtil.remove('test.text', dirEntry);
```



#### removeDir(dirEntry)

Remove directory

```javascript
// remove directory
cordovaFileUtil.removeDir(dirEntry);
```



## People

The original author of cordova-fileutil is [MushStory](https://github.com/MushStory)



## License

[MIT](LICENSE)



[npm-downloads-image]: https://badgen.net/npm/dm/cordova-fileutil
[npm-downloads-url]: https://npmcharts.com/compare/cordova-fileutil?minimal=true
[npm-install-size-image]: https://badgen.net/packagephobia/install/cordova-fileutil
[npm-install-size-url]: https://packagephobia.com/result?p=cordova-fileutil
[npm-url]: https://npmjs.org/package/cordova-fileutil
[npm-version-image]: https://badgen.net/npm/v/cordova-fileutil
