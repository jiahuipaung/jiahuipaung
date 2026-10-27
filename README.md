# Hi, I'm Jiahui 👋

Go Backend · Distributed Systems · AI & Agents

I'm a Computer Science master's student at the University of Macau, with a bachelor's degree from Huazhong University of Science and Technology (HUST). I work mainly with Go and Python, with experience in commerce backends, search infrastructure, model platforms, and agent workflows.

澳门大学计算机硕士在读，本科毕业于华中科技大学。主要写 Go 和 Python，做过交易、搜索和模型平台相关的后端开发，最近也在探索 Agent 如何融入实际业务。我喜欢把开发中遇到的问题整理成能运行的项目，也记录做这些选择的原因。

Looking for 2027 new-grad roles in backend and AI engineering / 寻找 2027 届后端与 AI 工程方向机会。

[LinkedIn](https://www.linkedin.com/in/jiahui-pang-510065352/) · [Email](mailto:jiahuipaung@gmail.com)

## Projects / 项目

### [Model Gateway Lab](https://github.com/jiahuipaung/model-gateway-lab)

A Go control plane for asynchronous AI generation tasks. Handles idempotent submissions, uncertain provider responses, worker recovery, and event delivery, with a local Docker demo and PostgreSQL integration tests.

模型调用超时后，任务究竟失败了，还是已经在供应商端执行？这个项目围绕长时生成任务，处理幂等提交、未知结果对账和故障恢复，并提供可本地复现的场景。

`Go` · `PostgreSQL` · `Docker`

[Code](https://github.com/jiahuipaung/model-gateway-lab) · [Design notes](https://github.com/jiahuipaung/model-gateway-lab/blob/main/docs/design/failure-windows.md)

### [GOrder](https://github.com/jiahuipaung/gorder)

A Go microservice project connecting orders, stock checks, Stripe payments, and fulfilment. Includes explicit state transitions and tests for duplicate payment events, concurrent updates, and message retries.

串起下单、库存校验、支付回调到履约的业务流程。重点解决支付消息重复到达、订单状态并发更新和消费失败重试等问题，配有架构文档与测试。

`Go` · `gRPC` · `MongoDB` · `MySQL` · `RabbitMQ` · `Stripe`

[Code](https://github.com/jiahuipaung/gorder) · [Architecture](https://github.com/jiahuipaung/gorder/blob/main/docs/architecture/overview.md)

## More of My Work / 其他实践

### Global Search Infrastructure

Contributed to an Algolia-to-Elasticsearch migration, including API compatibility, schema and filter adaptation, reliable index synchronization, and search result comparison.

参与在线搜索迁移，处理新旧引擎的接口兼容、数据同步与结果差异。一次预发布故障测试让我进一步理解了“有重试”和“任务不会丢”之间的区别，也推动了写链路向 Transactional Outbox 演进。

### Multi-Agent Content Workflow

Contributed to a multi-agent workflow for crypto content production. My subsequent implementation explores separate brief and article pipelines, structured outputs, rule-based audits, and feedback-driven revision.

参与 Crypto 内容生产工作流，并在后续实现中探索选题与写作分阶段、结构化输出、规则审计和反馈修订。我关心的是如何把规划、检索、写作和审核组织成一个能持续运行的流程。

## Exploring / 最近在探索

- Long-running AI tasks: recovery, reconciliation, and provider integration / AI 长任务与模型平台
- Agent workflows: tool use, evaluation, and human review / Agent 工具调用、评测与人工审核
- Turning project lessons into code and design notes / 把项目经验整理成代码与设计记录
