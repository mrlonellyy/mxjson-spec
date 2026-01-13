# 合同风险智能审核 / Contract Risk Review

> 基于 MxJSON 协议的合同风险自动识别与评估能力包

## 功能特性

- ✅ 自动识别合同类型
- ✅ 关键条款智能提取
- ✅ 风险点自动分析
- ✅ 高风险条款人工复核
- ✅ 结构化审核报告

## 快速使用

```php
use MxJSON\Runtime;

$runtime = new Runtime();
$result = $runtime->execute(__DIR__ . '/contract-review.mxjson', [
    'contract_text' => file_get_contents('sample-contract.txt'),
    'contract_type' => 'auto'
]);

echo "风险等级: " . $result['risk_level'];
echo "风险评分: " . $result['risk_score'];
```

## 输入参数

| 参数 | 类型 | 必需 | 说明 |
|------|------|------|------|
| `contract_text` | string | 是 | 合同全文内容 |
| `contract_type` | string | 否 | 合同类型，默认自动识别 |

## 输出结果

```json
{
  "risk_level": "medium",
  "risk_score": 65,
  "risk_items": [
    {
      "clause": "第八条 违约责任",
      "risk": "违约金比例过高（30%）",
      "suggestion": "建议降至10%-20%"
    }
  ],
  "suggestions": [
    "建议明确付款时间节点",
    "建议增加不可抗力条款"
  ],
  "reviewed_by": "AI"
}
```

## 工作流程

```
合同输入 → 条款提取 → 风险分析 → 高风险检查 → [人工复核] → 生成报告
```

## 定价

- 免费试用：5 次/账户
- 按次付费：2.0 元/次

## License

MIT
