# 开玉模拟器 - Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 创建网页开玉模拟器，还原开玉魄体验

**Architecture:** 单HTML文件，内嵌CSS和JS，玉类型和属性数据从Excel提取内嵌

**Tech Stack:** 纯HTML/CSS/JS

---

## Task 1: 创建HTML基础结构和样式

**Files:**
- Create: `jade-simulator/index.html`

**Steps:**

- [ ] 创建HTML基本结构
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>上古玉魄模拟器</title>
    <style>/* CSS代码 */</style>
</head>
<body>
    <div class="container">
        <header><h1>上古玉魄模拟器</h1></header>
        <div class="main-content">
            <div class="control-panel">...</div>
            <div class="stats-panel">...</div>
        </div>
        <div class="results" id="results"></div>
    </div>
    <script>/* JS代码 */</script>
</body>
</html>
```

- [ ] 实现CSS样式（古典玄幻风格）

- [ ] 保存文件

---

## Task 2: 嵌入玉魄数据

**Files:**
- Modify: `jade-simulator/index.html` (添加JS数据)

**Steps:**

- [ ] 从Python输出的JSON数据中提取yangyu和yinyu数组

- [ ] 将数据内嵌到HTML的JS变量中

- [ ] 确保数据格式正确（概率和价格）

---

## Task 3: 实现开玉核心逻辑

**Files:**
- Modify: `jade-simulator/index.html`

**Steps:**

- [ ] 实现 `openJade()` 函数
```javascript
function openJade() {
    // 50%阳玉 50%阴玉
    const jadeType = Math.random() < 0.5 ? 'yangyu' : 'yinyu';
    // 根据概率分布随机选择属性组合
    const result = selectByProbability(jadeType);
    return result;
}
```

- [ ] 实现 `selectByProbability(jadeType)` - 根据概率选择

- [ ] 实现批量开玉 `openJadesBatch(count)`

- [ ] 实现统计计算和UI更新

---

## Task 4: 实现动画和交互

**Files:**
- Modify: `jade-simulator/index.html`

**Steps:**

- [ ] 实现玉牌卡片的创建和动画效果

- [ ] 实现开1块玉的动画展示

- [ ] 实现批量开玉的结果批量展示

- [ ] 实现统计面板的数字动画

---

## Task 5: 验证和测试

**Steps:**

- [ ] 在浏览器中打开测试

- [ ] 测试开1块玉功能

- [ ] 测试批量开玉功能

- [ ] 验证统计计算正确性
