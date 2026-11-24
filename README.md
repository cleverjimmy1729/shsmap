# shsmap · 上海中学校园互动地图 🗺️

**made by 2811CPS小组**

在校园平面图上点击发光的红色标记点，弹窗查看该地标的实拍照片。纯静态页面、零依赖，已启用 GitHub Pages 在线访问。

## 🌐 在线使用

仓库已开启 GitHub Pages，入口为 `index.html`（自动跳转到最新版地图）：

> https://cleverjimmy1729.github.io/shsmap/

## 🚀 本地使用

下载仓库后直接双击 `shsmap3.9.html`（最新版），无需服务器；或用任意静态服务器托管本目录。

## ✨ 功能

- **8 个地标标记点**：龙门楼、影视传媒中心、卧龙亭、篮球场、水杉林、甄陶楼、中兴楼、体育场
- 悬停显示名称标签，点击弹出该地点的实拍照片（支持 ESC / 点击遮罩关闭）
- 标记点带呼吸动画，悬停放大
- 内置**调试面板**（左下角"调试模式"按钮）：标记点坐标 / 可见性检查、图片加载检查、点击取坐标

## 📁 文件结构

| 文件 | 说明 |
|---|---|
| `index.html` | GitHub Pages 入口（跳转到最新版） |
| `shsmap3.9.html` | **最新版地图**（当前推荐使用） |
| `shsmap3.6.html` / `shsmap1.3.html` | 历史迭代版本，留存备用 |
| `debug后的shsmap显示尝试.html` | 调试实验版（内嵌地图图片） |
| `map.png` | 校园平面图底图 |
| `*.jpg` / `*.png` | 各地标实拍照片 |

## 🛠️ 添加新地标

在 `shsmap3.9.html` 的 `.map-container` 中复制一组标记点与标签，修改坐标和 `data-title` / `data-image` 即可：

```html
<div class="clickable-area pulse"
     style="left: 800px; top: 600px;"
     data-title="图书馆"
     data-image="library.jpg">
</div>
<div class="location-label" style="left: 800px; top: 600px;">图书馆</div>
```

坐标可通过调试模式点击地图读取。
