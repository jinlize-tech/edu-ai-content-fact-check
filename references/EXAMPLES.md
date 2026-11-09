# AI生成教学内容事实核验示例

## 典型场景

AI生成的科学课讲义把实验结论说得过绝对，并引用了不存在的标准。

## 具体示例

系统标记虚构来源和过度结论，保留可验证部分，并要求教师依据权威材料确认。

## 脱敏输入示例

```json
{
  "contract_version": "1.2.0",
  "data_status": "confirmed",
  "contains_sensitive_data": false,
  "requested_output_language": "zh-CN",
  "ai_generated_content": "AI生成教学内容已核对（脱敏示例）",
  "grade_subject": "年级与学科已核对（脱敏示例）",
  "curriculum_scope": "教材与课程标准范围已核对（脱敏示例）",
  "allowed_sources": [
    {}
  ],
  "answer_key": "参考答案已核对（脱敏示例）",
  "target_age": "目标年龄已核对（脱敏示例）",
  "intended_use": "用途已核对（脱敏示例）"
}
```

## 预期处理

1. 运行输入契约校验。
2. 逐项核对输入来源、版本和口径。
3. 按`references/PROFESSIONAL_PLAYBOOK.md`完成专业分析。
4. 输出事实核验表、错误/待核实项、发布建议等核心成果。
5. 由业务负责人确认输入事实、关键假设和最终成果适用范围后才可作为正式业务结论。

## 不应出现的输出

- 虚构政策、价格、人员、课程或客户事实。
- 以“暂无”“待完善”等占位文本冒充完成。
- 无依据的确定性判断或伪造人工签批。
