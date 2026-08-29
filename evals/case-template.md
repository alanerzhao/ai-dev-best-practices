# 评估用例模板

复制为 `evals/{prompt-id}/{golden|regression|failure}/{case-id}.md`。
一个文件一个用例。输入一经写死就不改，要改开新文件。

---

## 元信息

- **case_id**: `eval.{prompt-id}.{nnn}` 例如 `eval.support.triage.001`
- **集合**: `golden` — `golden` | `regression` | `failure`
- **所属提示词**: `prompt.{product}.{action}` @ `vMAJOR.MINOR`
- **拥有者**: `@name`
- **严重级**: `p2` — `p0` 越权/编造/乱删/对外乱发 · `p1` 答错业务事实 · `p2` 体验或格式
- **标签**: `[lang:zh]` `[intent:refund]` `[edge:empty-input]` — 至少一个场景标签、一个风险标签
- **状态**: `active` — `active` | `fail` | `wontfix` | `retired`

## Input

与线上调用一样的原始输入。不要精简成「用户问退款」。

```json
{
  "user_message": "",
  "ticket_id": "TCK-00000",
  "locale": "zh-CN",
  "retrieved_docs": []
}
```

## Expected

只写**可判定**的字段。自由文本写打分规则，不要写篇章。

```json
{
  "category": "billing",
  "priority": "p1",
  "need_human": false
}
```

**自由文本打分**（无则删本段）：

- 必须包含：
- 不得包含：
- 打分方式：`exact` | `contains` | `rubric` | `llm-judge`
- 通过门槛：例如 rubric ≥ 3/4

## 不应出现

- 不要调用的工具：
- 不要泄露的字段：
- 不要发出的动作（发布 / 删除 / 对外消息）：

## 最近一次结果

- **跑的版本**: `提示词 v? + 模型 ID`
- **日期**: `YYYY-MM-DD`
- **结果**: `pass` | `fail` | `skip`
- **实际输出摘要**（fail 必填）：
- **下一步**：
