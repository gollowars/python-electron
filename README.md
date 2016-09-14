# Python+Electronデスクトップアプリのパッケージング

## require
```
pip install Flask
pip install pyinstaller
npm install electron-prebuilt -g
npm install request-promise -g
```

## packaging
python packaging

```terminal:shell
pyinstaller hello.py
```
alter code in main.js for electron app

```Node:main.j
// develop
var subpy = require('child_process').spawn('python',['./hello.py']);
```

change to

```Node:main.j
// pacaking
var subpy = require('child_process').spawn('./dist/hello/hello');
```

electron packaging

```terminal:shell
electron-packager . sample --platform=darwin --arch=x64 --version=0.36.1
```


refer : [Electron as GUI of Python Applications](https://www.fyears.org/2015/06/electron-as-gui-of-python-apps.html)
