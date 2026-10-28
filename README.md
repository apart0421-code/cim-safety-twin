# 建筑安全 CIM 数字孪生 · 上线包

这个文件夹里只有一个 `index.html`（数据、样式、脚本全部内嵌），
上传到任意静态托管就能得到一个可分享的链接。

## 方式 A：GitHub Pages（推荐，免费、稳定）

1. 登录 GitHub，新建仓库，例如 `cim-safety-twin`（Public）。
2. 把本文件夹里的 `index.html` 上传到仓库根目录（网页端 Add file → Upload files）。
3. 仓库 Settings → Pages → Source 选 `Deploy from a branch`，
   Branch 选 `main`，目录选 `/ (root)`，Save。
4. 等 1–2 分钟，访问：
   `https://你的用户名.github.io/cim-safety-twin/`
5. 手机打开测一遍：单指旋转、双指缩放、点建筑、点告警。

## 方式 B：Netlify Drop（不用命令行，30 秒）

1. 打开 https://app.netlify.com/drop
2. 把整个 `孪生上线包` 文件夹拖进去。
3. 得到 `https://随机名.netlify.app`，可在 Site settings 改名。

## 方式 C：Vercel

1. https://vercel.com/new → 导入仓库，或直接拖拽文件夹。
2. Framework 选 Other，Build Command 留空，Output Directory 填 `.`。

## 上线后要做的两件事

1. **换二维码**：用草料二维码（cli.im）把作品集链接生成二维码，
   替换 `求职/assets/qr-vcard.png`，重新导出简历/作品集 PDF。
   （现在简历上的二维码是 vCard，扫码存联系方式；上线后建议换成作品集链接。）
2. **把链接写进简历**：在页脚或项目名后加 `Demo: 你的链接`。

## 说明

- 页面里的建筑、设备、告警、工单数据是**仿真台账**，用于演示流程与交互；
  面试时主动说明，并讲清“可替换为 PostGIS / MQTT 真实数据”。
- 单文件约 830KB，首次加载 1–2 秒；手机端已适配触控。
- 如果 GitHub Pages 访问慢，优先用 Netlify 或 Vercel。

## 自测清单

- [ ] 手机能打开，横屏/竖屏都不错位
- [ ] 点建筑能出属性卡
- [ ] 能触发告警 → 复核 → 工单
- [ ] GeoJSON 能导出
- [ ] 页面底部/关于里有“仿真数据”说明
