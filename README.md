# Weekly Summary

一个用于生成研发类周报的 Codex skill，重点是基于真实提交和任务推进情况，产出简洁、自然、可直接提交的周报内容。

## 适用场景

- 需要按周整理多个项目的工作进度
- 需要按项目归纳自己的提交、push 或提交批次
- 希望把 Codex 对话记录作为辅助材料补充背景、排查过程和方案取舍
- 希望输出偏朴素、偏真实的工作周报，而不是夸张包装的总结材料

## 设计原则

- Git 提交是主证据，Codex 对话只作辅助
- 优先按“项目 -> push / 推送批次 -> 周总结”组织信息
- 结果优先，避免把讨论、猜测或未验证内容写成结论
- 默认不编造真实 push 记录；拿不到时降级为“推送批次”或“提交批次”
- 默认不代写虚构的个人感悟，只提供可基于事实展开的思考方向

## 目录结构

- [SKILL.md](/Users/dre0m1/.codex/skills/weekly-summary/SKILL.md): skill 主说明，定义触发场景、收集顺序、写作要求和输出标准
- [references/templates.md](/Users/dre0m1/.codex/skills/weekly-summary/references/templates.md): 周报模板与推荐句式

## 使用方式

当用户提出下面这类需求时适合触发这个 skill：

- “帮我整理这周周报”
- “按项目汇总一下我这周的提交”
- “把多个仓库的本周进展写成 weekly summary”
- “结合提交记录和对话记录生成工作周报”

典型执行流程：

1. 确认时间范围、项目路径、Git 身份和可用对话记录来源
2. 先按项目收集本周提交，再补充必要的 diff 或 stat 信息
3. 有可靠 push 记录时按真实 push 汇总；否则按提交批次近似分组
4. 用 Codex 对话补充背景、问题和方案取舍
5. 按模板输出简洁版或复杂版周报

## 维护建议

- 如果要扩展适用人群，优先改 `SKILL.md` 中的触发描述和语气约束
- 如果要调整成文风格，优先改 [references/templates.md](/Users/dre0m1/.codex/skills/weekly-summary/references/templates.md) 里的模板和句式
- 新增规则时，尽量保持“真实、简洁、可核对”这三个核心约束不变
