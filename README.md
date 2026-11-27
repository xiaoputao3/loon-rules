# loon-rules（私有，自用）

自用的 Loon 规则与配置，合并自以下公开来源，仅供个人使用，非商业用途。

## 来源

- iKeLee 进阶配置（luestr/ProxyResource）：`Loon_Advanced_Config_By_iKeLee.lcf`，2025-11-08，CC BY-NC-SA 4.0
- fmz200 / 奶思 `wool_scripts`：服务分流规则、AI.list、去广告插件，GPLv3
- Cue / Manus 规则：RikkaSaiko1/clash_config `rules/cue.txt`，2026-11-25

## 文件

- `Loon_iKeLee_plus_fmz.lcf` — 合并版 Loon 配置：iKeLee 自动分流 + fmz200 服务分流 + Muse / Meta AI 等补全的 AI 规则。导入会覆盖原配置，先备份；`[Proxy]` / `[Remote Proxy]` 仍需自行加节点订阅。
- `rules/my.list` — 自托管规则：Cue / Manus（8 条）+ Muse / Meta AI（7 条）。在 Loon `[Remote Rule]` 里引用，策略写 `人工智能`（或你自己的 AI 策略组名）。
- `rules/AI.list` — AI 分流合集（fmz200 原版 + 补全）：ChatGPT、Claude、Gemini、Meta AI / Muse、Midjourney、Poe、Cursor 等；国产 AI（DeepSeek、Kimi、千问、豆包等）默认注释，国内直连更快，人在海外或想走代理时再去掉 `#`。

## Loon 引用（仓库私有，需在 Loon 里登录 GitHub 账号才能拉取 Raw）

```
https://raw.githubusercontent.com/xiaoputao3/loon-rules/main/rules/my.list, policy=人工智能, tag=MyRules, enabled=true
```

## 注意

- 私有仓库 Raw 链接需要认证，Loon 直接拉取可能会 404；如需在 Loon 里直接用，建议改用公开仓库，或用本地文件导入 `Loon_iKeLee_plus_fmz.lcf`。
- 去广告插件需开 MitM 并装好证书才生效；证书跟着手机 / Loon 走，换配置不用重装。
