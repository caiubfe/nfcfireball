# NFC 写入使用手册（简明版）

## 推荐标签型号
- NTAG213 / NTAG215 / NTAG216（常见、兼容性好）
- 容量（NTAG213 ~144 bytes）适合保存短 URL

## 推荐写入 App
- Android: NFC Tools, NXP TagWriter
- iOS: NFC Tools, NXP TagWriter (iOS 支持写入需 iPhone 7 及以上并有 NFC 写入权限)

## 写入步骤（用 NFC Tools 为例）
1. 打开 NFC Tools -> Write -> Add a record -> URL
2. 填写要写入的 URL，例如：
   `https://<your-username>.github.io/<repo-name>/?spell=fireball`
3. 点击 Write，把手机背部贴近标签并保持直到提示写入成功。

## 测试读取
- Android: 将标签靠近手机，通常会直接弹出浏览器选择并打开 URL（Chrome 等）。
- iPhone: 系统会在锁屏或主屏幕弹出一个通知，点击通知进入 Safari 打开该 URL。

## 注意事项
- URL 请使用 HTTPS（GitHub Pages 默认 HTTPS），以避免被某些系统阻止。
- 若想在浏览器内直接扫描并处理标签（不离开页面），仅 Chrome for Android 支持 Web NFC（NDEFReader）。iOS 不支持 Web NFC，目前无法在网页内读取 NFC 数据。

## 批量写入
- 可使用支持批量写入的 NFC 写入工具（部分 Android app / 专业写卡器支持）。
- 也可以用带 NFC 写功能的 Linux 工具或专用硬件批量写标签。
