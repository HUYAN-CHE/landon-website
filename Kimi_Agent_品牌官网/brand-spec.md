# Landon Technology 品牌规范

## 品牌识别
- **公司名**: Landon Technology / 澜动科技
- **Slogan**: Making Energy Smarter / 让能源更智慧
- **成立**: 2017年
- **总部**: 苏州，研发中心：深圳光明

## 色彩系统（已验证）

### 主色
| Token | HEX | 用途 |
|-------|-----|------|
| `--ocean` | `#040B35` | 深色背景、Hero遮罩 |
| `--foundation` | `#0B2676` | 次级深色、渐变起点 |
| `--brand` | `#085CF0` | 主品牌色、CTA、高亮 |
| `--sky` | `#B1E8FE` | 辅助强调、标题点缀 |
| `--mist` | `#E5F7FD` | 浅色背景、Logo填充 |

### 中性色
| Token | 值 | 用途 |
|-------|-----|------|
| `--ink` | `#0a1628` | 主文字色（浅色背景） |
| `--ink-80` | `rgba(255,255,255,0.82)` | 深色背景主文字 |
| `--ink-60` | `rgba(255,255,255,0.58)` | 次要文字 |
| `--muted` | `rgba(255,255,255,0.40)` | 辅助信息 |
| `--dim` | `rgba(255,255,255,0.18)` | 分割线、边框 |
| `--hairline` | `rgba(255,255,255,0.12)` | 细边框 |

## 字体系统

### 字体栈
```css
--font-display: "Inter", -apple-system, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", sans-serif;
--font-body: "Inter", -apple-system, "PingFang SC", sans-serif;
--font-mono: "JetBrains Mono", "SF Mono", ui-monospace, monospace;
```

### 字号层级
| 层级 | 桌面端 | 移动端 | 字重 | 行高 | 用途 |
|------|--------|--------|------|------|------|
| Display | 72px | 40px | 500 | 1.1 | Hero主标题 |
| H1 | 56px | 32px | 500 | 1.15 | 区块标题 |
| H2 | 40px | 28px | 500 | 1.2 | 卡片标题 |
| H3 | 24px | 20px | 500 | 1.3 | 小标题 |
| Body | 18px | 16px | 400 | 1.7 | 正文 |
| Caption | 14px | 13px | 400 | 1.5 | 标签、辅助 |
| Overline | 13px | 12px | 500 | 1.4 | 区块标签（tracking-widest） |

## 间距系统
- 区块间距：128px（桌面）/ 80px（移动）
- 内容最大宽度：1280px
- 卡片内边距：32px
- 网格间距：24px

## 动画规范
- **缓动函数**: 
  - 入场：`cubic-bezier(0.16, 1, 0.3, 1)` (expo-out)
  - 平滑：`cubic-bezier(0.4, 0, 0.2, 1)`
- **时长**:
  - 微交互：200ms
  - 标准过渡：400ms
  - 入场动画：600ms
  - 打字机：120ms/字符
- **交错延迟**: 100ms 递增

## 反 AI Slop 检查清单
- ✅ 不使用紫渐变（当前是蓝调，符合）
- ✅ 不使用 emoji 图标（使用 Lucide SVG）
- ✅ 不使用 Inter 做 display（已规划）
- ✅ 使用 text-wrap: pretty
- ✅ 使用 CSS Grid 精确布局
- ✅ 精心选择字体搭配

## 资产清单
- Logo: SVG inline（已存在）
- 产品图: ./images/product-*.jpg/png（需优化质量）
- 客户Logo: ./images/client-*.png（需统一尺寸）
- Hero背景: ./images/hero-bg.jpg
