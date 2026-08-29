# AI 项目开发最佳实践

这个仓库用来收拾、验证和复用 AI 项目开发的实践细则。

## 目录

- [`prompts/`](prompts/) 提示词模板与约束 — [任务简报模板](prompts/task-brief.md)
- [`evals/`](evals/) 评估集、回归集、失败案例 — [评估用例模板](evals/case-template.md)
- [`agents/`](agents/) Agent 角色、工具与交付规范 — [角色规范模板](agents/role-spec.md)
- [`workflows/`](workflows/) 开发流程（计划 → 实现 → 审查 → 发布） — [计划-实现-审查](workflows/plan-build-review.md)
- [`examples/`](examples/) 可复制的示例项目

## 基线原则

1. **可验证**：每条实践要有对应的评估或失败案例。
2. **可复用**：写成模板，不写成经验贴。
3. **可回滚**：改提示、改模型、改工具都要能对比效果。
4. **人在环里**：发布、删除、外部发消默认需要人确认。
