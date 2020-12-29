
- 下载地址：[releases](https://github.com/wzdnzd/ShadowsocksX-NG-R/releases)

# ShadowsocksX-NG-R

[![Build Status](https://travis-ci.org/shadowsocksr/ShadowsocksX-NG.svg?branches=develop)](https://travis-ci.org/shadowsocksr/ShadowsocksX-NG)

[ShadowsocksX-NG](https://github.com/shadowsocks/ShadowsocksX-NG) with SSR support.

## Why?

It's hard to maintain the original implement. There are too many unused code in it. 
It also embed ss-local source. It's crazy to maintain depandences of ss-local. 
So it's hard to update ss-local version.

Now I just copy the ss-local from home brew. Run ss-local executable as a Launch Agent in background. 
Serve pac js file as a file url. So there are only some souce code related to GUI left. 
Then I rewrite the GUI code by swift.

## Requirements

### Running

- macOS 10.12 +

### Building

- Xcode 11.1+
- cocoapod 1.8.4+

## Fetures

- SSR features!
- Ability to check update from GitHub.
- White domain list & white IP list
- Use ss-local from shadowsocksr-libev 2.5.6
- Ability to update PAC by download GFW List from GitHub. (You can even customize your list)
- Ability to update ACL white list from GutHub. (You can even customize your list)
- Show QRCode for current server profile.
- Scan QRCode from screen.
- Import config.json to config all your servers (SSR-C# password protect not supported yet)
- Auto launch at login.
- User rules for PAC.
- Support for OTA is removed
- An advance preferences panel to configure:
  - Local socks5 listen address.
  - Local socks5 listen port.
  - Local socks5 timeout.
  - If enable UDP relay.
  - GFW List url.
  - ACL White List url.
  - ACL GFW list and proxy bach CHN list.
- Manual spesify network service profiles which would be configure the proxy.
- Could reorder shadowsocks profiles by drag & drop in servers preferences panel.
- Auto check update (unable to auto download)

## Different from orignal ShadowsocksX

Run ss-local as backgroud service through launchd, not in app process.
So after you quit the app, the ss-local maybe is still running. 

Add a manual mode which won't configure the system proxy settings. 
Then you could configure your apps to use socks5 proxy manual.

## Contributing

Contributions must be available on a separately named branch based on the latest version of the main branch develop.

ref: [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/)

## License

The project is released under the terms of GPLv3.
