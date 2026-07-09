目标文件：

【填写 HTML 路径】

请先阅读以下设计系统文件：

* `/Users/yin/pto-design-system/SKILL.md`
* `/Users/yin/pto-design-system/references/DESIGN.md`
* `/Users/yin/pto-design-system/references/quick-reference.md`
* `/Users/yin/pto-design-system/references/retrofit-container-audit.md`
* `/Users/yin/pto-design-system/patterns/patterns.json`

然后阅读目标 HTML。请先不要修改代码。

## 一、先输出迁移方案

请先输出一个简短迁移方案，包含：

1. 当前页面是什么结构，是否是完整业务工具 / demo 页面，还是单页展示页面
2. 应该映射到哪些 PTO tokens / classes / patterns
3. 是否需要迁移到 `patterns/ide-frame`
4. 是否需要使用 `patterns/workbench-shell`
5. graph / timeline / memory architecture / playback 等复杂视图是否已有对应 pattern，是否可以复用
6. 要删除哪些旧视觉，包括硬编码颜色、私有按钮、私有卡片、渐变背景、border-left、过重阴影、inset shadow、伪元素竖条、侧向渐变等
7. 哪些业务内容、交互意图和数据结构必须保留
8. 哪些地方超出现有 Design System，需要我确认后再处理

在我确认迁移方案之前，不要修改 HTML / CSS / JS。

## 二、迁移规则

迁移时请遵守：

1. 保留原业务内容和交互意图，只刷新为 PTO 风格。
2. 完整业务工具 / demo 页面优先迁移到 `patterns/ide-frame`。
3. 多分屏页面使用 `patterns/workbench-shell`。
4. graph / timeline / memory architecture / playback 等复杂视图必须优先使用对应 pattern，不要本地重画。
5. 页面运行时引用 `/Users/yin/pto/vendor/pto-design-system/...`，不要复制设计系统文件。
6. 按钮使用 `.btn` / `.btn-solid` / `.btn-ghost` / `.btn-icon`。
7. 颜色、间距、圆角、阴影、字体使用 Design System token，不要硬编码。
8. 不要新增私有 button / card / panel / badge / toolbar / page shell 视觉系统。
9. 删除旧的 border-heavy card、左侧高亮条、inset shadow、伪元素竖条、侧向渐变、过重投影和装饰性渐变。
10. 如果 Design System 没有覆盖某个组件，先说明缺口和最小补充方案，不要直接发明新样式。

## 三、实现阶段

等我确认迁移方案后，再开始修改目标 HTML / CSS / JS。

完成后请：

1. 启动本地预览服务。
2. 给出可访问 URL。
