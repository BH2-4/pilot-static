# pilot-static

网站管理体系 P1+P2 试点站：最简纯静态页，用于验证部署链路。

**链路**：本仓库 `git push` → Render 自动构建 → 全球 CDN → `pilot.randomplayx.com`（HTTPS，灰云 CNAME）

- 自定义域名：`pilot.randomplayx.com`（Cloudflare 灰云 CNAME → `pilot-static.onrender.com`）
- 默认域名：`pilot-static.onrender.com`

## 部署配置

- 类型：Render Static Site（免费档）
- 构建命令：无
- 发布目录：`public/`（Render 标准约定）
- 声明式配置见 [`render.yaml`](./render.yaml)（Blueprint）

## 验收记录（P1 + P2 均通过，2026-08-21）

- [x] `pilot-static.onrender.com` 可正常打开
- [x] HTTPS 绿锁（Google Trust Services 自动签发）
- [x] `pilot.randomplayx.com` 全球解析生效（灰云 CNAME）
- [x] 自定义域名证书自动签发（CN=pilot.randomplayx.com）

## 后续

- P3：其余静态站 / 3D 站复制本流程（每站一仓库 + 一条灰云 CNAME）
