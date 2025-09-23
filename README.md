<img src="https://yoran-images-1256970527.cos.ap-guangzhou.myqcloud.com/20250923175145651.png"/>

# Blue Topaz Yoran 主题修改说明

## 主题基本信息
- **主题名称**: Blue Topaz Yoran
- **基于版本**: Blue Topaz v1.5.0
- **修改者**: Yoran
- **原作者**: WhyI & Pkmer
- **版本**: 1.0.0

## 主要修改内容

### 1. 光标样式增强
在文件末尾添加了自定义光标样式，包括：
- **光标发光效果**: 添加了 `cursor-glow-large` 动画，实现光标的发光脉冲效果
- **动画关键帧**: 0%-100% 为基础发光，50% 为最强发光状态
- **颜色**: 使用主题的 `--interactive-accent` 颜色变量

```css
@keyframes cursor-glow-large {
  0%, 100% {
    box-shadow: 0 0 6px var(--interactive-accent);
  }
  50% {
    box-shadow: 0 0 12px var(--interactive-accent), 0 0 18px var(--interactive-accent);
  }
}
```

### 2. 文件夹彩色边框系统
为第一层文件夹添加了15种不同的彩色左边框：

#### 选择器规则
- **目标元素**: `.tree-item.nav-folder:not(.tree-item-children *):nth-child(n)`
- **应用范围**: 仅第一层文件夹（父级不包含 `.tree-item-children`）
- **边框样式**: 6px 实线左边框

#### 配色方案（现代流行色）
1. **青绿色 (Teal)**: `#4ECDC4`
2. **珊瑚红 (Coral Red)**: `#FF6B6B`
3. **天空蓝 (Sky Blue)**: `#45B7D1`
4. **薄荷绿 (Mint Green)**: `#96CEB4`
5. **香草黄 (Vanilla Yellow)**: `#FFEAA7`
6. **梅花紫 (Plum Purple)**: `#DDA0DD`
7. **海泡石绿 (Seafoam)**: `#98D8C8`
8. **金丝雀黄 (Canary Yellow)**: `#F7DC6F`
9. **薰衣草紫 (Lavender)**: `#BB8FCE`
10. **婴儿蓝 (Baby Blue)**: `#85C1E9`
11. **桃子橙 (Peach Orange)**: `#F8C471`
12. **翡翠绿 (Emerald Green)**: `#82E0AA`
13. **玫瑰金 (Rose Gold)**: `#F1948A`
14. **石墨灰 (Graphite Gray)**: `#85929E`
15. **丁香紫 (Lilac)**: `#D7BDE2`

### 3. 布局调整
修改了导航按钮容器的对齐方式：
```css
.nav-buttons-container, .view-actions, .workspace-tab-header-inner, .side-dock-settings, .side-dock-actions {
  justify-content: start !important;
}
```

### 4. 个人定制注释
在代码中添加了个人标识注释：
```css
/*比上面那个还菜鸟的人做的一些修改*/
```

## 技术特点

### CSS 选择器优化
- 使用 `:not(.tree-item-children *)` 精确选择第一层文件夹
- 通过 `:nth-child()` 伪类为不同位置的文件夹分配不同颜色
- 避免影响嵌套文件夹的样式

### 视觉设计理念
- **现代化配色**: 选择了当前流行的UI设计颜色
- **视觉层次**: 通过颜色区分不同文件夹，提高识别度
- **用户体验**: 保持原主题的整体风格，仅在关键位置添加个性化元素

## 兼容性说明
- 基于 Blue Topaz v1.5.0 开发
- 兼容 Obsidian 最新版本
- 保持原主题的所有功能和设置选项
- 新增功能不影响原有样式系统

## 使用建议
1. **文件夹组织**: 建议将重要的文件夹放在前15个位置以获得彩色标识
2. **主题设置**: 可以通过原 Blue Topaz 的设置面板调整其他样式选项
3. **个性化**: 可以根据个人喜好修改颜色值

## 更新日志
- **v1.0.0**: 初始版本，添加光标发光效果和文件夹彩色边框系统

