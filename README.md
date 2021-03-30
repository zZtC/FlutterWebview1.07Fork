# WebView for Flutter
基于官方Webview插件做的改造。  
由于官方插件不支持读取assets中的h5，  
三方插件[InAppWebview](https://github.com/pichillilorenzo/flutter_inappwebview)又不支持传递参数

故修改源码使支持。
## 说明
- 基于官方[WebView(tag:webview_flutter-v1.0.7)](https://github.com/flutter/plugins/tree/webview_flutter-v1.0.7/packages/webview_flutter)
插件
- 支持assets中的h5加载，支持参数传递
- 不支持Flutter2.0
- 自用

## 使用方法
在flutter工程中放入文件后，在`pubspec.yaml`中做如下声明

```
assets:
    - h5/
```
然后就可使用WebView进行加载  
`assets://`开头即为本地h5

```
WebView(
  initialUrl: 'assets://h5/index.html?language=zh',
),
```