# 知识库使用说明

## 目录结构

知识导图图片存放在：
```
love02-master/assets/images/knowledge/
```

## 如何添加新的知识导图

### 第一步：准备图片

将你的知识导图图片放入 `assets/images/knowledge/` 目录，命名建议：
- 使用英文小写
- 用连字符分隔单词
- 例如：`product-mvp.png`、`user-research.png`

### 第二步：在知识库页面添加内容

打开 `_pages/knowledge.md`，按以下格式添加：

#### 1. 添加新书签分类（如需要）

在 `.knowledge-container` 区域内添加：

```html
<div class="category-bookmark product" onclick="showCategory('new-category')">
  <div class="bookmark-icon">🎯</div>
  <div class="bookmark-title">新分类名称</div>
  <div class="bookmark-count">X 个知识导图</div>
</div>
```

#### 2. 添加对应的导图展示区域

```html
<div id="new-category" class="map-gallery">
  <h2 class="map-gallery-title">🎯 新分类名称</h2>
  <div class="map-grid">

    <div class="map-item">
      <img src="/assets/images/knowledge/your-image.png" alt="导图名称" onclick="openModal(this.src)">
      <div class="map-item-title">导图名称</div>
    </div>

  </div>
</div>
```

### 第三步：更新数量

记得更新书签上的数量显示。

## 书签颜色说明

已预设4种颜色样式，可通过修改 `class` 切换：

| 样式类 | 颜色 | 适合分类 |
|--------|------|----------|
| `product` | 绿色渐变 | 产品、方法论 |
| `ai` | 紫色渐变 | AI、技术 |
| `data` | 粉色渐变 | 数据、分析 |
| `career` | 蓝色渐变 | 职业、成长 |

## 当前示例结构

| 分类 | 文件夹位置 | 示例图片 |
|------|-----------|----------|
| 产品方法论 | knowledge/ | product-mvp.png, user-research.png, prd-structure.png |
| AI技术 | knowledge/ | rag-architecture.png, mcp-protocol.png |
| 数据分析 | knowledge/ | ab-test.png, metrics-design.png |
| 职业成长 | knowledge/ | pm-growth.png |

## 图片格式建议

- **格式**：PNG 或 JPG
- **尺寸**：建议宽度 800-1200px
- **比例**：横向长方形（适合思维导图展示）

## 替换示例图片

你只需要：
1. 将你的知识导图图片放入 `assets/images/knowledge/` 目录
2. 修改 `_pages/knowledge.md` 中的图片文件名和标题
3. 更新分类和数量

非常简单！
