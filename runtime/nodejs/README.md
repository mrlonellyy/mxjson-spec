# MxJSON Node.js Runtime

> MxJSON 协议的 Node.js 运行时引擎实现

## 状态

📅 **计划中** - 预计 v1.2.0 版本发布

## 预期功能

- [ ] 协议解析器
- [ ] 模型适配器
- [ ] 工作流调度器
- [ ] 人工审核节点
- [ ] 审计日志
- [ ] 动态UI渲染

## 预期安装方式

```bash
npm install @mxjson/runtime
```

## 预期使用方式

```javascript
import { Runtime } from '@mxjson/runtime';

const runtime = new Runtime({
  openaiApiKey: 'sk-xxx',
});

const result = await runtime.execute('path/to/capability.mxjson', {
  input1: 'value1',
});
```

## 贡献

欢迎社区贡献！如果您有兴趣参与 Node.js 运行时的开发，请联系我们。

## License

MIT
