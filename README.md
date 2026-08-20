# pilot-static

网站管理体系 P1 试点站：最简纯静态页，用于验证部署链路。

**链路**：本仓库 `git push` → Render 自动构建 → 全球 CDN → `xxx.onrender.com`（HTTPS）

## 部署配置

- 类型：Render Static Site（免费档）
- 构建命令：无
- 发布目录：仓库根目录（`.`）
- 声明式配置见 [`render.yaml`](./render.yaml)（Blueprint）

## 验收标准（P1）

- [ ] `xxx.onrender.com` 可正常打开
- [ ] HTTPS 绿锁（证书由 Render 自动签发）

## 后续

- P2：Cloudflare 添加 CNAME（灰云）→ Render 绑定自定义二级域名
- P3：其余静态站 / 3D 站复制本流程（每站一仓库）
