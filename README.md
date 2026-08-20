# TwitchDropsMiner No Auto-Claim Build

这是基于 [TwitchDropsMiner](https://github.com/DevilXD/TwitchDropsMiner) `16.dev` 制作的非官方 Windows 补丁构建。

This is an unofficial patched Windows build based on [TwitchDropsMiner](https://github.com/DevilXD/TwitchDropsMiner) `16.dev`.

## 下载 / Download

请从本仓库的 [Releases](../../releases) 页面下载 `TwitchDropsMiner不领取.exe`。仓库不包含用户 Cookie、登录令牌、设置文件、缓存或代理凭据。

Download `TwitchDropsMiner不领取.exe` from this repository's [Releases](../../releases) page. The repository contains no user cookies, login tokens, settings, cache, or proxy credentials.

## 补丁行为 / Patched behavior

该构建来自加入“自动领取掉宝”控制逻辑后的 TwitchDropsMiner。关闭自动领取后，程序不会自动发送领取请求；Twitch 可能要求先领取前置掉宝，才能继续为同一活动的后续掉宝计算服务端进度。

This build comes from TwitchDropsMiner with automatic Drop-claim control added. When automatic claiming is disabled, the program does not automatically send claim requests. Twitch may require prerequisite Drops to be claimed before server-side progress can continue for later Drops in the same campaign.

未领取的掉宝可能过期。该补丁不能绕过 Twitch 服务端规则，也不伪造服务端进度。

Unclaimed Drops may expire. This patch does not bypass Twitch server rules or fabricate server-side progress.

## 校验 / Verification

```text
SHA-256  TwitchDropsMiner不领取.exe
58C7B719496F448CA5E6153724E86334EF551ADF3682AF8DDD929A152250592A
```

PowerShell 校验命令：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath ".\TwitchDropsMiner不领取.exe"
```

## 隐私 / Privacy

请勿上传或分享运行目录中的以下内容：

- `cookies.jar`
- `settings.json`
- `cache/`
- 日志、令牌、代理认证信息或其他凭据

Do not upload or share `cookies.jar`, `settings.json`, cache data, logs, tokens, proxy authentication information, or other credentials.

## 许可和归属 / License and attribution

原项目由 DevilXD 开发并采用 MIT License。本仓库不是 Twitch、Amazon 或原项目作者的官方发布。详见 [LICENSE](LICENSE)。

The original project is developed by DevilXD and licensed under the MIT License. This repository is not an official release from Twitch, Amazon, or the upstream author. See [LICENSE](LICENSE).
