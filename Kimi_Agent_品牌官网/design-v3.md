# Landon 品牌官网设计文档 V3
## 参考: terminal-industries.com 风格

---

## 品牌基础

### 颜色
- **主色 (Foundation Blue)**: #0B2676
- **深色背景 (Deep Ocean)**: #040B35
- **荧光绿强调色**: #C8FF3D (类似 terminal-industries 的亮绿色)
- **浅蓝**: #B1E8FE
- **白色**: #FFFFFF
- **文字主色**: #1A1A2E
- **文字副色**: #6B7280

### 字体
- 主字体: Inter, system-ui, sans-serif
- 中文: 思源黑体

---

## 页面结构

### 1. 导航栏 (Pill Navigation)
- 胶囊形状，居中显示
- 毛玻璃效果: backdrop-filter: blur(20px)
- 背景: rgba(255,255,255,0.8)
- 包含: Logo | 解决方案 | 关于我们 | 联系我们 | EN/中文切换 | CTA按钮

### 2. Hero区域
- 全屏高度 (100vh)
- 背景: 日落/黄昏色调的智慧能源场景图
- 大标题: "深耕智慧能源" (打字机效果)
- 副标题: "Landing on Energy Intelligence"
- 底部: "SCROLL TO EXPLORE" 提示

### 3. Features区域 (左右分栏)
- 白色背景
- 网格线背景图案
- 三栏布局展示核心能力
- 每张卡片带编号 (01, 02, 03)

### 4. About区域 (深绿色背景)
- 深绿色背景 (#042520 类似 terminal-industries)
- 网格线效果
- 大字体标语
- 品牌Logo展示

### 5. Testimonials区域
- 客户评价引用
- 全屏背景图
- 引用文字居中

### 6. Contact区域
- 左右分栏
- 左侧: 联系选项列表
- 右侧: 联系表单

### 7. Footer
- 深绿色背景
- 多列链接布局
- 社交媒体图标

---

## 动画效果

### 打字机效果
```css
@keyframes typewriter {
  from { width: 0; }
  to { width: 100%; }
}
```

### 滚动触发动画
- 元素进入视口时淡入/滑入
- 使用 Intersection Observer

### 悬停效果
- 按钮: 背景色变化 + 轻微上移
- 卡片: 阴影加深 + 轻微上移

---

## 响应式设计

### 桌面端 (>1024px)
- 完整布局
- 左右分栏

### 平板端 (768-1024px)
- 简化布局
- 单列展示

### 移动端 (<768px)
- 单列布局
- 汉堡菜单
