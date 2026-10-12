# 搜索入口与搜索词

下列入口来自原始调研使用的网站清单，仅作为寻找候选的入口，不是排名或对当前服务可用性的保证。每次使用时核对站点状态，最终结论回到官方仓库与文档。

## 按问题选择入口

| 搜索目标 | 可用入口 | 接下来核对什么 |
|---|---|---|
| 寻找商业软件的开源替代品 | [OpenAlternative](https://openalternative.co/) | 替代的是哪些功能，社区版是否覆盖关键需求 |
| 寻找自部署系统或工具 | [awesome-selfhosted](https://awesome-selfhosted.net/)、[selfh.st](https://selfh.st/) | 官方仓库、安装条件、外部服务依赖 |
| 通过中文介绍发现项目 | [HelloGitHub](https://hellogithub.com/) | 推荐文章对应的实际仓库、版本和维护状态 |
| 搜索代码、模块和开发底座 | [GitHub](https://github.com/)、[Gitee](https://gitee.com/)、[GitCode](https://gitcode.com/)、[GitLab](https://gitlab.com/) | 是否官方维护、源码与文档版本是否一致 |
| 补充托管与发行线索 | [Codeberg](https://codeberg.org/)、[SourceForge](https://sourceforge.net/)、[Bitbucket](https://bitbucket.org/) | 上游身份、许可证、下载包来源 |
| 寻找模型或 AI 组件 | [Hugging Face](https://huggingface.co/)、[ModelScope](https://modelscope.cn/) | 代码与权重许可、模型卡、硬件要求、目标语言/场景验证 |

用户指定网站时优先检索，并如实报告实际覆盖。未检索的站点与检索无结果的站点分开记录。

## 组合业务词与能力词

先拆需求，再生成中英文检索式。例如：

- 客户管理：`开源 CRM 客户跟进 数据权限`、`open source CRM record sharing follow-up`。
- 集团系统：`ERP CRM 财务 商城 开源`、`self hosted ERP CRM accounting integration`。
- 现场采集：`field sales geolocation photo offline sync`。
- 专项组件：`中文 ASR 方言 热词`、`Chinese speech recognition dialect`、`receipt OCR`。
- 开发底座：`multi tenant RBAC audit file permission`。

按具体平台的搜索语法调整，不把这些示例当作每次都要执行的命令。先按相关性发现，再检查维护与版本；不要只按 Star 筛选。

## 证据升级

目录条目 → 上游官方仓库 → 匹配版本的文档/许可 → 相关源码 → 获授权的隔离运行 → 目标环境/真实业务验收。

遇到付费边界、源码与文档不一致、只提供在线演示或公开仓库缺少初始化材料，单独记录，不能用相邻产品或旧版的结论补齐。
