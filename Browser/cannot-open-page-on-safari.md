# Cannot open page on browser Safari

## Source article

[Debug a Website in iOS Safari on Windows 10](https://washamdev.com/debug-a-website-in-ios-safari-on-windows/) - John Washam

## Install iTunes

You can install iTunes for Windows from Windows App Store

## Install NodeJS

### Install Scoop

Source: [How to install the Scoop package manager in Windows 10](https://www.onmsft.com/how-to/how-to-install-the-scoop-package-manager-in-windows-10) - James Walker

Open PowerShell and run commands:

```
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

### Install remote debug

```
npm install remotedebug-ios-webkit-adapter -g
scoop install ios-webkit-debug-proxy
```
## Run debug

```
remotedebug_ios_webkit_adapter --port=9000
```

## Config Chrome

Open chrome and go to: [chrome://inspect/#devices](chrome://inspect/#devices)

Click `Configure...` button

Add address: `localhost:9000` and click `Done`

## Config device

On your iOS device, go to `Settings` > `Safari` > `Advance` and enable `Web Inspector`