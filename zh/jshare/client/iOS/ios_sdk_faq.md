#iOS SDK FAQ




##分享不成功？


在iOS9/10下就需要增加一个应用可跳转的白名单，如果没配置白名单，则分享不成功。

在项目中的 info.plist 应用白名单看：<a href="https://docs.jiguang.cn/jshare/client/iOS/ios_sdk/#xcode">ApplicationQueriesSchemes</a>


##分享成功后，回不到应用

URL Types 没有配置或者 URL Schemes 格式不对；查看：<a href="https://docs.jiguang.cn/jshare/client/iOS/ios_sdk/#xcode">URL Types 设置</a>


##分享成功，但是统计不到数据
必须在 Appdelegate 的 application 中调用 handleOpenUrl:(NSURL *)url 回调接口。 如果不调用 handleOpenUrl 接口，则获取不到分享成功后的数据。


