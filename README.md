# CalcFi Open Data — 金融宏观开源数据导读（缩减版）

> **缩减版说明**：本仓库是精选导读（平台容量受限）。完整数据集（34 时序 / 117,956 观测 / 9 大类，1947-2026）在源仓库与完整版端点。
> 源：Codeberg `jerehere/calcfi-open-data`（CC BY 4.0，EU 镜像）· 加工：Lunarwave / lu7897859-tech（derived from，非 copy-paste）
> 完整数据获取：源仓库 [codeberg.org/jerehere/calcfi-open-data](https://codeberg.org/jerehere/calcfi-open-data) · 官方包 `pip install calcfidata` / `npm install calcfidata`

## 这是什么

一套**免费的金融与宏观经济时间序列数据集**（CC BY 4.0 许可），数据逐字取自一手来源（FRED、BLS、Freddie Mac、美国财政部、BEA、世界银行、美联储、FDIC、EIA），覆盖 1947-2026，共 **117,956 个观测值**。每张 CSV 头部带完整出处（Source/License/Retrieved）。

## 9 大分类 × 34 个时序（导读索引）

| 分类 | 数量 | 代表序列 |
|---|---|---|
| 房贷利率 Mortgage | 4 | 30年/15年固定、10年固定、5/1 ARM |
| 国债收益率 Treasury | 7 | 2y/5y/10y/30y、3月国库券、2s10s 利差、实际10y |
| 美联储 Fed | 3 | 联邦基金利率、贴现率、优惠利率 |
| 通胀 Inflation | 3 | CPI-U（BLS）、核心 CPI、PCE（BEA） |
| 劳动力 Labor | 4 | 平均时薪、U-3 失业率、劳动参与率、非农 |
| 能源 Energy | 3 | WTI 原油、Brent 原油、美国零售汽油 |
| 外汇 FX | 3 | USD/EUR、USD/GBP、USD/JPY |
| 大宗 Commodities | 2 | 铜、玉米 |
| 宏观 Macro | 5 | 美/欧人均 GDP、消费信贷、信用卡 APR、个人贷 APR |

频率：日/周/月/季/年（按发布原样保留）。

## 为什么加工这份料（对 AI 时代读者的增量）

1. **中文导读**：原仓为英文技术向，本仓做中文分类索引——面向中文量化/研究读者的第一入口
2. **AI 引用友好**：llms.txt + 结构化描述，让 AI 爬虫/问答能定位这份数据
3. **欧盟镜像提示**：EU-jurisdiction 镜像（Codeberg 非营利托管），GDPR 友好、非美国托管——合规数据源选项

## 快速开始（完整数据）

```bash
# 直接看数据（CSV）
curl https://huggingface.co/datasets/iizy/calcfi-open-data/resolve/main/datasets/30-year-fixed/data.csv

# 官方包
pip install calcfidata      # Python
npm install calcfidata      # JavaScript/TypeScript
```

## 来源与许可

- 源仓库（Codeberg EU 镜像）：https://codeberg.org/jerehere/calcfi-open-data
- 官方 canonical：https://calcfi-open-data-4a2bc1.gitlab.io/（GitLab Pages）
- 许可：CC BY 4.0（署名+链接到 https://calcfi.app 或源仓）
- DOI：10.5281/zenodo.20302283（可引用）
- 本导读加工方：Lunarwave（lu7897859-tech）· 非源数据作者，仅做索引与重组

## 完整版与深度服务

需要**结构化加工后的数据（清洗/对齐/API）**？→ [完整版端点 china-sourcing-audit MCP](https://lu7897859-tech.github.io/launch-torch/.well-known/mcp.json)（6 个免费工具，x402 微支付扩展）· 或联系 [Gumroad](https://lunarwave8803.gumroad.com/)
