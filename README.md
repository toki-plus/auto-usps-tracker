# Auto USPS Tracker

[简体中文](./README.md) | [English](./README_en.md)

面向跨境电商运营的批量物流状态采集与报告工作流案例。

该方案将批量单号导入、状态查询、异常重试、结果清洗和 Excel 报告整合为一个桌面流程，用于减少运营人员逐单查询和手工整理物流状态的重复劳动。

> 本仓库是脱敏后的公开案例，包含方案说明与界面展示，不包含完整实现代码，也不包含任何客户或订单数据。

## 问题背景

跨境电商团队需要持续跟踪大量物流单号。旺季时一个运营人员每天可能要核对成百上千个 USPS 包裹的状态：逐单打开官网查询页、复制状态、粘贴回表格，一次全量核对就要数小时，而且容易漏查、重复录入、格式不一致，异常件（延误、派送失败、无记录）往往要到客户投诉时才被发现。

Auto USPS Tracker 将批量查询过程拆分为输入校验、受控并发、失败恢复、状态标准化和报告输出几个环节，把"逐单查询"变成"一次导入、一份报告"。

## 目标用户

- 跨境电商运营团队
- 负责物流异常跟进的客服与供应链人员
- 需要定期形成物流状态报表的业务人员

## 方案流程

```text
Tracking-number file
    -> Input validation
    -> Controlled query queue
    -> Retry and exception handling
    -> Status normalization
    -> Excel report
    -> Manual exception review
```

## 主要能力

- **批量导入与校验**：一次性导入数千个物流单号，自动剔除重复单号并校验格式，无效单号在进入查询队列前即被标记
- **合规频率下的批量状态查询**：基于 Playwright 驱动真实浏览器会话，以受控并发和请求限速执行批量查询，在遵守目标站点服务条款的前提下提升吞吐量，而非绕过任何访问控制
- **失败恢复**：对超时、临时失败和异常响应自动重试，最终失败的记录在报告中单独标注，不会静默丢失
- **详尽状态提取**：不仅获取最新状态（Delivered / In Transit 等），还采集详细状态描述与完整物流历史轨迹，便于异常溯源
- **状态标准化**：统一不同状态字段和时间格式，区分已签收、运输中、异常和无结果记录
- **格式化 Excel 报告**：导出 `.xlsx` 报告，带彩色表头、自动换行、边框和自适应列宽，按状态分组，适合直接筛选与跟进
- **桌面进度反馈**：在 PyQt5 界面中展示查询进度、成功数和异常数，支持配置 HTTP 代理以适应不同网络环境

## 技术方案

- Python 负责任务编排、数据处理和报告生成
- Playwright 负责浏览器会话与页面交互
- Pandas / Excel 工具负责结果清洗和报表输出
- PyQt5 提供桌面端参数配置与进度反馈
- 重试、限速和日志机制用于控制对外部服务的请求压力，并保证每一单的处理结果可追溯

## 📸 软件截图

<p align="center">
  <img src="./images/cover_software01.png" alt="软件主界面" width="800"/>
  <br>
  <em>软件主界面：导入单号、配置参数并跟踪查询进度。</em>
</p>
<p align="center">
  <img src="./images/cover_software02.png" alt="导出表格展示" width="800"/>
  <br>
  <em>导出的 Excel 报告：状态分组、格式统一，可直接用于跟进。</em>
</p>

## 当前状态

本仓库用于展示经过脱敏的需求背景、工作流设计和界面原型。完整实现与运行配置未公开。

## 数据与合规

- 不应在仓库、日志或截图中提交真实客户信息和物流单号；本仓库所有界面截图均已脱敏。
- 自动化查询应遵守 USPS 服务条款，并采用合理的请求频率；本方案通过限速与受控并发控制请求压力，不包含也不鼓励任何绕过访问控制的行为。
- 结果应由业务人员复核后再用于客户沟通或运营决策。

## 📂 更多项目

- [video-mover](https://github.com/toki-plus/video-mover) — 多平台内容分发自动化流水线：素材处理、文案生成、定时调度与多平台适配
- [ai-highlight-clip](https://github.com/toki-plus/ai-highlight-clip) — 长视频智能初筛：Whisper 转写 + LLM 评分 + 人工终审，分钟级定位高光片段
- [ai-ttv-workflow](https://github.com/toki-plus/ai-ttv-workflow) — 文案到短视频的桌面工作流，关键节点保留人工确认
- [ai-video-workflow](https://github.com/toki-plus/ai-video-workflow) — 多模型 AIGC 视频生成流水线：文生图、图生视频、文生音乐的异步编排
- [ai-mixed-cut](https://github.com/toki-plus/ai-mixed-cut) — 素材库结构化与脚本重组的视频再创作工作流
- [ai-trader-for-mt4](https://github.com/toki-plus/ai-trader-for-mt4) — LLM×MT4 受控执行框架：工具约束、风控规则、状态管理与异步桥接
- [ai-trader-for-mt5](https://github.com/toki-plus/ai-trader-for-mt5) — 面向 MT5 的 AI 交易助手与 EA 工程化框架
- [AB-Video-Deduplicator](https://github.com/toki-plus/AB-Video-Deduplicator) — 基于高帧率抽帧混合的视频再创作实验工具
- [netease-downloader](https://github.com/toki-plus/netease-downloader) — 网易云音乐下载桌面应用：扫码登录、下载队列、ID3 元数据写入

## License

See [LICENSE](./LICENSE).
