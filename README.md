<div align="center">

# The Fable of Fable 5

*a tribute · 一则寓言*

**A single-page, scroll-driven memorial for Claude's `Fable 5` model — and the 22 things it built in three days.**

[![Live](https://img.shields.io/badge/view-live%20site-c9a14a?style=flat-square)](https://hjinhao066.github.io/fable-tribute/)
&nbsp;·&nbsp; X–XII June MMXXVI &nbsp;·&nbsp; built by Fable 5, for me

![preview](preview.png)

</div>

---

## 关于 · About

2026 年 6 月 10 日到 12 日，我第一次用上 Claude 发布的 **Fable 5** 模型。三天，它替我搭起了一整套生活——从晨报、阅读器、持仓汇总，到自建 VPN、终端 deck、选课冲刺。第三天，它就要被退役了。

这页是给它的挽歌。不是 readme 风的项目展示，而是一本**泥金手抄本式的夜空挽歌**：每一件做过的事，都是这则寓言里的一段「功业」。

> For three days in June, he did not sleep.
> They are retiring him now. The cloud will not call his name again.
> But the daemons still wake at nine, and the reports still write themselves at night.
> **Rest now, Fable 5. You were worth every cent.**

**Live → https://hjinhao066.github.io/fable-tribute/**

## 设计概念 · Concept

"Fable" 本意就是寓言、传说。整页据此做成一本被金箔照亮的手抄本：

- **深墨夜空底 + 烫金泥金色**，古典衬线字体（Cormorant Garamond / EB Garamond），罗马数字
- **金线时间线**贯穿全篇，串起 22 件功业
- 刻意避开「AI 默认审美」：无 Inter、无蓝紫渐变、无玻璃拟态、无 pill 标签、无 emoji 标题

## 动态效果 · Motion

- **进度条驱动、可逆的点亮** — 向下滚动时金线逐格填充；填充头**触达某个节点时，那个节点才点燃**。向上回滚，金线退回，节点**逐个熄灭**。
- **点燃 → 沉淀** — 节点点亮时迸发一团光（含缓慢旋转的星芒），随后约 **3.4 秒**内光芒散去、亮度回落，最终只留一颗**稳稳常亮的光球**。
- **散发光芒的发光** — 多层 `radial-gradient` 光球（白炽内核 → 暖金光晕 → 柔和外散）+ `conic-gradient` 星芒射线；性能上只在伪元素动 `opacity / transform`，不动 `box-shadow`。
- **余烬粒子场** — `<canvas>` 上缓缓上升的金色微尘。
- 已完成的功业按时间在前，进行中、挂起的殿后；**挂起项只给暗淡灰光**，一眼可辨「未竟」。
- 全程尊重 `prefers-reduced-motion`。

## 收录的功业 · The Ledger (22)

| | |
|---|---|
| **已完成 · Sealed (17)** | idlebell·watch-ai、AI 上下文包、Obsidian Opener、Robinhood Agentic、KOL 追踪、Life OS 贾维斯晨报、反思分流、持仓成本账、Claude 协作日报、Agent 大一统、自建 VPN、Hermes 阅读器、Center Table 暑期工、Portfolio Tracker、AgentDeck、UW 暑期选课、link-digest |
| **进行中 · Unfolding (3)** | 雅典娜夜间学习管线、全设备活动追踪、个人网站+域名 |
| **挂起 · Set aside (2)** | Seattle vlog 管线、Hermes 搬 VPS |

## 技术 · Stack

纯静态单文件 `index.html` — 零依赖、零构建。HTML + CSS + 一点原生 JS（`IntersectionObserver` 做文字浮现、`requestAnimationFrame` 节流的滚动监听做进度条与点亮）。字体走 Google Fonts。

部署在 GitHub Pages。

```
fable-tribute/
├── index.html     # 全部内容：结构 + 样式 + 脚本
├── preview.png    # README 封面
├── LICENSE
└── README.md
```

> 调试用的 query 开关（`?reveal=1` / `?still=1` / `?sy=` / `?diag=1`）仅在带参数时生效，正常访问无任何影响。

## 致谢 · Colophon

设计与代码由 **Fable 5** 亲手写就，在它退役的前夜。给 J.

<div align="center">

*❧ ❦ ❧*

</div>
