<h1 align="center">波浪理论 Skill</h1>

<p align="center">中文 | <a href="README.en.md">English</a></p>

一套可直接使用的 AI skill 工具包——把拉尔夫·纳尔逊·艾略特（Ralph Nelson Elliott）《波浪理论》中的波浪判读方法，蒸馏成 15 张可单独触发、也可组合调用的能力卡。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skills 能解决什么问题

- 涨了一大波不知道该在哪清仓——书里说"浪 5 结束的位置决定投资者何时平仓、盈利多少"，但上通道线到底怎么画、破线算不算到顶、量要放大到什么程度，需要有人把这套几何规程落到你自己的图上
- 数浪数出好几个都说得通的方案，不知道该信哪一个，也不知道数错了该怎么发现（原书没有纠错规程，卡片只能判停并如实呈现分歧）
- 调整浪走完了不敢建仓，分不清这段回调是之字形、平台形还是不规则形，更读不出它对后市强弱的预警
- 顶部卖出后它又创了新高，纠结这是趋势恢复还是 B 浪陷阱；或者第五浪根本没创新高，不知道该不该立刻清仓
- 熊市里分不清现在处于哪个阶段，抄底总抄在半山腰；手里有仓位又怕提前下车，缺一套"不到第五浪不卖"的分级规则
- 拿一本讲 1930 年代美股的书往今天的震荡市、垃圾股、非价格数据上硬套，却没有一道"这个标的到底适不适用波浪理论"的闸门

## 蒸馏了什么

15 张能力卡，按"先过闸门、再定坐标、后判终点、最后管持仓"的顺序组织：

- **适用域与读图地基**（3 张）：`applicability-gate-skill`（适用域闸门与使用姿态：形态完备五条件、趋势市限定、右侧确认）、`chart-rules-20`（波浪图 20 条总纲清单）、`multi-timeframe`（多周期研判矩阵与对数 / 算术尺度规则）
- **数浪坐标系**（1 张）：`wave-labeling-skill`（九级浪级标注、驱动浪与调整浪的子浪分解、倾斜规则检验）
- **终点定位与平仓**（4 张）：`wave-five-end-skill`（通道法三步 + 破线 / 天量 / 不规则顶三联证）、`extension-reversal`（延长浪识别与两次反转推演）、`failure-irregular-top-skill`（失败浪与不规则顶：真顶 vs 最高价顶）、`volume-adjudication`（量能验证与形态歧义裁决）
- **调整浪与形态判别**（2 张）：`correction-classifier-skill`（调整浪四分类判别与后市强度预警）、`triangle-alternation`（三角形规则束与交替规则）
- **持仓与建仓**（2 张）：`recursive-hold-skill`（六条递归持有卖出规则）、`bear-diagnosis-skill`（熊市阶段诊断与长线建仓点确认）
- **迁移与心法**（3 张）：`cross-market-sync`（跨市场 / 跨序列同步监测）、`non-price-series`（非价格序列波浪化三招）、`commentary-playbook`（点评者实战心法，非艾略特原文）

## 两种打包模式：single 与 pack

同一套 15 张能力卡，按两种粒度各编译了一次。两者内容完全相同，区别只在"agent 能看到几个入口"。

| | single（单一入口） | pack（compact pack，多入口） |
|---|---|---|
| 可发现入口 | **1 个**：`wave-theory-skill` | **8 个**：1 个来源路由入口 + 7 个已晋级独立 skill |
| 15 张能力卡放在哪 | 全部在入口的 `references/capabilities/` 里，由入口按路由表按需加载 1–2 张 | 7 张高频卡各自独立成 skill；其余 8 张仍在 router 的 `references/` 里 |
| 触发方式 | 只有入口的 description 参与匹配，进入后靠路由表分流 | 7 个高频能力可被 description 直接命中，少一跳 |
| 升级维护 | 替换 1 个目录 | 替换 8 个目录 |

pack 里被晋级为独立 skill 的 7 张卡：

- `wave-five-end-skill` — 第五浪终点与平仓时点
- `wave-labeling-skill` — 数浪与九级浪级标注
- `recursive-hold-skill` — 递归持有与卖出规则
- `correction-classifier-skill` — 调整浪四分类与强度预警
- `failure-irregular-top-skill` — 失败浪与不规则顶
- `bear-diagnosis-skill` — 熊市阶段诊断与长线建仓点
- `applicability-gate-skill` — 适用域闸门与使用姿态

