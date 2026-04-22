---
title: 博客更新语法参考（永远草稿）
pubDate: 2026-04-21
description: 特殊Markdown语法
category: 指南
image: ""
draft: true
slugId: blog/reference
---

# 博客更新语法参考（永远草稿）

> 这是一篇永远不发布的草稿，用来快速查看 Momo 博客常用语法。  
> 每次写博客前打开这篇即可。

---

## 0. Frontmatter 模板

```yaml
---
title: 文章标题
pubDate: 2026-04-21
description: 一句话简介
category: 分类
image: ""
draft: true
slugId: blog/reference
---
```

### 字段说明

- `title`：文章标题
- `pubDate`：发布日期
- `description`：摘要
- `category`：分类
- `image`：封面图路径，可留空
- `draft`：是否为草稿
- `slugId`：路由标识，建议短、稳定、不要随便改

> 注意：Momo 常用的是 `pubDate` 和 `slugId`，不要误写成 `date` / `slug`

---

## 1. 标题

```markdown
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
```

---

## 2. 段落、强调与分隔线

### 普通段落

```markdown
这是第一段。

这是第二段。
```

### 粗体、斜体、删除线

```markdown
**粗体**
*斜体*
***粗斜体***
~~删除线~~
```

示例：**粗体** / *斜体* / ***粗斜体*** / ~~删除线~~

### 分隔线

```markdown
---
```

---

## 3. 列表

### 无序列表

```markdown
- 项目 A
- 项目 B
  - 子项目 B1
  - 子项目 B2
```

### 有序列表

```markdown
1. 第一步
2. 第二步
3. 第三步
```

### 任务列表

```markdown
- [x] 已完成
- [ ] 未完成
```

---

## 4. 引用与代码

### 普通引用

```markdown
> 这是一段引用
```

### 行内代码

```markdown
使用 `git status` 查看状态
```

### 代码块

