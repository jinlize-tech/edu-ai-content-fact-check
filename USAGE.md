# 使用说明

## 适用任务

AI生成的科学课讲义把实验结论说得过绝对，并引用了不存在的标准。

## 准备输入

AI生成内容、年级学科、课程标准/教材范围、允许使用的来源、参考答案、审核用途。使用前先脱敏姓名、联系方式和与任务无关的敏感信息。

## 操作步骤

1. 拆分断言
2. 分类可内部核验/需外部来源
3. 检查计算和逻辑
4. 对照用户材料
5. 标记未证实项
6. 输出修订与复核

## 校验命令

```powershell
node scripts/validate_input.js examples/typical_input.json
node scripts/validate_output.js examples/typical_output.json
```

## 状态使用

- `completed`：核心成果完整。
- `completed_with_limits`：只完成可验证部分，并说明受阻范围。
- `needs_input`：缺少关键输入。
- `needs_confirmation`：资料冲突或需人工确认。
- `failed`：工具或计算失败，提供恢复动作。

## 人工确认

业务负责人复核输入事实、关键假设和最终成果适用范围后，成果才可进入正式业务使用。
