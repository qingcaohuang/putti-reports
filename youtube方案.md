### 方案 1：使用 Cloudflare WARP 伪装出口 (推荐)

在你的 Ubuntu 服务器上安装 **Cloudflare WARP**。它可以将你的云服务器出口 IP 转换成 Cloudflare 的“干净”住宅级 IP。

- **原理**：OpenClaw -> 你的代理 -> **WARP** -> YouTube。
    
- **操作**：在服务器执行 `wget https://pkg.cloudflareclient.com/pubkey.gpg` 安装 warp-cli，并开启 `warp-mode proxy`。这通常能解决 90% 的云服务器封锁问题。
    

---

### 方案 2：最省力的“半自动”折中方案 (不下载视频，只拿字幕)

如果你确实觉得配置代理环境太麻烦，又不想下载巨大的视频文件，你可以使用 **Obsidian Web Clipper 的“内建能力”**：

1. **在 Clipper 模板中集成字幕**：目前一些高级的 Web Clipper 插件支持通过 API 抓取页面上的 Subtitle 轨道。
    
2. **利用“复制字幕”插件**：在浏览器装一个 `YouTube Summary with ChatGPT & Claude` 之类的插件。
    
    - **流程**：你点一下这个插件，它会弹出一键复制全文字幕的按钮。
        
    - **手动接力**：你把字幕粘进 Obsidian 笔记，剩下的**提取重点、整理等脏活累活，统统交给 OpenClaw 在后台扫描这个笔记并执行。