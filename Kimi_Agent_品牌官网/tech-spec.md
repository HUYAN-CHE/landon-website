# LandingOnEnergy 技术规格文档

## 项目架构

### 技术栈
- **框架**: React 18 + TypeScript
- **构建工具**: Vite
- **样式**: Tailwind CSS
- **UI组件**: shadcn/ui
- **动画**: GSAP + ScrollTrigger
- **图标**: Lucide React

### 项目结构
```
app/
├── src/
│   ├── sections/          # 页面区域组件
│   │   ├── Hero.tsx       # 主视觉区
│   │   ├── Features.tsx   # 功能区域
│   │   ├── About.tsx      # 关于我们
│   │   └── Footer.tsx     # 页脚
│   ├── components/        # 可复用组件
│   │   ├── Button.tsx     # 按钮组件
│   │   ├── FeatureCard.tsx # 功能卡片
│   │   ├── ParticleField.tsx # 粒子背景
│   │   └── FeishuChat.tsx  # 飞书客服
│   ├── hooks/             # 自定义Hooks
│   │   └── useScrollAnimation.ts
│   ├── styles/            # 样式文件
│   │   └── animations.css
│   ├── App.tsx
│   └── main.tsx
├── public/                # 静态资源
│   └── images/
├── index.html
├── tailwind.config.js
└── package.json
```

## 组件清单

### shadcn/ui 组件
- Button - 按钮组件
- Card - 卡片容器

### 自定义组件
1. **ParticleField** - 粒子背景效果
2. **FeatureCard** - 3D功能卡片
3. **FeishuChat** - 飞书客服浮窗
4. **AnimatedText** - 文字动画组件

## 动画实现方案

| 动画效果 | 实现库 | 实现方式 | 复杂度 |
|---------|--------|---------|--------|
| 粒子背景 | CSS + Canvas | Canvas绘制粒子，CSS定位 | 中 |
| 文字交错入场 | GSAP | SplitText + stagger | 中 |
| 3D卡片翻转 | CSS 3D | transform-style: preserve-3d | 中 |
| 视差滚动 | GSAP ScrollTrigger | scrub模式 | 中 |
| 按钮悬停 | CSS | transition + transform | 低 |
| 图标旋转 | CSS | @keyframes rotate | 低 |
| 渐变流动 | CSS | @keyframes background-position | 低 |
| 滚动展现 | GSAP ScrollTrigger | toggle actions | 中 |

## 颜色配置

### Tailwind 自定义颜色
```javascript
colors: {
  'ocean': '#040B35',
  'foundation': '#0B2676',
  'primary': '#085CF0',
  'sky': '#B1E8FE',
  'mist': '#E5F7FD',
}
```

## 依赖安装

```bash
# 动画库
npm install gsap @gsap/react

# 图标
npm install lucide-react
```

## 飞书客服集成

### 实现方案
使用飞书开放平台提供的客服SDK，通过iframe或JS SDK方式嵌入。

### 配置参数
- 企业ID: 需用户配置
- 客服窗口位置: 右下角
- 触发方式: 点击浮窗

## 性能优化

1. **图片优化**
   - 使用WebP格式
   - 懒加载非首屏图片
   - 适当压缩

2. **动画优化**
   - 使用transform和opacity
   - 添加will-change
   - 支持prefers-reduced-motion

3. **代码优化**
   - 组件懒加载
   - Tree shaking
   - 代码分割

## 响应式断点

```javascript
screens: {
  'sm': '640px',
  'md': '768px',
  'lg': '992px',
  'xl': '1280px',
  '2xl': '1536px',
}
```

## 浏览器兼容

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
