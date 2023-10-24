# 存放 apple appstore 和 google play 相关的文档

## Apple Appstore

### App Store Connect 上传、提交和管理 App
- https://developer.apple.com/cn/app-store-connect/
- https://developer.apple.com/cn/app-store-connect/api/ API介绍
- https://developer.apple.com/documentation/appstoreconnectapi  API文档

### App 审核
- https://developer.apple.com/cn/app-store/review/

### ScreenShot 应用截图相关API
上传的格式可以用2种：
- 图片叫做 app screenshot
- 视频叫做 app preview

官方文档：
- 什么是app预览: https://developer.apple.com/app-store/app-previews/

- List All App Screenshot Sets for an App Store Version Localization （截图） https://developer.apple.com/documentation/appstoreconnectapi/list_all_app_screenshot_sets_for_an_app_store_version_localization
- List All App Preview Sets for an App Store Version Localization （短视频） https://developer.apple.com/documentation/appstoreconnectapi/list_all_app_preview_sets_for_an_app_store_version_localization

官方API： 截图相关：Create sets of app screenshots to upload to App Store Connect.

- https://developer.apple.com/documentation/appstoreconnectapi/app_store/app_metadata/app_screenshot_sets 图片集合，包含目标语言和屏幕大小
- https://developer.apple.com/documentation/appstoreconnectapi/app_store/app_metadata/app_screenshots 单张图片

Swift API，有 openapi生成，相邻的文档都值得一看

- https://github.com/AvdLee/appstoreconnect-swift-sdk/blob/master/Sources/OpenAPI/Generated/Entities/AppScreenshot.swift
- https://github.com/AvdLee/appstoreconnect-swift-sdk/blob/master/Sources/OpenAPI/Generated/Entities/AppScreenshotSetAppScreenshotsLinkagesResponse.swift
- https://github.com/AvdLee/appstoreconnect-swift-sdk/blob/master/Sources/OpenAPI/Generated/Entities/ScreenshotDisplayType.swift

### Fastline
- AppStore 上传图片的文档： https://docs.fastlane.tools/getting-started/ios/screenshots/#upload-screenshots-to-the-app-store 参考命令 ```fastlane deliver```
- GooglePlay 上传图片的文档： https://docs.fastlane.tools/getting-started/android/screenshots/#upload-screenshots-to-google-play 参考命令 ```fastlane supply```
- 上传图片相关代码参考ruby https://github.com/fastlane/fastlane/blob/ab9fb3249adaddf6c05655891b4d280415dfc84e/deliver/lib/deliver/upload_screenshots.rb

- 上传到 AppStore/GooglePlay
  - 文档
    - https://docs.fastlane.tools/actions/upload_to_app_store/
    - https://docs.fastlane.tools/actions/upload_to_play_store/
  - 源码
    - https://github.com/fastlane/fastlane/blob/master/fastlane/lib/fastlane/actions/upload_to_app_store.rb
    - https://github.com/fastlane/fastlane/blob/master/fastlane/lib/fastlane/actions/upload_to_play_store.rb

截图 图片格式要求： 
- https://developer.apple.com/help/app-store-connect/reference/screenshot-specifications

### 人机界面指南
- https://developer.apple.com/cn/design/human-interface-guidelines/

## Google Play
- 上传应用 https://developers.google.com/android-publisher?hl=zh-cn#publishing
- 上传图片 https://developers.google.com/android-publisher/api-ref/rest/v3/edits.images/upload?hl=zh-cn
- 上传文件API + SDK: https://developers.google.com/android-publisher/upload?hl=zh-cn#exp-backoff
- RestAPI列表 https://developers.google.com/android-publisher/api-ref/rest?hl=zh-cn#rest-resource:-v3.edits.images

- JWT用法 https://developers.google.com/identity/protocols/oauth2/service-account?hl=zh-cn#jwt-auth
- 上传文件 https://developers.google.com/android-publisher/upload?hl=zh-cn
- 上传应用的参考代码，使用SDK https://github.com/googlesamples/android-play-publisher-api/tree/master/v3/java/src/com/google/play/developerapi/samples
- 上传代码SDK+非SDK
  - https://developers.google.com/api-client-library/java/google-api-java-client/media-upload?hl=zh-cn
  - https://developers.google.com/api-client-library/java/google-api-java-client/media-upload?hl=en

  - temu in Google Play: https://play.google.com/store/apps/details?id=com.einnovation.temu&hl=zh-cn&gl=cn

## 多语言 Localization
- 第三方网站找到了iOS/AppStore/GooglePlay的语言代码列表，非常好用
  - https://www.ibabbleon.com/iOS-Language-Codes-ISO-639.html
  - https://www.ibabbleon.com/Google-Play-Store-Language-Codes.html
- 苹果官方的语言列表 https://developer.apple.com/help/app-store-connect/reference/app-store-localizations/
- 第三方苹果语言列表，带国旗emoji https://appfollow.io/app-store-keywords-localizations
