# Contributing to Lexicon Agent Framework

感谢您考虑为 Lexicon Agent Framework 做出贡献！我们欢迎所有形式的贡献，包括但不限于：

- 🐛 Bug 报告
- 💡 功能请求
- 📝 文档改进
- 🔧 代码贡献
- 🧪 测试用例
- 📖 示例和教程

## 🚀 快速开始

### 开发环境设置

1. **Fork 并克隆仓库**
```bash
git clone https://github.com/your-username/lexicon-agent.git
cd lexicon-agent
```

2. **安装依赖**
```bash
# 使用 Poetry (推荐)
pip install poetry
poetry install

# 或使用 pip
pip install -e ".[dev]"
```

3. **运行测试**
```bash
poetry run pytest tests/
# 或
python -m pytest tests/
```

4. **运行示例**
```bash
poetry run python examples/basic_usage.py
```

## 📋 贡献指南

### Bug 报告

如果您发现了 bug，请创建一个 issue 并包含以下信息：

- **描述**: 清晰简洁的问题描述
- **重现步骤**: 详细的重现步骤
- **期望行为**: 您期望发生什么
- **实际行为**: 实际发生了什么
- **环境信息**: Python 版本、操作系统等
- **错误日志**: 相关的错误信息和堆栈跟踪

### 功能请求

我们欢迎新功能的建议！请创建一个 issue 并包含：

- **功能描述**: 清晰描述建议的功能
- **使用场景**: 解释这个功能的用途
- **实现建议**: 如果有想法，请分享实现方案
- **替代方案**: 考虑过的其他解决方案

### 代码贡献

#### 代码规范

我们遵循以下代码规范：

- **Python 风格**: 遵循 PEP 8
- **类型提示**: 使用 Python 类型提示
- **文档字符串**: 使用 Google 风格的 docstring
- **测试**: 为新功能编写测试用例

#### 提交流程

1. **创建分支**
```bash
git checkout -b feature/your-feature-name
# 或
git checkout -b fix/your-bug-fix
```

2. **编写代码**
   - 遵循代码规范
   - 添加必要的测试
   - 更新相关文档

3. **测试验证**
```bash
# 运行所有测试
poetry run pytest

# 检查代码风格
poetry run flake8 lexicon_agent/

# 类型检查
poetry run mypy lexicon_agent/
```

4. **提交更改**
```bash
git add .
git commit -m "feat: add new feature description"
# 或
git commit -m "fix: fix bug description"
```

我们使用 [Conventional Commits](https://www.conventionalcommits.org/) 规范：
- `feat:` 新功能
- `fix:` Bug 修复
- `docs:` 文档更新
- `style:` 代码格式调整
- `refactor:` 代码重构
- `test:` 测试相关
- `chore:` 其他更改

5. **推送并创建 PR**
```bash
git push origin feature/your-feature-name
```

然后在 GitHub 上创建 Pull Request。

#### Pull Request 指南

请确保您的 PR：

- [ ] 有清晰的标题和描述
- [ ] 链接到相关的 issue
- [ ] 包含必要的测试
- [ ] 更新了相关文档
- [ ] 通过了所有 CI 检查
- [ ] 遵循项目的代码规范

### 文档贡献

文档改进同样重要！您可以：

- 修复文档中的错误
- 改进现有文档的清晰度
- 添加新的示例
- 翻译文档到其他语言

## 🏗️ 架构指南

### 核心组件

Lexicon Agent Framework 包含以下核心组件：

1. **Context Engineering** (`lexicon_agent/core/context/`)
   - 上下文检索、处理和管理
   - 实现智能上下文工程

2. **Agent Controller** (`lexicon_agent/core/agent/`)
   - 六阶段流式生成循环
   - 会话状态管理

3. **Orchestration Engine** (`lexicon_agent/core/orchestration/`)
   - 多智能体协调
   - 五种编排策略

4. **Tool System** (`lexicon_agent/core/tools/`)
   - 工具注册和调度
   - 安全管理

5. **Streaming Processing** (`lexicon_agent/core/streaming/`)
   - 流式数据处理
   - 性能优化

### 设计原则

- **模块化**: 每个组件都是独立的、可测试的
- **可扩展**: 易于添加新功能和组件
- **类型安全**: 使用 Python 类型提示
- **异步优先**: 使用 asyncio 进行异步处理
- **流式处理**: 支持实时流式响应

## 🧪 测试指南

### 测试结构

```
tests/
├── test_core_functionality.py    # 核心功能测试
├── test_context_engineering.py   # 上下文工程测试
├── test_tool_system.py          # 工具系统测试
├── test_orchestration.py        # 编排系统测试
└── test_performance.py          # 性能测试
```

### 测试类型

- **单元测试**: 测试单个组件的功能
- **集成测试**: 测试组件间的交互
- **性能测试**: 测试系统性能和并发能力
- **端到端测试**: 测试完整的用户流程

### 编写测试

```python
import pytest
from lexicon_agent import LexiconAgent

class TestYourFeature:
    @pytest.mark.asyncio
    async def test_your_feature(self):
        async with LexiconAgent() as agent:
            result = await agent.your_method()
            assert result is not None
```

## 📝 文档指南

### 文档结构

- **README.md**: 项目概述和快速开始
- **docs/**: 详细文档
- **examples/**: 使用示例
- **API 文档**: 自动生成的 API 文档

### 文档规范

- 使用 Markdown 格式
- 包含代码示例
- 提供清晰的说明
- 保持更新

## 🤝 社区

### 行为准则

我们致力于为所有人提供友好、安全和欢迎的环境。请阅读我们的行为准则。

### 沟通渠道

- **GitHub Issues**: Bug 报告和功能请求
- **GitHub Discussions**: 一般讨论和问题
- **Pull Requests**: 代码审查和讨论

## 🙏 致谢

感谢所有为 Lexicon Agent Framework 做出贡献的开发者！

### 贡献者

- 查看 [贡献者列表](https://github.com/your-org/lexicon-agent/contributors)

## 📄 许可证

通过为此项目做出贡献，您同意您的贡献将在 [MIT License](LICENSE) 下授权。