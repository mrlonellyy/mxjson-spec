# 智能多语言翻译 / Smart Translator

> 基于 MxJSON 协议的智能翻译能力包

## 功能特性

- ✅ 自动语言检测
- ✅ 多语言互译（中/英/日/韩/法/德）
- ✅ 专业领域适配
- ✅ 自定义术语表支持

## 快速使用

```php
use MxJSON\Runtime;

$runtime = new Runtime();
$result = $runtime->execute(__DIR__ . '/translator.mxjson', [
    'content' => 'Hello, how are you today?',
    'target_language' => 'zh',
    'domain' => 'general'
]);

echo $result['translated_text'];
// 输出：你好，今天过得怎么样？
```

## 输入参数

| 参数 | 类型 | 必需 | 说明 |
|------|------|------|------|
| `content` | string | 是 | 待翻译内容 |
| `source_language` | string | 否 | 源语言，默认自动检测 |
| `target_language` | string | 是 | 目标语言代码 |
| `domain` | string | 否 | 专业领域 |

## 支持的语言

| 代码 | 语言 |
|------|------|
| `zh` | 中文 |
| `en` | 英语 |
| `ja` | 日语 |
| `ko` | 韩语 |
| `fr` | 法语 |
| `de` | 德语 |

## 定价

- 免费试用：20 次/账户
- 按次付费：0.1 元/次

## License

MIT