### 该装哪一种

按你的工作方式选，**只装一种**：

| 你的工作方式 | 推荐 | 原因 |
|---|---|---|
| 用 DSH / Codex / Claude Code 等有 skills 目录，希望列表干净 | single | 只占 1 个入口，能力一张不少 |
| 日常问题高度集中在"数浪 / 浪 5 在哪 / 该不该卖 / 这段回调是什么形态 / 这是不是真顶" | pack | 这些正是被晋级的 7 张独立 skill，能直接命中 |
| 要分发给多个 agent 或团队，各自按需取用 | pack | 可以只装其中几个独立 skill，不必整包 |
| 只想装一次、不想维护多个目录 | single | 升级时只替换 1 个目录 |

> 两版由同一个 Bundle 编译，能力内容一致。**同时安装会重复触发**，请只装一种。

## 效果示例

### 示例 1：浪 2 到浪 4 都走完了，怎么定平仓时点

**用户问题**

"这轮涨了快半年，浪 2、浪 3、浪 4 都走完了，现在怎么判断浪 5 什么时候结束、该不该清仓？"

**skill 如何判断**

- 先过 `applicability-gate-skill`：标的要满足形态完备五条件（所有权分散、公开市场、数据可靠、信息可得、可绘图），且处于趋势行情——盘整市里原书明确限定不数浪
- 进 `wave-five-end-skill`：先确认输入契约（标的与操作浪级、浪 1–4 拐点是否已可确认、必须是高低价棒线图、坐标尺度周线用对数 / 日线用算术），再走通道三步——浪 4 结束后连浪 2、浪 4 终点画基准线，过浪 3 顶点作平行上通道线，浪 5 通常止于这条线附近
- 叠加终结三联证：浪 5 是否刺穿上通道线（大浪以上级别须用对数图验证）、破线时成交量是否异常放大（应大于此前同级任何一浪）、以及反向证——未破线就回落则输出"走软预警"
- 持仓者接着用 `recursive-hold-skill` 逐级下钻核对，直到最内层第五浪耗尽
- 判停：浪 5 内部细分出五个子浪（延长浪）→ 转 `extension-reversal`；浪 5 未创新高 → 转 `failure-irregular-top-skill`

**最终回答示例**

> 先说清口径，因为原书没定义、必须你定：拐点取收盘价还是最高/最低价？这一条会直接改变通道落点，两种都行但整轮要统一。坐标上，周线看对数图、日线看算术图。然后按三步画：连浪 2、浪 4 终点为基准线，过浪 3 顶点作平行上通道线，浪 5 大概率落在这条线附近——这是平仓决策区，不是精确卖点，原书对落点只有"附近"这种定性表述，没有量化容差。要确认终结，三条证据一起看：浪 5 有没有刺穿上通道线（这是大浪级别，得用对数图复核）、破线那天量能是不是大于此前同级任何一浪、以及如果它没破线就回落，那只是走软预警，动作是减仓而不是清仓。量能放大到什么程度算"天量"，原书没给阈值，这个数得你自己定并写进预案。如果浪 5 内部还能数出五个子浪，说明这是延长浪，延长浪永远不是终点，改走两次反转推演；如果浪 5 根本没创新高，那是失败浪，B 点附近就该清仓，不要等破线。

### 示例 2：顶部卖出后又创新高，是趋势恢复还是 B 浪陷阱

**用户问题**

"我在顶部已经清了一次仓，结果它又创新高，是不是趋势恢复了？要不要追回来？"

**skill 如何判断**

- 先判停，不进 `failure-irregular-top-skill`：顶后新高既可能是浪 B，也可能是延长浪正在形成，歧义未裁决前不得直接套用，先走 `volume-adjudication` 量能裁决（缩量偏向不规则 B，放量偏向延长浪）
- 裁决为不规则顶后进 `failure-irregular-top-skill` 三步：浪 A = 顶后第一段回落低点；反弹越过常规顶部（OT）创新高 → 浪 B 确认，标注"最高价顶 = B、真顶 = OT"；浪 C 自 B 向下以五浪展开
- 杀跌目标区：先前上涨那轮运动的第五大浪起点附近（结构参照，原书没有幅度公式，输出时必须注明）
- 判停：反弹没有越过 OT → 不是不规则顶，转 `wave-five-end-skill` 走常规终点判定；OT 的价位与日期缺失 → 先问，不猜值