````markdown
```bash
git add .
git commit -m "docs: update post"
git push
```
`````

```bash
git add .
git commit -m "docs: update post"
git push
```

---

## 5. 链接

### 普通链接

```markdown
[我的主页](https://timelyr1c.com)
[我的博客](https://blog.timelyr1c.com)
```

### 站内链接（推荐）

```markdown
[返回首页](/)
[另一篇文章](/blog/purpose/)
```

> 站内跳转优先写站内路径，不建议写完整绝对链接。

---

## 6. 图片

### 当前文章目录下的图片

```markdown
![封面](./cover.jpg)
```

### 外链图片

```markdown
![示意图](https://example.com/demo.png)
```

> 图片删掉后，记得同步删掉 Markdown 中的引用，否则会报 `Image not found`

---

## 7. 表格

```markdown
| 时间 | 记录 |
| --- | --- |
| 2026.04.21 | 博客以 Momo 主题在 Cloudflare Pages 上部署并上线 |
| 2026.04.22 | 增加主页并完成双站结构 |
```

> 一定要用英文半角竖线 `|`，不要用中文全角 `｜`

---

## 8. 数学公式（KaTeX）

### 行内公式

```markdown
爱因斯坦公式：$E = mc^2$
```

示例：爱因斯坦公式：$E = mc^2$

### 块级公式

```markdown
$$
\int_a^b f(x)\,dx
$$
```

$$
\int_a^b f(x),dx
$$

---

## 9. 引用卡片测试

### 普通文本

```markdown
:::quote

宇宙就是一座黑暗森林，每个文明都是带枪的猎人，像幽灵般潜行于林间，轻轻拨开挡路的树枝，竭力不让脚步发出一点儿声音，连呼吸都必须小心翼翼：他必须小心，因为林中到处都有与他一样潜行的猎人，如果他发现了别的生命，能做的只有一件事：开枪消灭之。

<br><right>——《三体 II：黑暗森林》</right>
:::
```

### 数学公式

```markdown
:::quote
$E = mc^2$
:::
```

---

## 10. 卡片测试

### 音乐卡片（网易云）

```markdown
::music{id="30431366"}
```

> 当前 Momo 音乐卡片使用的是网易云歌曲 ID。

### GitHub 卡片

```markdown
::github{repo="Motues/Momo"}
```

---

## 11. 特殊样式语法

### 模糊效果

```markdown
这是一个!!模糊!!效果。
```

这是一个!!模糊!!效果。

说明：

```markdown
对于桌面端，鼠标移入时，会移除模糊效果，点击后会保持3秒清晰显示；对于移动设备，点击后移除模糊效果，当同时满足点击后超过3秒和页面滑动才会变为模糊状态。
```

对于桌面端，鼠标移入时，会移除模糊效果，点击后会保持3秒清晰显示；对于移动设备，点击后移除模糊效果，当同时满足点击后超过3秒和页面滑动才会变为模糊状态。

---

### 拼音

```markdown
下面的词会显示拼音：

{拼音}(pīn|yīn)，{君の名は}(きみ||な|)
```

下面的词会显示拼音：

{拼音}(pīn|yīn)，{君の名は}(きみ||な|)

---

### 彩虹文字

```markdown
这是一个==彩虹==文字效果。
```

这是一个==彩虹==文字效果。

---

### 嵌套效果

```markdown
这是一个!!==模糊并且带{拼音}(pīn|yīn)的{彩虹}(cǎi|hóng)==!!
```

这是一个!!==模糊并且带{拼音}(pīn|yīn)的{彩虹}(cǎi|hóng)==!!

---

## 12. Typst 测试

基于 [Typst.ts](https://myriad-dreamin.github.io/typst.ts/) 实现的 Typst 渲染。

图片在黑暗模式情况的效果可能不是很好。

### 基础示例

````markdown
```typst
#set page(width: auto, height: auto, margin: 10pt)
#set text(fill: rgb("#2f61eb"), size: 20pt)

$ cal(A) = pi r^2 $

Hello from *Typst*!
```
````

```typst
#set page(width: auto, height: auto, margin: 10pt)
#set text(fill: rgb("#2f61eb"), size: 20pt)

$ cal(A) = pi r^2 $

Hello from *Typst*!
```

### Waves 示例

````markdown
```typst *Waves
// Code from https://github.com/typst/packages/blob/main/packages/preview/cetz/0.4.2/gallery/waves.typ
#import "@preview/cetz:0.4.2": canvas, draw, vector, matrix

#set page(width: auto, height: auto, margin: .5cm)

#canvas({
  import draw: *

  ortho(y: -30deg, x: 30deg, {
    on-xz({
      grid((0,-2), (8,2), stroke: gray + .5pt)
    })

    // Draw a sine wave on the xy plane
    let wave(amplitude: 1, fill: none, phases: 2, scale: 8, samples: 100) = {
      line(..(for x in range(0, samples + 1) {
        let x = x / samples
        let p = (2 * phases * calc.pi) * x
        ((x * scale, calc.sin(p) * amplitude),)
      }), fill: fill)

      let subdivs = 8
      for phase in range(0, phases) {
        let x = phase / phases
        for div in range(1, subdivs + 1) {
          let p = 2 * calc.pi * (div / subdivs)
          let y = calc.sin(p) * amplitude
          let x = x * scale + div / subdivs * scale / phases
          line((x, 0), (x, y), stroke: rgb(0, 0, 0, 150) + .5pt)
        }
      }
    }

    on-xy({
      wave(amplitude: 1.6, fill: rgb(84, 219, 219, 80))
    })
    on-xz({
      wave(amplitude: 1, fill: rgb(216, 219, 90, 80))
    })
  })
})
```
````

```typst *Waves
// Code from https://github.com/typst/packages/blob/main/packages/preview/cetz/0.4.2/gallery/waves.typ
#import "@preview/cetz:0.4.2": canvas, draw, vector, matrix

#set page(width: auto, height: auto, margin: .5cm)

#canvas({
  import draw: *

  ortho(y: -30deg, x: 30deg, {
    on-xz({
      grid((0,-2), (8,2), stroke: gray + .5pt)
    })

    // Draw a sine wave on the xy plane
    let wave(amplitude: 1, fill: none, phases: 2, scale: 8, samples: 100) = {
      line(..(for x in range(0, samples + 1) {
        let x = x / samples
        let p = (2 * phases * calc.pi) * x
        ((x * scale, calc.sin(p) * amplitude),)
      }), fill: fill)

      let subdivs = 8
      for phase in range(0, phases) {
        let x = phase / phases
        for div in range(1, subdivs + 1) {
          let p = 2 * calc.pi * (div / subdivs)
          let y = calc.sin(p) * amplitude
          let x = x * scale + div / subdivs * scale / phases
          line((x, 0), (x, y), stroke: rgb(0, 0, 0, 150) + .5pt)
        }
      }
    }

    on-xy({
      wave(amplitude: 1.6, fill: rgb(84, 219, 219, 80))
    })
    on-xz({
      wave(amplitude: 1, fill: rgb(216, 219, 90, 80))
    })
  })
})
```

---

## 13. Alert 组件测试

Momo 支持：

* `note`
* `tip`
* `important`
* `warning`
* `caution`

### 单行内容测试

```markdown
:::note
这是一个提示。
:::

