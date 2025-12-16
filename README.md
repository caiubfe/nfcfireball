# Spell NFC Site

这是一个示例静态网站，演示如何：
- 上传并播放法术音效（audio/*.mp3）
- 为每个法术投掷骰子（例如 8d6）
- 将每个法术的 URL 写入 NFC 标签：当手机贴近标签时打开对应网页并自动播放音效与投骰

## 快速开始（GitHub Pages）
1. 新建一个 GitHub 仓库（例如 `spell-nfc-site`）。
2. 将 `index.html`、`spells.json`、`audio/` 文件夹上传到仓库根目录。
3. 在仓库 Settings -> Pages 启用 GitHub Pages（branch: main, root）。
4. 访问 `https://<your-username>.github.io/<repo-name>/` 即可。

## 修改法术（静态方式）
- 把音频文件放 `audio/` 目录。
- 编辑 `spells.json`，添加新的键（key）和对应字段：
  - name, desc, audio, dice
- 提交到仓库后页面会反映新的法术。

## NFC 写入
把 URL 写到标签，例如：
`https://<your-username>.github.io/<repo-name>/?spell=fireball`

写入建议使用手机应用：NFC Tools、NXP TagWriter 等。

## 进阶：Firebase 版（动态上传/管理）
仓库中包含 `firebase/` 目录示例，说明如何用 Firebase Storage + Firestore 实现网页内上传并管理法术。

