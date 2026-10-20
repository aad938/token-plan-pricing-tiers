# Token Plan 个人版购买：四档套餐价格对比、扣费规则与夜间折扣，按用量选档位更划算

Token Plan 个人版是阿里云百炼面向个人开发者的模型订阅服务，用 Credits 这一个单位支付文本模型、多模态模型和内置模型工具的调用费用。它目前只在北京地域开放，四档套餐限时价 39–499 元/月，订阅后按 30 天一个周期计算额度。

买之前真正要搞清楚的就三件事：选哪档、额度怎么扣、超额了怎么办。下面按这个顺序讲。

> **选购速览**：每月用量不大，Lite（限时 39 元/月，11,500 Credits）跑日常对话和轻量编码基本够用；同时挂多个 agent、或需要 AgentStudio 工具权益，从 Standard（限时 139 元/月）起步；高强度用户直接看 Pro（限时 499 元/月，180,000 Credits）。👉 [查看 Token Plan 个人版当前限时价格](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny)

## 四档套餐价格与额度对比

官方目前展示的套餐就这四档，价格分原价和限时时价，付款按限时价收：

| 套餐 | 限时价（原价） | 额度（每 30 天） | 并发 Agents | 权益差异 | 购买 |
| --- | --- | --- | --- | --- | --- |
| Lite | 39 元/月（原价 60 元） | 11,500 Credits | 1–2 | 多模态模型、内置工具、兼容主流工具 | [开通 Lite](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny) |
| Essential | 79 元/月（原价 120 元） | 25,500 Credits | 2–3 | 含 Lite 全部权益 | [开通 Essential](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny) |
| Standard | 139 元/月（原价 180 元） | 45,000 Credits | 3–4 | 含 Lite 权益 + Harness 权益 | [开通 Standard](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny) |
| Pro | 499 元/月（原价 600 元） | 180,000 Credits | 6–8 | 含 Standard 权益 + 更高并发 + Harness 权益 | [开通 Pro](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny) |

把限时价折算成每万 Credits 的成本：Lite 约 34 元，Essential 约 31 元，Standard 约 30.9 元，Pro 约 27.7 元。档位越高单位成本越低，Pro 比 Lite 便宜近两成，前提是你真能用得完。

几条选档判断：

- Essential 比 Lite 贵 40 元、额度多 14,000 Credits。月用量在 11,500 上下浮动，这 40 元买的是“月中不停服”；稳定在 8,000 以内，Lite 就是终点。
- Harness 权益（AgentStudio 工具的每月免费额度和后付费折扣）只有 Standard 和 Pro 有，单独计量，不从 Credits 里扣。要用 AgentStudio，Essential 再便宜也覆盖不到这块。
- 并发数影响多任务体验。同时挂 3 个以上 agent，Lite 的 1–2 并发会排队，至少上 Standard。

## 开通步骤：从订阅到在 Claude Code 里跑起来

全程在百炼控制台完成，四步：

1. 进入百炼控制台的 Token Plan 个人版订阅页，选档位付款。订阅周期从付款当天起算 30 天。
2. 在控制台获取 API Key 和对应的 Base URL。
3. 把密钥填进你在用的 AI 编程或 agent 工具。官方列出的兼容工具包括 Claude Code、Cursor、Qwen Code、Qoder、Qoder CN 和 OpenClaw。
4. 首次调用后回到订阅页的用量明细，确认每次请求实际扣了多少 Credits——这个数字由模型类型、token 用量、是否开思考模式、是否调用工具动态决定，没有统一价目表，以明细为准。

👉 [前往订阅页选择档位开通](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny)

## 扣费规则：这几条直接影响额度能撑多久

核心逻辑一句话：先扣主额度，再扣用量包，都没有就暂停服务；额度按订阅月清零。下面是容易踩坑的细节。

### 扣减顺序与用量包

每次调用先扣当期订阅月的主额度；主额度用完后自动扣用量包；连用量包也没有或已用完，服务暂停。这时可以升级档位，或等下个订阅月自动重置。

用量包 100 元一包，含 20,000 Credits，需要先有有效订阅才能购买，最多同时持有 5 包。注意它的单价：折合约 50 元/万 Credits，比任何一档主套餐都贵，它是应急用的，别当成省钱手段。

算笔账：每月需要约 45,000 Credits，直接买 Standard（139 元）比 Essential 加一包用量包（79 + 100 = 179 元，45,500 Credits）便宜 40 元，还多了 Harness 权益。连续几个月都要靠用量包撑，就该升档了。拿不准自己的月用量，可以按小档位先开一个月，👉 [在订阅页用量明细里核对实际消耗](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny) 再决定。

