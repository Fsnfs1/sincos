## 本地部署位置

此版本已把 **MathJax** 下載到本機，不再依賴外網 CDN。

- **入口檔**：`index.html`
- **本地資源**：`vendor/mathjax/es5/`

## 如何開啟

1. 打開資料夾 `C:\Users\Sam19\Desktop\123`
2. 直接用 Edge 或 Chrome 雙擊開啟 `index.html`

## 為什麼沒有下載 polyfill.io？

你目前環境解析不到 `polyfill.io`（DNS/網路封鎖），所以無法下載。

而且在 Windows 10 的 Edge/Chrome 裡，ES6 大多已原生支援，通常 **不需要 polyfill**；保留它反而會造成「一旦被擋就整個不能用」的不穩定依賴。

## 音效說明（無外部音檔）

遊戲內音效與 **BGM** 全部由 Web Audio API **即時合成**（不需下載 mp3）。立體聲使用 `StereoPannerNode`，依游標左右位置變化；戴耳機時空間感更明顯。開始遊戲後會自動播放背景節奏與和弦，遊戲結束時停止。

