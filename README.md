# Loon 平台分流规则：直接使用版

更新日期：2026-07-16。

此目录只有每个平台可直接使用的 `.list` 文件，没有 Core、Extended、Optional 或合并规则：

- `01-OKX.list`
- `02-Binance.list`
- `03-Bybit.list`（Global，不包含 EU）
- `04-Bybit-EU.list`
- `05-Wise.list`
- `06-iFAST.list`
- `07-Kraken.list`
- `08-Krak.list`

## 使用 GitHub Raw 链接订阅

在 Loon 的“订阅规则”中添加对应 URL，并选择固定策略：

- OKX: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/01-OKX.list`
- Binance: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/02-Binance.list`
- Bybit Global: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/03-Bybit.list`
- Bybit EU: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/04-Bybit-EU.list`
- Wise: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/05-Wise.list`
- iFAST: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/06-iFAST.list`
- Kraken: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/07-Kraken.list`
- Krak: `https://raw.githubusercontent.com/zrj766/loon-platform-rules/main/08-Krak.list`

如果同时使用 Bybit 与 Bybit EU，并希望使用不同出口，请让 `04-Bybit-EU.list` 排在 `03-Bybit.list` 前面。

## 本地 iCloud 备用方法

1. 解压 ZIP。
2. 在 iPhone“文件”App 中打开“iCloud 云盘/Loon/Rules/”。没有该目录就逐级新建。
3. 把需要的 `.list` 文件移动到 `Rules` 文件夹。不要放在“下载项”“在我的 iPhone”或 ZIP 内。
4. 等待云朵图标消失，再打开 Loon 添加本地规则并选择固定策略。

`08-Krak.list` 已包含 Krak 可能使用的 Kraken 公共基础域名。如果 Kraken 和 Krak 使用同一策略，只导入 `08-Krak.list` 也可以；如果分别导入二者，重复域名不会改变匹配结果，但应给二者选择相同策略。

规则应排在宽泛的 `GEOIP`、`Proxy`、`Global`、`FINAL` 规则之前。金融账户建议使用固定地区、固定出口，不要使用频繁跨国家切换的自动策略。