### 夜间折扣：把批处理留在 22 点以后

北京时间 22:00 到次日 08:00，qwen3.8-max 和 qwen3.8-flash 的 Credits 消耗打 6 折，deepseek-v4-pro-0813、deepseek-v4-flash-0731、deepseek-v4.1-flash 打 5 折。消耗打 6 折意味着同样的额度能多跑六成多的调用量，跑批处理或长任务时把调度放进夜间窗口，实际能用的量明显更多。折扣是限时活动，以订阅页当前说明为准。

另外 decision-model-preview 目前限时免费，调用不消耗 Credits。不想挑模型时可以用 auto 模型，平台按请求自动匹配底层模型，在质量和成本之间取平衡。

### 视频和异步任务的额度陷阱

视频生成的 Credits 随时长和分辨率上涨，单次消耗远高于文本对话，可能一次就吃掉一大块额度。更隐蔽的是结算方式：视频这类异步任务在提交时不扣费，任务跑完后才一次性结算。短时间内提交多个视频任务，集中结算到账时额度可能瞬间见底。第一次试视频生成，用短时长、低分辨率，先在用量明细里看清单次扣多少再放量。

### 额度按订阅月重置，不累积

额度从订阅日起 30 天一个周期，没用完的不结转到下期，每个订阅月开始时自动恢复满额。顺带说一个近期的变化：2026 年 9 月 22 日起周额度已取消，存量订阅当天被一次性重置为所在档位的满月额度，订阅周期和到期时间不变。旧文章里如果还写着“每周额度”，那条已经过时。

## 和国际版、小米 MiMo 的区别

"Token Plan"这个名字容易撞车，下单前先分清你买的是哪一个。

阿里云国际站（新加坡地域）的 Token Plan 按美元计价，限时价 $6–$68/月，额度机制也不同：按 7 天一个窗口计算，Lite 每窗口 2,500 Credits 起，而不是国内版的 30 天订阅月。人在海外、习惯美元结算可以留意那个版本；要用北京地域的服务，买的就是本文这套人民币方案。

小米 MiMo 也有一个叫 Token Plan 的订阅产品，个人版月付从 ¥39（Lite）到 ¥659（Max），绑定 MiMo 系模型（mimo-v2.6-pro、mimo-v2.6-flash）以及 ASR、TTS。两家的 Credits 体系互不通用，数字没法直接换算，选择基本取决于你想用哪家的模型：跑 Qwen、DeepSeek 系选阿里云这套，明确要用 MiMo 模型才需要看小米的套餐。

## 常见问题

**月额度用完会立刻断服吗？**
不一定。主额度用完后，如果持有有效用量包会先自动扣用量包的 Credits，都没有才暂停。暂停后可以升级档位，或等下个订阅月重置。

**没用完的额度能留到下个月吗？**
不能，按订阅月清零。所以新开通后尽快开始用，别把首月额度放着。

**qwen3.8-max-preview 这个模型 ID 还能用吗？**
能。请求会被自动路由到 qwen3.8-max，按 qwen3.8-max 的费率计 Credits，用量统计也按这个口径。建议尽快把配置里的模型 ID 改过来。

**每次调用扣多少 Credits 在哪查？**
订阅页的用量明细。官方没有统一价目表，消耗由模型类型、token 用量、思考模式、工具调用动态决定。

**Harness 权益要从 Credits 里扣吗？**
分开计量。Standard 和 Pro 包含的 AgentStudio 工具免费额度与后付费折扣不走 Credits，也不占用量包。

## 下单前最后确认两件事

按用量的选择建议：每月 1 万 Credits 以内、以文本对话和轻量编码为主，Lite 足够；用量在 1.2 万到 4 万之间，直接 Essential 或 Standard，别靠单价更贵的用量包硬撑；要 AgentStudio 或多 agent 并行，Standard 起步；高强度工作流加视频生成做得多的，Pro 的单位成本和并发都最宽裕。

付款前在订阅页确认两件事：当期限时价和夜间折扣是否仍在生效，限时活动随时可能调整；订阅周期从付款当天起算，挑一个你能立刻开始用的时间点开通，首月额度才不浪费。

👉 [按你的用量开通对应档位](https://bailian.console.aliyun.com/cn-beijing/subscription/token-plan/personal?userCode=5eqf8rny)
