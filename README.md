![banner](assets/banner.svg)

# Cursor 完全教程——AI 编程，从入门到精通 🚀

> **AI 编程时代，编辑器该长什么样？** Cursor 就是答案：把 Claude/GPT 直接嵌进代码编辑器，Tab 补全、对话改代码、Agent 自动干活——第一次用会觉得"回不去了"。
>
> 这份教程把 Cursor 从**下载安装到高阶工作流**整理成 10 大章节，每个功能都配**操作路径 + 适用场景 + 避坑提醒**，新手照着做就能上手，老手也能挖出几个不知道的技巧。

`cursor-tutorial-zh` 是一份**纯 Markdown 的中文 Cursor 教程**：打开就能跟着操作、按主题分文件、步骤清晰准确。

⭐ 如果对你有帮助，点个 Star 支持中文开源

## 为什么值得收藏

- 📚 **10 大章节全覆盖**：安装界面 / Tab 补全 / Chat 对话 / Agent 模式 / Rules 规则 / MCP 集成 / 模型配置 / 工作流 / 快捷键 / 避坑——Cursor 能干的，这里都讲。
- 🎯 **每个功能都能照做**：操作路径写到按键级别，跟着点一遍就会。
- 🔍 **适用场景标注**：每个功能告诉你"什么时候用、什么时候别用"，不教无脑用法。
- 🛡️ **避坑提醒**：登录失败、代理失效、规则不生效、Token 狂烧——高频坑提前预警。
- ✍️ **全原创中文措辞**：不搬运官方文档原文，以实际操作体验为准。

## 速查索引（想学哪块 → 打开哪篇）

| 章节 | 内容 | 适合谁 |
| --- | --- | --- |
| [01 安装与界面设置](topics/01-install-and-setup.md) | 下载/注册/语言包/界面布局 | 所有人，从零开始 |
| [02 Tab 补全与行内编辑](topics/02-tab-and-inline-edit.md) | Tab 补全 / Ctrl+K / Diff | 所有人，每天必用 |
| [03 Chat 对话模式](topics/03-chat-mode.md) | 对话改代码 / @ 引用 / 图片输入 | 所有人，核心用法 |
| [04 Agent 与 Composer](topics/04-agent-composer.md) | 多文件编辑 / 自动执行任务 | 想真正提效的 |
| [05 Cursor Rules 规则](topics/05-cursor-rules.md) | 全局/项目规则 / 规则写法 | 团队与项目协作 |
| [06 MCP 集成](topics/06-mcp-integration.md) | MCP 是什么 / 配置 / 常用服务 | 进阶玩家 |
| [07 模型与提供商](topics/07-models-and-providers.md) | 内置模型 / API Key 接入 | 想省钱/换模型的 |
| [08 高效工作流](topics/08-workflows.md) | 搭项目/重构/测试/Debug | 想提升开发效率的 |
| [09 快捷键与效率技巧](topics/09-shortcuts-and-tips.md) | 快捷键表 / 多光标 / 技巧 | 所有人，随时查 |
| [10 常见问题与避坑](topics/10-faq-and-pitfalls.md) | 登录/代理/规则/Token 问题 | 遇到问题先翻这篇 |

## 使用建议

1. **第一天**：过 01-03 章，把 Tab 补全和 Chat 用起来，立刻感受到效率差异。
2. **第一周**：学 04-05 章，试试 Agent 和 Rules，建立自己的使用习惯。
3. **进阶**：按需看 06-09 章，接入 MCP、配自己的模型、打磨工作流。
4. **卡住了**：先翻 10 章避坑清单，90% 的问题都有答案；没覆盖的欢迎提 Issue。

## 教程条目示例

```markdown
### Ctrl+K：行内编辑（Inline Edit）

- **操作路径**：光标选中代码 → `Ctrl+K` → 输入修改指令 → Enter → 查看 Diff
- **适用场景**：改函数名、加注释、修 bug、重命名变量等单点修改
- **避坑**：改动范围大时别用行内编辑，切 Composer/Agent 更稳
- **小技巧**：选中多行再 Ctrl+K，可一次改整块逻辑
```

每条都长这样：**功能 → 操作路径 → 适用场景 → 避坑提醒**。

## 教程结构

```
cursor-tutorial-zh/
├── topics/                    # 10 个章节
│   ├── 01-install-and-setup.md
│   ├── 02-tab-and-inline-edit.md
│   ├── 03-chat-mode.md
│   ├── 04-agent-composer.md
│   ├── 05-cursor-rules.md
│   ├── 06-mcp-integration.md
│   ├── 07-models-and-providers.md
│   ├── 08-workflows.md
│   ├── 09-shortcuts-and-tips.md
│   └── 10-faq-and-pitfalls.md
├── assets/
│   └── banner.svg              # 原创横幅
├── SOURCES.md                  # 外部参考来源与许可
├── LICENSE                     # MIT License
└── README.md
```

## 质量承诺

- ✅ 每个操作路径经过实测核对，按键/菜单名称确保正确
- ✅ 无占位符、无"待补充"——打开就能跟着做
- ✅ 全原创中文措辞，只参考官方文档与社区经验的覆盖面
- ❓ 发现错误？开 [Issue](https://github.com/zieang88888/cursor-tutorial-zh/issues)，核实后第一时间修正

## 星标理由（认真脸）

AI 编程工具更新太快，**教程收藏了不看 = 白收藏**。
Star 一下，等你想认真学 Cursor 的那天，回来照着做一遍，一小时入门，一天熟练。⭐

## License

[MIT](LICENSE) © zieang88888

---

*希望每一个用 Cursor 的开发者，都能少走弯路，早点下班。*

## 姊妹项目

中文开源矩阵，一网打尽开发者的知识库：

- [zhskills · 中文技能库](https://github.com/zieang88888/zhskills)
- [awesome-ai-tools-zh · AI 工具导航](https://github.com/zieang88888/awesome-ai-tools-zh)
- [llm-interview-zh · 大模型面试题库](https://github.com/zieang88888/llm-interview-zh)
- [free-programming-books-zh · 编程书籍大全](https://github.com/zieang88888/free-programming-books-zh)
- [system-design-zh · 系统设计面试](https://github.com/zieang88888/system-design-zh)
- [awesome-python-zh · Python 生态导航](https://github.com/zieang88888/awesome-python-zh)
- [ohmyzsh-zh · 终端效率神器](https://github.com/zieang88888/ohmyzsh-zh)
- [office-cheatsheet-zh · 办公效率速查](https://github.com/zieang88888/office-cheatsheet-zh)