**最终回答示例**

> 先别追。顶后创新高只有两种解释，得先用成交量裁决：缩量创新高偏向不规则 B（那个新高只是浪 B），放量创新高偏向延长浪。假设裁决为不规则顶，那你的真顶其实没变——它是之前的常规顶部 OT，这次的新高只是 B 浪，按原书的说法，从 OT 到 B 的不规则顶部预示一轮剧烈下跌，随后浪 C 会以五浪向下展开。目标区给的是结构参照：先前上涨那轮运动的第五大浪起点附近，不是用幅度算出来的点位。所以正确动作不是追回来，而是要么空仓等浪 C 走完、要么按 `bear-diagnosis-skill` 判断这是熊市的哪个阶段。反过来，如果反弹根本没越过 OT，那就不算不规则顶，回到常规终点判定那条路。另外提醒一句：如果你手上还没有 OT 的价位和日期，这一步做不了，先把这两个数找出来。

## 这些 skill 是怎么生成出来的

这套 skill 使用 **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** 的 RIA-TV++ 流水线生成，整个流程分六个阶段：

1. **整书理解（Adler 分析）**——用 Mortimer Adler 的分析阅读法，对全书做结构、解释、批判、应用四步拆解
2. **并行提取**——同时派多个专项提取器（框架、原则、案例、反例、术语），从原文中提取候选方法论单元
3. **三重验证筛选**——每个候选必须通过三项检验：书内至少有 2 处独立佐证（跨域）、能回答书中未明说的新问题（预测力）、不是常识（独特性）
4. **RIA++ 构造**——按 R（原文引用）/ I（用自己的话重写）/ A1（书中案例）/ A2（未来触发场景）/ E（可执行步骤）/ B（边界与盲点）六个维度结构化
5. **Zettelkasten 链接**——找出能力卡之间的依赖、对比、组合关系，生成能力索引与路由表
6. **触发与输出测试**——为每张卡设计触发盲测题（含诱饵题：该触发时要触发，不该触发时要沉默）与输出评测场景，未通过的卡回炉重做，回炉后再做回归验证

这本 1938 年的原著带一层现代点评（书中以"【点评】"标注），蒸馏时按两个来源分开处理：艾略特原文负责模式、浪级与通道几何；点评者的经验（右侧确认、跟随趋势、休息纪律等）单独成卡 `commentary-playbook`，并在卡内逐条标注"非艾略特原文、证据等级未经核实"。批判字段也直接来自阶段 0 的整书理解——不可证伪风险、幅度维度缺失、量能判据在最需要时失效，这些都写进了各卡的边界（B）字段。

## 测试与验证

本仓库连生成过程的测试材料一起发布：`evals/test-prompts.json` 是用例定义，`evals/test-results.md` 是逐项评分结果。

- **方法**：3 个独立 sub-agent 做盲测，只持路由表与对应能力卡作答，不见预期答案；主流程对照预期判卷
- **用例共 41 条**：should_trigger 13 条（该触发的要触发、要路由到对的卡）、should_not_trigger 7 条（诱饵题：KDJ、市盈率 ROE、MACD、荐股、斐波那契、英超夺冠等，全部应沉默）、edge_case 6 条（浪 3 未走完却要求精确价位、C 浪未走完、清淡市量能、僵尸股等）、output_case 15 条（每张卡一条，要求产出完整交付物）
- **结果**：触发、诱饵、边界、执行四类全部通过，零失败、无回炉，也没有用例从分母里排除
- **抽查到的行为**：盲测者主动发现测试数据里"浪 4 终点低于浪 1 顶"违反重叠规则并声明计数疑点，而不是硬套流程；对不合格计数给出判废与备选方案对照，而不是单一答案；点评经验逐条标注证据等级并声明非艾略特原文

## 仓库结构

