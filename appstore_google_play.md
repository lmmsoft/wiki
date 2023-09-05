# 存放 apple appstore 和 google play 相关的文档

## Apple Appstore

### App Store Connect 上传、提交和管理 App
- https://developer.apple.com/cn/app-store-connect/
- https://developer.apple.com/cn/app-store-connect/api/ API介绍
- https://developer.apple.com/documentation/appstoreconnectapi  API文档

### App 审核
- https://developer.apple.com/cn/app-store/review/

### ScreenShot 应用截图相关API

官方文档：

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
