# xxl-job

[xxl-job](https://www.xuxueli.com/xxl-job/)是一个全异步分布式任务调度平台，其包含调度中心（admin）和执行器（executor）两个部分，分别实现任务调度和任务执行。

对于一个分布式任务调度平台，需要解决的问题主要有：
- 调度管理：触发策略、路由策略、故障转移
- 任务管理：任务定义（支持不同类型的任务）、任务状态、状态处理（失败重试、失败告警、超时控制）、子任务编排
- 执行器管理：任务执行，动态扩缩容
- 分布式调度的一致性、调度中心和执行器的高可用HA

## 项目结构
```
xxl-job
├── xxl-job-admin                             调度中心
├── xxl-job-core                              公共依赖
└── xxl-job-executor-samples                  执行器Sample示例
    ├── xxl-job-executor-sample-frameless     无框架版本
    └── xxl-job-executor-sample-springboot    SpringBoot版本
```
