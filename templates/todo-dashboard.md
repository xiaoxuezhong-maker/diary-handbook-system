# 待办事项总览

这个页面用于集中查看分散在每日笔记、月度任务池和主题笔记里的 Markdown 待办。

它不是把原始待办复制到这里，而是用插件查询显示。这样不会出现同一个任务在两个地方状态不一致的问题。

## 使用前提

- 手动写待办：不需要插件
- 自动显示跨页面待办：需要安装 Tasks 或 Dataview
- 同步到 Microsoft To Do：需要额外脚本，公开模板不包含真实同步脚本

## Tasks 查询

安装并启用 Tasks 插件后，可以使用下面的查询。

```tasks
not done
path includes 01-日常手账
sort by path
sort by due
```

## Dataview 查询

安装并启用 Dataview 插件后，可以使用下面的查询。

```dataview
TASK
FROM "01-日常手账"
WHERE !completed
SORT file.path ASC
```

## 月度任务池检查

把月份改成你要检查的月份。

```dataview
TASK
FROM "01-日常手账"
WHERE !completed AND contains(file.path, "2026-06")
SORT file.path ASC
```

## 手动整理区

如果暂时不装插件，也可以在这里手动整理重要待办。

### 本周必须处理

- [ ] 

### 等待别人/等待条件

- [ ] 

### 暂缓

- [ ] 
