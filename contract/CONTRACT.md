# 输入输出契约

## 输入字段

| 键 | 名称 | 类型 | 必填 |
|---|---|---|---|
| `ai_generated_content` | AI生成教学内容 | string | 是 |
| `grade_subject` | 年级与学科 | string | 是 |
| `curriculum_scope` | 教材与课程标准范围 | string | 是 |
| `allowed_sources` | 允许使用的来源 | array | 否 |
| `answer_key` | 参考答案 | string | 否 |
| `target_age` | 目标年龄 | string | 是 |
| `intended_use` | 用途 | string | 是 |

## 状态

- `completed`：核心成果完整，关键结论人工确认要求满足。
- `completed_with_limits`：至少一项实质成果，说明限制、已完成和受阻范围。
- `needs_input`：必填字段缺失。
- `needs_confirmation`：资料冲突或人工确认未完成。
- `failed`：计算或工具失败。

## 输出

- `事实核验表`：结构化条目数组，不允许空壳或占位文本。
- `错误/待核实项`：结构化条目数组，不允许空壳或占位文本。
- `引用检查`：结构化条目数组，不允许空壳或占位文本。
- `答案复核`：结构化条目数组，不允许空壳或占位文本。
- `适龄风险`：结构化条目数组，不允许空壳或占位文本。
- `发布建议`：结构化条目数组，不允许空壳或占位文本。

完整机器契约见`contract/input.schema.json`、`contract/output.schema.json`和`contract/runtime_contract.json`。
