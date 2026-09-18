# 爬么 Crux 官方网站

该目录是微信开放平台“应用官网”、App Store Connect 隐私政策、用户支持页面，以及 iOS Universal Link AASA 文件的静态站点。

当前定位为审核临时站点。页面设置 `noindex, nofollow, noarchive`，不主动参与搜索收录；拥有准确 URL 的审核人员仍可直接访问。

上线前必须完成：

1. 在 `index.html` 中把两个 `data-testflight-link` 按钮替换为真实的公开 TestFlight 链接，并移除 `disabled`、`aria-disabled`。
2. 购买并绑定正式域名 `pamecrux.com`，使用 HTTPS 公开部署。
3. 完成正式域名 ICP 备案；抖音移动应用“应用官网”要求可正常访问且已备案，备案主体建议与开发者主体一致。
4. 逐页验证首页、隐私政策、用户协议、支持页，以及 AASA 文件：
   - `https://pamecrux.com/.well-known/apple-app-site-association`
   - `https://pamecrux.com/apple-app-site-association`
5. 微信开放平台的“应用官网”填写首页 URL，不要填写尚未开放的预览地址。
6. 微信开放平台的 Universal Link 建议填写 `https://pamecrux.com/ul/wechat/`，并保持尾部 `/`。

临时审核地址：

- 官网：`https://sophiemly.github.io/crux-review-site/`
- 隐私政策：`https://sophiemly.github.io/crux-review-site/privacy.html`
- 用户协议：`https://sophiemly.github.io/crux-review-site/terms.html`
- 用户支持：`https://sophiemly.github.io/crux-review-site/support.html`

正式域名预定地址：

- 官网：`https://pamecrux.com/`
- 隐私政策：`https://pamecrux.com/privacy.html`
- 用户协议：`https://pamecrux.com/terms.html`
- 用户支持：`https://pamecrux.com/support.html`
- Universal Link / 微信回调：`https://pamecrux.com/ul/wechat/`

本地预览：

```bash
python3 -m http.server 4173 --directory website
```