:::tip
这是一个建议。
:::

:::important
这是一个重要事项。
:::

:::warning
这是一个警告。
:::

:::caution
这是一个危险事项。
:::
```

---

### 多行内容测试

```markdown
:::tip
这是一个包含多行内容的提示框。

- 支持列表项
- 可以包含多个段落

**重点内容**：还可以包含粗体文字和其他 Markdown 元素。
:::
```

---

### 嵌套内容测试

````markdown
:::warning
提示框内可以包含代码块等其他元素。

```javascript
console.log('Hello World');
```
:::
````

---

### 自定义标题测试

```markdown
:::important[自定义标题]
这是一个带有自定义标题的提示框。标题会显示为“自定义标题”而不是默认的“IMPORTANT”。
:::
```

---

## 14. 常用写作速查

### 站内跳转

```markdown
[上一篇](/blog/purpose/)
[主页](https://timelyr1c.com)
[博客首页](https://blog.timelyr1c.com)
```

### 命令记录

```bash
git pull --rebase origin main
git add .
git commit -m "docs: update blog post"
git push
```

### 更新日志表格模板

```markdown
| 时间 | 记录 |
| --- | --- |
| 2026.04.21 | 博客以 Momo 主题在 Cloudflare Pages 上部署并上线 |
| 2026.04.22 | 增加主页并完成双站结构 |
```

---

## 15. 常见坑

* 表格必须用英文半角 `|`
* `pubDate` / `slugId` 不要写错
* 图片删掉后要同步删引用
* 站内链接尽量用 `/blog/xxx/`
* `draft: true` 时不会进入正式文章列表
* 删除内容后如果报旧图片错误，先检查引用，再清 `.astro` 缓存

---

## 16. 发布前检查清单

```markdown
- [ ] frontmatter 正确
- [ ] 标题正确
- [ ] slugId 稳定
- [ ] 图片路径正确
- [ ] 站内链接可点
- [ ] 表格使用半角 |
- [ ] draft 设置正确
- [ ] 本地 `pnpm dev` 正常
- [ ] 本地 `pnpm build` 正常
```

* [ ] frontmatter 正确
* [ ] 标题正确
* [ ] slugId 稳定
* [ ] 图片路径正确
* [ ] 站内链接可点
* [ ] 表格使用半角 |
* [ ] draft 设置正确
* [ ] 本地 `pnpm dev` 正常
* [ ] 本地 `pnpm build` 正常

---

## 17. 说明

这篇文章永远只做草稿，不发布。
每次写博客前打开它，作为速查笔记使用。