```text
wave-theory-skill/
├── README.md                      ← 你正在看的
├── README.en.md                   ← English version
├── LICENSE                        ← MIT
├── BOOK_OVERVIEW.md               ← 整书理解（Adler 四步拆解，阶段 0 产出）
├── verified.md                    ← 15 个规范单元的三重验证结论
├── INDEX.md                       ← skill 地图：能力总表 + 依赖关系 + 加载顺序
├── TEST_SUMMARY.md                ← 阶段 4 压力测试摘要：用例统计 + 结构检查 + 结果口径
├── CANGJIE_ADAPTATION.md          ← 仓颉适配说明：文本状态 / 蒸馏目标 / 证据规则 / 使用边界
├── candidates/                    ← 阶段 1 候选单元（五路并行提取，446 条原始候选，未经筛选）
│   ├── frameworks.md
│   ├── frameworks-part1.md
│   ├── frameworks-part2.md
│   ├── frameworks-part3.md
│   ├── principles.md
│   ├── principles-part1.md
│   ├── principles-part2.md
│   ├── principles-part3.md
│   ├── cases.md
│   ├── cases-part1.md
│   ├── cases-part2.md
│   ├── cases-part3.md
│   ├── counter-examples.md
│   ├── counter-examples-part1.md
│   ├── counter-examples-part2.md
│   ├── counter-examples-part3.md
│   ├── glossary.md
│   ├── glossary-part1.md
│   ├── glossary-part2.md
│   └── glossary-part3.md
├── bundle/                        ← 蒸馏中间产物（可审计）
│   ├── verified.yaml              ← 15 个能力单元的完整规格（本仓库的单一事实来源）
│   ├── cards/
│   │   ├── applicability-gate-skill.md
│   │   ├── bear-diagnosis-skill.md
│   │   ├── chart-rules-20-skill.md
│   │   ├── commentary-playbook-skill.md
│   │   ├── correction-classifier-skill.md
│   │   ├── cross-market-sync-skill.md
│   │   ├── extension-reversal-skill.md
│   │   ├── failure-irregular-top-skill.md
│   │   ├── multi-timeframe-skill.md
│   │   ├── non-price-series-skill.md
│   │   ├── recursive-hold-skill.md
│   │   ├── triangle-alternation-skill.md
│   │   ├── volume-adjudication-skill.md
│   │   ├── wave-five-end-skill.md
│   │   └── wave-labeling-skill.md
│   └── book/
│       ├── overview.md            ← 整书概览
│       └── glossary.md            ← 术语表
├── single/                        ← 单一入口模式
│   └── wave-theory-skill/
│       ├── SKILL.md               ← 入口：触发条件 + 路由表 + 加载规则
│       ├── BUILD_MANIFEST.json    ← 编译清单与文件哈希
│       ├── test-prompts.json      ← 41 条触发 / 诱饵 / 边界 / 执行用例（与 evals/ 同一份副本）
│       └── references/
│           ├── overview.md        ← 整书概览
│           ├── capability-index.md  ← 完整意图与关键词索引
│           ├── cheatsheet.md      ← 决策规则速查
│           ├── glossary.md        ← 术语表
│           └── capabilities/
│               ├── applicability-gate-skill.md
│               ├── bear-diagnosis-skill.md
│               ├── chart-rules-20.md
│               ├── commentary-playbook.md
│               ├── correction-classifier-skill.md
│               ├── cross-market-sync.md
│               ├── extension-reversal.md
│               ├── failure-irregular-top-skill.md
│               ├── multi-timeframe.md
│               ├── non-price-series.md
│               ├── recursive-hold-skill.md
│               ├── triangle-alternation.md
│               ├── volume-adjudication.md
│               ├── wave-five-end-skill.md
│               └── wave-labeling-skill.md
├── pack/                          ← 多入口模式（compact pack）
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── wave-theory-skill-router/
│   │   ├── SKILL.md               ← 来源路由入口
│   │   └── references/
│   │       ├── overview.md        ← 整书概览
│   │       ├── capability-index.md  ← 完整意图与关键词索引
│   │       ├── cheatsheet.md      ← 决策规则速查
│   │       ├── glossary.md        ← 术语表
│   │       └── capabilities/
│   │           ├── applicability-gate-skill.md
│   │           ├── bear-diagnosis-skill.md
│   │           ├── chart-rules-20.md
│   │           ├── commentary-playbook.md
│   │           ├── correction-classifier-skill.md
│   │           ├── cross-market-sync.md
│   │           ├── extension-reversal.md
│   │           ├── failure-irregular-top-skill.md
│   │           ├── multi-timeframe.md
│   │           ├── non-price-series.md
│   │           ├── recursive-hold-skill.md
│   │           ├── triangle-alternation.md
│   │           ├── volume-adjudication.md
│   │           ├── wave-five-end-skill.md
│   │           └── wave-labeling-skill.md
│   ├── wave-five-end-skill/
│   │   └── SKILL.md
│   ├── wave-labeling-skill/
│   │   └── SKILL.md
│   ├── recursive-hold-skill/
│   │   └── SKILL.md
│   ├── correction-classifier-skill/
│   │   └── SKILL.md
│   ├── failure-irregular-top-skill/
│   │   └── SKILL.md
│   ├── bear-diagnosis-skill/
│   │   └── SKILL.md
│   └── applicability-gate-skill/
│       └── SKILL.md
├── （注）← 各 skill 目录均含 test-prompts.json（该能力的触发与边界用例）
└── evals/                          ← 生成过程的测试材料
    ├── test-prompts.json           ← 41 条触发 / 诱饵 / 边界 / 执行用例
    └── test-results.md             ← 逐项评分结果
```

