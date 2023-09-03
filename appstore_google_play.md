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

截图 图片格式要求： 
- https://developer.apple.com/help/app-store-connect/reference/screenshot-specifications

### 人机界面指南
- https://developer.apple.com/cn/design/human-interface-guidelines/

## Google Play
