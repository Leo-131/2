# 2
辅助选品

## 通用自动化客户开发插件

版本：1.1.0。支持不同品牌、产品或服务类目、目标市场及合作模式。

- `plugin.json`：标准插件入口及展示信息。
- `.codex-plugin/plugin.json`：兼容格式入口。
- `.agents/plugins/marketplace.json`：可从 GitHub 导入的插件目录。
- `skills/automated-customer-development/SKILL.md`：客户开发工作流。
- `dist/universal-customer-development-1.1.0.zip`：可上传的插件包。

### 安装

在支持 ZIP 上传的 ChatGPT 插件界面上传 `dist/universal-customer-development-1.1.0.zip`，等待扫描完成后安装。也可通过 Plugin Creator 创建或更新插件，提供本仓库和 ZIP。

支持 GitHub 插件目录导入的工作区管理员，可以导入 `https://github.com/Leo-131/2` 的 `main` 分支；目录位于 `.agents/plugins/marketplace.json`。在导入结果中检查技能是否可用，并设置安装策略。

支持插件 CLI 的 Codex 环境可运行：

```sh
codex plugin marketplace add https://github.com/Leo-131/2.git
codex plugin add universal-customer-development@leo-customer-development
```

安装到一个云端执行环境不代表安装到你的 ChatGPT 账号或本地桌面应用。应在实际使用的界面确认插件已出现、技能可调用，再视为生效。

### 使用示例

> 使用通用自动化客户开发：品牌为我提供的品牌，产品为家居收纳用品，目标市场为德国，寻找 20 家进口商和分销商。本次进行研究并生成德语开发信草稿。

插件本身提供流程技能。搜索、CRM、邮件发送和定时跟进依赖宿主中实际可用的工具及用户授权，不附带发送账号或后台执行器。

### 发布范围

GitHub 仓库与版本标签用于分发源码和插件包。账号内安装、工作区发布和公共插件目录上架是不同状态；仅推送仓库不会自动完成后两者。

格式与安装流程依据：[OpenAI 插件打包文档](https://developers.openai.com/plugins/build/plugins)及[GitHub 插件目录导入说明](https://help.openai.com/en/articles/20001504-importing-and-syncing-plugin-marketplaces-from-github)。
