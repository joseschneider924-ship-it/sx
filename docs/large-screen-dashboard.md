# 智慧供应链运营指挥中心 · 大屏可视化高保真设计

Figma 文件：https://www.figma.com/design/0BhdxOq0CSEyXYje6Jt35z

- 主画板：`大屏 / 智慧供应链运营指挥中心 1920×1080`（node `5:2`）
- 组件库：`🧩 Components`（位于主画板下方）

## 画布与栅格

| 项 | 值 |
| --- | --- |
| 分辨率 | 1920 × 1080（16:9） |
| 顶部标题栏 | 高 96 |
| 内容区 | y = 104 → 1056，高 952 |
| 三栏布局 | 左 x=24 w=456 / 中 x=496 w=928 / 右 x=1440 w=456，栏间距 16 |
| 面板间距 | 8 |
| 背景 | `bg/base` + 40px 网格 + 中心径向光晕 |

## 版块

| 区域 | 面板 | 内容 |
| --- | --- | --- |
| 顶部 | 标题栏 | 时间与日期、导航页签 ×6、主标题（带发光效果）、数据同步状态、天气 |
| 左栏 | 核心运营指标 | 6 张 KPI 卡片（订单总量、采购金额、库存周转、订单履约率、在途车辆、异常订单） |
| 左栏 | 月度订单趋势 | 柱线组合图：订单量柱状 + 履约率折线，11–12 月为预测（虚线柱） |
| 左栏 | 库存结构分析 | 环形图（5 类库存）+ 图例 + 3 项库存指标 |
| 中栏 | 大数字指标 | 今日订单 / 今日发货 / 在库货值 / 准时交付率 |
| 中栏 | 全国仓储物流网络 | 中国轮廓示意图、武汉中央枢纽仓、13 个区域分拨中心、干线流向、区域仓储分布、实时播报 |
| 中栏 | 实时物流动态 | 运单表格（单号 / 线路 / 承运商 / 货物 / 状态 / 预计到达） |
| 右栏 | 供应商绩效排名 TOP 8 | 排名条形图，前三名单独配色 |
| 右栏 | 运输方式与准时率 | 270° 仪表盘（综合准时率）+ 4 种运输方式占比 |
| 右栏 | 风险预警中心 | 预警等级统计 + 5 条分级预警（紧急 / 重要 / 一般） |

## 设计令牌（Figma Variables：`Dashboard Tokens`）

| 令牌 | 色值 | 用途 |
| --- | --- | --- |
| `bg/base` | `#040A18` | 页面背景 |
| `bg/elevated` | `#0A1932` | 卡片、轨道 |
| `bg/panel` | `#0B1E3C` | 面板 |
| `border/default` | `#1B4A7E` | 描边 |
| `border/strong` | `#2B7BC4` | 强调描边 |
| `accent/cyan` | `#22D3EE` | 主强调色 |
| `accent/blue` | `#3B82F6` | 数据系列 |
| `accent/green` | `#34D399` | 正向 / 正常 |
| `accent/amber` | `#FBBF24` | 枢纽 / 重要 |
| `accent/red` | `#F87171` | 紧急 / 异常 |
| `accent/purple` | `#A78BFA` | 数据系列 |
| `text/primary` | `#E6F1FF` | 主文字 |
| `text/secondary` | `#8BA3C7` | 次要文字 |
| `text/muted` | `#4F6A8F` | 辅助文字 |

另有 `space/panel` = 16、`radius/panel` = 4。

## 文字样式

| 样式 | 字体 | 字号 / 行高 |
| --- | --- | --- |
| Display/Screen Title | Noto Sans SC Bold | 34 / 44 |
| Panel/Title | Noto Sans SC Bold | 17 / 24 |
| Body/Medium | Noto Sans SC Medium | 14 / 20 |
| Body/Regular | Noto Sans SC Regular | 13 / 18 |
| Caption | Noto Sans SC Regular | 12 / 16 |
| Number/XL | Rajdhani Bold | 44 / 48 |
| Number/L | Rajdhani Bold | 30 / 34 |
| Number/M | Rajdhani SemiBold | 20 / 24 |
| Label/EN | Barlow Condensed Medium | 11 / 14 |

效果样式：`Glow/Cyan`；填充样式：`Gradient/Panel`。

## 组件

| 组件 | 文本属性 |
| --- | --- |
| `Panel/Header` | Title、Subtitle |
| `KPI/Card` | Label、Value、Unit、Trend |
| `Rank/Row` | Rank、Name、Value（条长度可调 `Bar Fill`） |
| `Alert/Item` | Level、Message、Time |
| `Legend/Item` | Label、Value |
| `Table/Header`、`Table/Row` | 单号、线路、承运商、货物、Status、预计到达 |
| `Deco/Corners` | 面板四角装饰，随实例尺寸拉伸 |

所有图表（柱状、折线、环形、仪表盘、地图节点）都是可编辑的矢量和文字图层；
屏幕上的数据均为示例数据。地图轮廓仅为示意，用于真实项目时请替换为标准地图底图。
