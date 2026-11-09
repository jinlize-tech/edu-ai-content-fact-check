# AI生成教学内容事实核验

对AI生成的教学材料做事实、计算、引用、适龄性和内部一致性核验，标记需外部权威来源确认的项。

## 适用用户

教师、教研、内容审核员、教学主管

## 主要输出

- 事实核验表
- 错误/待核实项
- 引用检查
- 答案复核
- 适龄风险
- 发布建议

## 安装

将包含`SKILL.md`的根目录导入支持的Skill环境。

本地验证：

```powershell
node scripts/validate_input.js examples/typical_input.json
node scripts/validate_output.js examples/typical_output.json
```

## 使用

1. 阅读`USAGE.md`。
2. 按`contract/input.schema.json`准备输入。
3. 调用产品或Agent完成专业处理。
4. 使用`scripts/validate_output.js`检查成果。
5. 高风险结论交由业务负责人确认。

## 边界

- 不使用外部收费API。
- 不依赖其他产品完成核心任务。
- 不自动执行正式审批、退款、人员处罚或系统变更。
- 客户可见内容不包含公司品牌推广或内部研发资料。

## 状态

- 版本：`1.0.0`
- 本地契约与自动化测试：见`test-results/`
- 生成式模型运行：`MODEL_RUNTIME_NOT_VERIFIED`
- WorkBuddy安装、调用、审核、上架：`NOT_EXECUTED`
- 安装包：`dist/edu-ai-content-fact-check-v1.0.0.zip`

## 许可证

Apache-2.0。详见`LICENSE`。