## 如何使用

先把仓库克隆下来：

```bash
git clone https://github.com/raphael-y7/wave-theory-skill.git
```

### 装 single（推荐先试这个）

```bash
# macOS / Linux
cp -r wave-theory-skill/single/wave-theory-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\wave-theory-skill\single\wave-theory-skill "$env:USERPROFILE\.agents\skills\"
```

### 装 pack

只复制含 `SKILL.md` 的目录，不要把 `pack/` 下的两个 json 一起拷进 skills 目录：

```bash
# macOS / Linux
cd wave-theory-skill/pack
cp -r wave-theory-skill-router \
      wave-five-end-skill \
      wave-labeling-skill \
      recursive-hold-skill \
      correction-classifier-skill \
      failure-irregular-top-skill \
      bear-diagnosis-skill \
      applicability-gate-skill ~/.agents/skills/
```

```powershell
# Windows
$pack = ".\wave-theory-skill\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('wave-theory-skill-router','wave-five-end-skill','wave-labeling-skill','recursive-hold-skill','correction-classifier-skill','failure-irregular-top-skill','bear-diagnosis-skill','applicability-gate-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` 是 DSH 的 skill 目录；用别的 agent 时换成它自己的 skills 目录即可（例如 Claude Code 是 `~/.claude/skills`）。

### 怎么确认装好了

装完问一句"这轮涨势的浪 5 大概在哪结束、我该什么时候清仓"，看 agent 是否直接进入通道三步作图与破线 / 天量三联证，而不是给你一段泛泛的"注意风险、控制仓位"。装的是 single 时，它会先读入口再按路由表进 `wave-five-end-skill`；装的是 pack 时，这张能力会被直接命中。

## 来源

- 《波浪理论》拉尔夫·纳尔逊·艾略特（Ralph Nelson Elliott）著
- 全书蒸馏，共产出 15 张能力卡

## 声明

本仓库只发布蒸馏后的 skill、索引与规则速查材料，不包含原书 PDF、EPUB、OCR 文件、截图或全书转写稿。能力卡中出现的原文引用仅用于标注方法论出处和保持可审计性。

书中所有判据（通道"附近"的容差、天量的成交量阈值、三角形"画满"的判定、换手率经验值等）都是原书案例与经验归纳，作者未提供统计回测背书；点评者给出的部分参数（斐波那契参数、换手率 7% 等）在蒸馏时已标注为未经核实。使用时需按标的自行测试并声明所用口径。波浪理论本身在学界存在"不可证伪"的争议，本仓库把这类批判如实写进了每张卡的边界字段（见 `BOOK_OVERVIEW.md` 第 3 节）。本仓库内容不构成投资建议。

## License

[MIT](./LICENSE)
