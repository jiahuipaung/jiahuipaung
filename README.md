# Jiahui Pang / 庞嘉辉

**Backend Engineering · Distributed Systems · AI/Agent Engineering**

Computer Science master's student at the University of Macau, with a B.Eng. from Huazhong University of Science and Technology. I build backend and AI systems with a focus on explicit state, idempotency, failure recovery, and executable verification.

澳门大学计算机硕士在读，主要方向是 Go 后端、分布式工作流和 Agent 工程。相比堆叠组件，我更关注系统在重复请求、部分失败、消息乱序与外部调用结果不确定时，如何保持可恢复、可解释和可验证。

Open to 2027 new-grad opportunities in backend engineering and AI systems / 寻找 2027 届后端与 AI 系统方向机会。

[LinkedIn](https://www.linkedin.com/in/jiahui-pang-510065352/) · [Email](mailto:jiahuipaung@gmail.com)

## Featured Projects / 代表项目

### [Model Gateway Lab](https://github.com/jiahuipaung/model-gateway-lab)

An executable control plane for long-running AI generation tasks, built with Go and PostgreSQL. It models the failure windows around external model providers instead of treating every timeout as a simple retry.

一个面向长时 AI 生成任务的可运行控制面，重点处理“供应商已经受理、但本地没有收到响应”这类不确定结果，并验证后续恢复链路。

- Idempotent task intake and tenant-scoped APIs
- `UNKNOWN` reconciliation through a stable provider request key
- Lease-based workers with per-attempt fencing tokens
- Atomic terminal-state transitions with transactional outbox events
- Deterministic fake provider, Docker demo, and PostgreSQL integration tests

`Go` · `PostgreSQL` · `Docker` · `Distributed Systems`

[Repository](https://github.com/jiahuipaung/model-gateway-lab) · [Failure model and guarantees](https://github.com/jiahuipaung/model-gateway-lab/blob/main/docs/design/failure-windows.md)

### [GOrder](https://github.com/jiahuipaung/gorder)

A Go microservice workflow covering order creation, stock checks, payment sessions, payment callbacks, and fulfilment. The project focuses on keeping business state explainable under duplicate messages, concurrent updates, and partial failures.

一个围绕订单、库存、支付与履约展开的 Go 微服务项目。核心不是商城功能，而是通过显式状态机、数据库条件更新和消息确认语义，让重复与乱序事件能够安全重放。

- Explicit order state transitions instead of arbitrary status updates
- Database-level idempotency for payment and fulfilment commands
- Stable Stripe idempotency keys for checkout creation
- Mutually exclusive ACK/NACK paths with retry handoff failure handling
- Replay, concurrency, webhook, and race-detector coverage

`Go` · `gRPC` · `MongoDB` · `MySQL` · `RabbitMQ` · `Stripe`

[Repository](https://github.com/jiahuipaung/gorder) · [Architecture and reliability model](https://github.com/jiahuipaung/gorder/blob/main/docs/architecture/reliability.md)

## Selected Engineering Work / 工程实践

### Global Search Infrastructure

Participated in an online search migration from Algolia to Elasticsearch across multiple business indexes. My work included compatibility adapters, schema and filter normalization, transactional outbox workers, and dual-engine result comparison.

参与运行中搜索基础设施迁移，重点处理调用契约兼容、异构数据同步与搜索质量验证；通过 Outbox、租约、领取令牌和版本控制，使至少一次投递下的重复、乱序与失败恢复能够收敛。

### Multi-Agent Content Workflow

Worked on a multi-agent content workflow for crypto knowledge production, separating planning and brief validation from the more expensive writing pipeline. I implemented typed contracts, deterministic audits, selective semantic judging, reflection loops, and constrained access to external data.

参与并实现多 Agent 内容生产工作流，将 Brief 与 Article Pipeline 解耦：代码负责状态、预算、重试和质量闸门，模型负责规划、写作与语义判断；能用确定性规则解决的问题不交给 LLM。

## Current Focus / 当前关注

- Reliable execution for long-running AI tasks and uncertain provider outcomes
- Idempotency, Outbox/Inbox, reconciliation, and observable distributed workflows
- Agent harnesses with typed state, bounded tools, evaluation, and human handoff

Primary tools: `Go` · `Python` · `PostgreSQL / MySQL` · `Redis` · `RabbitMQ / Kafka` · `gRPC` · `Docker / Kubernetes` · `Elasticsearch` · `OpenTelemetry`

## Connect / 联系我

[LinkedIn](https://www.linkedin.com/in/jiahui-pang-510065352/) · [Email](mailto:jiahuipaung@gmail.com) · [GitHub](https://github.com/jiahuipaung)
