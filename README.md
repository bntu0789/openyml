# OpenYML - Clash 精简配置

专注 **AI 服务分流**的 Clash 配置文件，简化规则、提升效率。

## 📁 文件说明

| 文件 | 用途 | DNS 配置 |
|------|------|----------|
| `clash_Lite.yaml` | 订阅覆盖 | ❌ |
| `clash_Lite_DNS.yaml` | 独立使用 | ✅ |
| `clash_Full.yaml` | 完整配置（参考） | ❌ |
| `subs.txt` | 订阅地址 | - |

## 🔗 CDN 链接（推荐）

```bash
# 精简版（订阅覆盖）
https://cdn.jsdelivr.net/gh/bntu0789/openyml@main/clash_Lite.yaml

# 精简版 + DNS（独立使用，兼容 OpenClash/ShellCrash）
https://cdn.jsdelivr.net/gh/bntu0789/openyml@main/clash_Lite_DNS.yaml

# 完整版
https://cdn.jsdelivr.net/gh/bntu0789/openyml@main/clash_Full.yaml
```

## 🎯 策略组

| 策略组 | 用途 |
|--------|------|
| 🚀 节点选择 | 主代理选择器 |
| 🤖 AI 服务 | Gemini/Claude/OpenAI/Copilot 专用 |
| 🤖 AI 美国/日本/新加坡 | AI 专用地区节点（GM/GPT 关键字筛选） |
| 🇯🇵 日本节点 | 日本地区节点 |
| 🇸🇬 新加坡节点 | 新加坡地区节点 |
| 🇺🇸 美国节点 | 美国地区节点 |
| 🌏 亚洲节点 | 港/台/日/新/韩 |
| 🛑 广告拦截 | 默认 REJECT，误杀时可切换 |
| 🎯 全球直连 | 国内流量直连 |

## 📋 规则优先级

1. **Google Play 下载直连** → 解决下载问题
2. **私有网络直连** → 局域网/本地
3. **广告拦截** → Loyalsoldier 规则（10万+）
4. **AI 服务** → Gemini/Claude/OpenAI/Copilot
5. **GFW 被墙域名** → 走代理
6. **中国 IP** → 直连
7. **兜底规则** → 走代理

## 📦 规则集来源

- **Loyalsoldier/clash-rules** - 基础规则（每日更新，24k+ Stars）
- **blackmatrix7/ios_rule_script** - AI 服务规则（覆盖最全，24k+ Stars）

## ⚙️ DNS 配置特点（clash_Lite_DNS.yaml）

- ✅ **Fake-IP 模式** - 性能最优
- ✅ **国内外 DNS 分流** - 国内用阿里/腾讯 DOH，国外用 Cloudflare/Google DOH
- ✅ **无 `listen` 端口** - 兼容 OpenClash/ShellCrash 自动管理
- ✅ **Fake-IP 过滤** - NTP、游戏、网易云等返回真实 IP

## 📝 使用方法

### 订阅覆盖（推荐）

在 Sub-Store 或 Clash Verge 中使用 `clash_Lite.yaml` 作为覆盖配置。

### 独立使用

直接导入 `clash_Lite_DNS.yaml`，需要手动添加 `proxies` 节点。

## 📄 License

MIT
