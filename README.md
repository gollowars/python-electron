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

```terminal:shell
pyinstaller hello.py

```
alter code in main.js for electron app

```Node:main.j
// develop
var subpy = require('child_process').spawn('python',['./hello.py']);
```Node:main.j
change to 
```
// pacaking
var subpy = require('child_process').spawn('./dist/hello/hello');
```


electron pacaking
```terminal:shell
electron-packager . sample --platform=darwin --arch=x64 --version=0.36.1
```