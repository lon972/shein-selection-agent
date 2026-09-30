# SHEIN 女装选品与跟版决策 Agent

这是一个实验性的 Node.js 采集与选品工具包，按公开页面发现候选，做证据清洗、去重、欧美/土耳其区域化评分，并在满足证据门禁后调用 Dify 写作。

文件：[SHEIN-source.zip](./SHEIN-source.zip)，解压后目录为 `sheIn-agent/`。

## 包含与运行

压缩包包含源码、测试、docs、fixtures、配置、Dify DSL、`.env.example`、package-lock 和启动脚本；包含空白候选模板，不包含 `.env`、`node_modules`、数据库、历史输出或真实业务输入。需要 Node.js 20 或 22 LTS。解压后在 `sheIn-agent/` 执行 `npm ci`，复制 `.env.example` 为 `.env`，再执行 `npm test` 与 `npm run check`。

## 实验边界

本仓库是公开试验材料。本次上传前已完成源码静态语法、JSON/YAML 和压缩包排除项检查，没有做本次真实 SHEIN 页面或线上 Dify 端到端验收。采集失败或解析为空不代表市场没有商品；公开发现级候选不能直接变成打样建议。决策仍需人工核验商品详情、企业成本、历史经营数据和知识产权边界。请遵守目标网站条款、robots 规则和适用法律，不绕过登录、验证码或访问控制。

## 反馈

请在 [Issues](https://github.com/lon972/shein-selection-agent/issues) 提交可复现的问题或改进建议。
