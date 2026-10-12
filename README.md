# 开源项目适配调研 · Open Source Fit

一个帮助 Codex 为现有项目查找、核验和比较开源方案的 skill。

它回答：**哪些开源产品或组件能帮到我的项目？哪些可以直接用，哪些需要改造，哪些只值得学习？**

## 让 Codex 帮你安装

把下面这段话复制给能够联网并访问本机文件的 Codex：

```text
帮我安装此 skill：https://github.com/dog0813-stack/open-source-fit
```

也可以直接提供技能目录的链接：

```text
帮我安装此 skill：https://github.com/dog0813-stack/open-source-fit/tree/main/skills/open-source-fit
```

安装完成后，下一轮对话可以输入：

```text
使用 $open-source-fit，先阅读当前项目的规则、README 和最新状态，
帮我从开源网站查找能改善本项目的产品或组件。
预算优先免费，核对官方仓库、源码、免费版范围、许可和部署条件。
比较保留现项目优化与采用新底座的收益和代价，给出推荐方案及最小验证计划。
先商量好，再开始实施。
```

## 给安装技能的 Codex

- 本仓库中的技能名：`open-source-fit`。
- 唯一技能目录：`skills/open-source-fit`。
- 入口文件：`skills/open-source-fit/SKILL.md`。
- 下载整个技能目录，包括 `agents/`、`references/` 和 `LICENSE`，保留其相对路径；不必把仓库 README 放进技能目录。
- 优先使用当前环境的内置 `skill-installer` 从 GitHub 安装，不运行本仓库的业务或安装脚本；本仓库没有可执行脚本和必须连接的服务。
- 根仓库 URL 需要同时传入 `--path skills/open-source-fit`；含 `/tree/main/skills/open-source-fit` 的 URL 已包含路径。
- 已有同名技能时先检查现有内容和来源；不要静默覆盖用户修改。
- 安装目标使用当前 Codex 的技能目录。手动安装可使用用户主目录 `.agents/skills/open-source-fit/` 或项目 `.agents/skills/open-source-fit/`。
- 确认 `SKILL.md`、引用文件和许可齐全，再报告安装结果。Codex 检测不到时重启；此请求只授权安装该技能。

内置安装器的调用参数如下。脚本文件位于当前环境的 `skill-installer/scripts/`，请由 Codex 找到其实际路径，不要照搬其他电脑的绝对路径：

```text
install-skill-from-github.py --repo dog0813-stack/open-source-fit --path skills/open-source-fit
```

本地发现方式参考 [OpenAI 官方技能文档](https://learn.chatgpt.com/docs/build-skills)。安装需要当前环境能访问 GitHub，并拥有对应目录的写入权限；网址提供安装来源，不会自动授予执行权限。

## 方法流程

1. **建立项目画像**：了解业务流程、当前实现、技术栈、预算和不能改变的规则。
2. **分层搜索**：成品系统、开发底座、专项组件、可借鉴设计分别寻找。
3. **核对官方证据**：仓库、版本、源码、免费版边界、许可、运行资源和维护情况。
4. **映射关键需求**：区分直接满足、需要适配、仅可借鉴、不满足和待核实。
5. **比较采用路线**：保留项目接入组件、局部借鉴、采用新底座或使用成品系统。
6. **给出最小验证计划**：用可观察的业务场景检验关键假设，明确未验证事项。

例如：多个模块共用一个后台，不代表客户、订单和库存已打通；不同语言的模块可能只能复用设计；开源标签不能证明关键功能在免费版中。

## 文件结构

```text
skills/open-source-fit/
├── SKILL.md
├── LICENSE
├── agents/openai.yaml
└── references/
    ├── search-sources.md
    ├── research-template.md
    └── historical-example.md
```

包含搜索入口、调研报告模板和匿名历史案例。无需指定插件；实际搜索与源码阅读能力由当前 Codex 环境提供。检索受限时要求如实报告。

## 使用范围与开源许可

这个技能整理自实际开源调研流程，并用通用示例解释选型方式。它用于调研和方案比较；采购、试用、数据迁移与部署按用户实际授权处理。旧案例不是固定推荐，价格、许可、版本与功能边界需要在使用时重新核验。

本仓库只包含技能及说明，采用 [MIT License](LICENSE)。搜索入口与示例中提及的第三方项目保留其各自许可，本仓库许可不覆盖它们。
