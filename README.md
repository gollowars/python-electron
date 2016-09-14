# Python+Electronデスクトップアプリのパッケージング

## require
```
pip install Flask
pip install pyinstaller
npm install electron-prebuilt -g
npm install request-promise -g
```


## packing
python packing

```
pyinstaller hello.py

```

alter code in main.js for electron app

```
// develop
var subpy = require('child_process').spawn('python',['./hello.py']);
```
change to 
```
// pacaking
var subpy = require('child_process').spawn('./dist/hello/hello');
```


electron pacaking
```
electron-packager . sample --platform=darwin --arch=x64 --version=0.36.1
```