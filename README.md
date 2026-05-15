# HuaFuture

国仕无双 · 期货研究智库 — HuaFuture Research Reports Portal

专业的 AI 期货分析平台，由华研究体系开发。

## 项目结构

```
HuaFuture/
├── Domestic/          ← 国内期货研究报告（如螺纹钢、玻璃等）
├── International/     ← 国际期货研究报告（如原油、黄金、LME 金属等）
├── build.js           ← 静态站点生成器
├── config.json        ← 站点配置
├── index.html         ← 门户首页（由 build.js 自动生成）
├── favicon.jpg        ← 网站图标
└── README.md
```

## 报告命名规范

将新报告放入 `Domestic/` 或 `International/` 目录下，文件名格式如下：

```
{品种}-{合约代码}-{报告类型}.html
```

**示例：**

| 目录 | 文件名 |
|------|--------|
| `Domestic/` | `螺纹钢-RB2610-深度分析.html` |
| `Domestic/` | `玻璃-FG2609-综合评级报告.html` |
| `International/` | `原油-SC2506-技术分析.html` |
| `International/` | `黄金-AU2512-基本面研究.html` |

报告类型包括：深度分析、技术分析、基本面研究、套利策略、期限结构、期现基差、综合评级、专题报告。

## 构建

```bash
node build.js
```

该命令将扫描 `Domestic/` 和 `International/` 目录下的所有 HTML 文件，提取元数据（标题、描述、日期），生成 `index.html` 门户首页，并为每份报告自动注入浮动的"返回首页"按钮。

## 技术栈

- Node.js 构建脚本
- Tailwind CSS 样式
- Noto Serif SC / Inter 字体
- 全静态部署（GitHub Pages / EdgeOne Pages 等均适用）

## 免责声明

本平台提供的期货研究报告仅供信息参考，不构成任何投资建议。期货交易风险较高，投资者应独立判断并自担风险。
