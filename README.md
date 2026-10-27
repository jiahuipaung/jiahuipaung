# Hi, I'm Jiahui 👋

Go Backend · Distributed Systems · AI & Agents

I'm a Computer Science master's student at the University of Macau, with a bachelor's degree from Huazhong University of Science and Technology (HUST). I work mainly with Go and Python, with experience in commerce backends, search infrastructure, model platforms, and agent workflows.

澳门大学计算机硕士在读，本科毕业于华中科技大学。主要写 Go 和 Python，做过交易、搜索和模型平台相关的后端开发，最近也在探索 Agent 如何融入实际业务。我喜欢把开发中遇到的问题整理成能运行的项目，也记录做这些选择的原因。

Looking for 2027 new-grad roles in backend and AI engineering / 寻找 2027 届后端与 AI 工程方向机会。

[LinkedIn](https://www.linkedin.com/in/jiahui-pang-510065352/) · [Email](mailto:jiahuipaung@gmail.com)

## Experience / 工作与实习经历

### Bybit · Backend & AI Agent Engineering Intern / 后端与 Agent 开发实习生

May–Aug 2026 · Consumer Growth

Worked on search infrastructure migration and multi-agent content workflows. 参与统一搜索服务迁移与多 Agent 内容生产系统。

### Qiniu Cloud / 七牛云 · Backend Engineering Intern / 后端开发实习生

Dec 2025–Mar 2026 · LLM Inference Platform

Contributed to the MaaS platform, including trial-access controls, multimodal model integration, and asynchronous generation tasks. 参与 MaaS 平台开发，涉及体验期访问治理、多模态模型接入与异步生成任务。

### TP-Link · Backend Engineer / 后端开发工程师

Jul 2023–Mar 2025 · Full-time / 全职

Developed order, payment, and inventory services for virtual-product sales and subscriptions on an IoT platform. 从事物联平台虚拟商品销售与订阅业务的订单、支付和库存后端开发。

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

### [llmaz](https://github.com/InftyAI/llmaz) · Open Source

Worked on a Dragonfly integration proposal for this Kubernetes-based LLM inference platform, exploring P2P distribution of model files and container images. Also contributed a merged fix aligning the OpenModel example with its CRD.

参与 Dragonfly 集成方案，探索通过 P2P 分发模型文件与容器镜像；另修复了 OpenModel 示例与 CRD 定义不一致的问题。

[Dragonfly proposal](https://github.com/InftyAI/llmaz/pull/479) · [Merged contribution](https://github.com/InftyAI/llmaz/pull/481)

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
