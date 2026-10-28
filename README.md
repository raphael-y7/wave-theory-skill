<h1 align="center">波浪理论 Skill</h1>

<p align="center">中文 | <a href="README.en.md">English</a></p>

一套可直接使用的 AI skill 工具包——把 R.N. 艾略特《波浪理论（专业解读版）》里的数浪、通道作图与卖出规程，蒸馏成 15 张可单独触发、也可组合调用的能力卡。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skills 能解决什么问题

- 一段上涨到底数到第几浪、现在该不该走：浪 4 走完后用最终通道把浪 5 终点框成一个可复述的几何位置，而不是凭感觉猜顶
- 已经建仓、怕提前下车：按六条递归持有规则逐级下钻（中浪→小浪→细浪→微浪），本级第五浪没走完就不卖，走完再拿"破上通道线 + 同级天量"双证确认
- 这段回调是之字形、平台形还是不规则形，形态走完之后对后面行情的强弱意味着什么
- 顶后回落又创了新高，到底是新一波上涨还是 B 浪诱多（不规则顶 / 失败浪），真顶该认哪一个
- 大级别跌了一年，现在处在熊市六段序列的哪一段，长线建仓点该等什么确认信号
- 这套理论到底适不适用于我手上这个品种、这段行情：先过五条件闸门与"有趋势才数浪"的行情层过滤，避免在震荡市里硬套

## 蒸馏了什么

15 张能力卡，按"先过闸门、再建坐标、最后定位终点与处置异常"的顺序组织：

- **前置闸门与读图总纲**：`applicability-gate-skill`（波浪理论适用域闸门与使用姿态）、`chart-rules-20`（波浪图 20 条总纲清单）
- **数浪与浪级坐标**：`wave-labeling-skill`（波浪计数与九级浪级标注规范）
- **终点定位与卖出**：`wave-five-end-skill`（第五浪终点定位与终结判定：通道法三步 + 三联证）、`recursive-hold-skill`（六条递归持有卖出规则）
- **调整形态与异常收场**：`correction-classifier-skill`（调整浪四分类判别与强度预警）、`triangle-alternation`（三角形判别与交替规则）、`extension-reversal`（延长浪识别与两次反转推演）、`failure-irregular-top-skill`（失败浪与不规则顶应对）
- **熊市诊断与建仓**：`bear-diagnosis-skill`（熊市阶段诊断与长线建仓点确认）
- **第二证据链与边界场景**：`volume-adjudication`（量能验证与形态歧义裁决）、`multi-timeframe`（多周期研判与图表尺度规则）、`cross-market-sync`（跨市场同步监测）、`non-price-series`（非价格序列波浪化三招）、`commentary-playbook`（点评者实战心法，张艺博，非艾略特原文）

## 两种打包模式：single 与 pack

同一套 15 张能力卡，按两种粒度各编译了一次。两者内容完全相同，区别只在"agent 能看到几个入口"。

| | single（单一入口） | pack（compact pack，多入口） |
|---|---|---|
| 可发现入口 | **1 个**：`wave-theory-skill` | **8 个**：1 个来源路由入口 + 7 个已晋级独立 skill |
| 15 张能力卡放在哪 | 全部在入口的 `references/capabilities/` 里，由入口按路由表按需加载 1 张（跨域最多 2 张） | 7 张各自独立成 skill；其余 8 张仍在 router 的 `references/` 里 |
| 触发方式 | 只有入口的 description 参与匹配，进入后靠路由表分流 | 7 个高频能力可被 description 直接命中，少一跳 |
| 升级维护 | 替换 1 个目录 | 替换 8 个目录 |

pack 里被晋级为独立 skill 的 7 张卡：

- `wave-five-end-skill` — 第五浪终点定位与终结判定（通道法三步 + 三联证）
- `wave-labeling-skill` — 波浪计数与九级浪级标注规范
- `recursive-hold-skill` — 六条递归持有卖出规则
- `correction-classifier-skill` — 调整浪四分类判别与强度预警
- `failure-irregular-top-skill` — 失败浪与不规则顶应对
- `bear-diagnosis-skill` — 熊市阶段诊断与长线建仓点确认
- `applicability-gate-skill` — 波浪理论适用域闸门与使用姿态

### 该装哪一种

按你的工作方式选，**只装一种**：

| 你的工作方式 | 推荐 | 原因 |
|---|---|---|
| 用 DSH / Codex / Claude Code 等有 skills 目录，希望列表干净 | single | 只占 1 个入口，能力一张不少 |
| 日常问题高度集中在"数浪 / 浪 5 终点 / 该不该卖 / 调整形态 / 异常顶 / 熊市建仓 / 能不能用" | pack | 这 7 类正是被晋级的独立 skill，能直接命中 |
| 要分发给多个 agent 或团队，各自按需取用 | pack | 可以只装其中几个独立 skill，不必整包 |
| 只想装一次、不想维护多个目录 | single | 升级时只替换 1 个目录 |

> 两版由同一个 Bundle 编译，能力内容一致。**同时安装会重复触发**，请只装一种。

## 效果示例

### 示例 1：浪 4 刚走完，想提前框出浪 5 终点和清仓区

**用户问题**

"这波涨了很久，浪 2、浪 3、浪 4 我觉得都走完了，浪 5 大概到哪？什么时候该清仓？"

**skill 如何判断**

- `wave-five-end-skill` 先要输入契约：标的与操作浪级、浪 1–4 拐点、高低价棒线数据、坐标尺度（周线用对数、日线/60 分钟用算术）
- 按三步作图：浪 2 走完连 M-O 为基准线、过浪 1 顶点 N 作平行上通道线；浪 3 结束后**无论触线、穿线还是未达线，旧通道一律作废**，连 N-P 为新上通道线、过 O 作新基准线；浪 4 结束后连 O-Q 为基准线、过浪 3 顶点 P 作平行线，得到最终通道
- 浪 5 通常止于最终上通道线附近，这个落点就是平仓决策区
- 叠加三联证：浪 5 是否刺穿上通道线、破线时成交量是否明显放大、以及反向证（未破线却回落 = 走软预警）

**最终回答示例**

> 先把口径定下来，不然画出来的通道不算数：拐点用收盘价还是最高/最低价，原书没有定义，你得选一种并记住它。然后确认浪 1–4 的拐点是否真能辨认——辨认不了就别硬画。按你的浪级，最终通道是连浪 2 终点 O 和浪 4 终点 Q 作基准线、过浪 3 顶点 P 作平行上通道线，浪 5 的终点区就落在这一带。
>
> 但"附近"是定性说法，书里没给容差，别把它当成精确挂单价。要确认终结，再看三条：一、浪 5 有没有刺穿上通道线（大浪以上级别要用对数图验证）；二、破线时成交量有没有明显放大——书里只说"大浪第五浪会出现大于此前同级任何一浪的成交量"，**没有给具体倍数阈值，这个数得你自己定并写进预案**；三、如果浪 5 根本没破线就回落，那不是正常整理，是走软预警，调整幅度按浪级估。
>
> 还有一个坑：破线不等于立刻见顶，书里明说"有时在突破点附近，第五浪不会很快结束"，见破线就清仓会错过末段。所以动作是分批：破线 + 天量确认后减第一笔，剩下按递归持有规则逐级核对。另外提醒一句，这套方法全书没有止损规程，也没有幅度算法，它给的是决策参考，不是完整风控闭环。

### 示例 2：这段回调算哪一类调整，走完之后是强还是弱

**用户问题**

"从顶上一路跌下来，中间反弹了一下又跌，这算之字形还是平台形？跌完还能涨吗？"

**skill 如何判断**

- `correction-classifier-skill` 先做完成度检查：如果 C 浪还没展开、起点也没定，**直接判停**——作者自认调整浪形成过程中很难准确预测形态与幅度，这张卡是"走完后的预警器"，不是事前预测器
- 形态走完后只读两个相对位置：浪 B 相对调整起点（回到 / 越过 / 没回来）、浪 C 相对浪 A 低点（创新低 / 持平 / 更高）
- 四类落型：B 明显低于起点且 C 创新低 = 之字形；B 回到起点且 C 与 A 持平 = 平台形；B 越过起点创新高且 C 跌破 A = 不规则形(1)；B 不创新高且 C 不破 A = 不规则形(2)
- 强度分级：之字形 = 后市一般；平台形 = 较长强劲波动；调整终点明显高于 a 低点 = 超级强势。熊市反弹按同一几何镜像评估，B 失守起点且 C 乏力 = 超级弱势

**最终回答示例**

> 先回答"能不能涨"这个问题之前，得先看你的 A-B-C 走完了没有。如果 C 浪还在跌、低点还没出来，那现在判型就是抢跑——书里作者自己说了，调整浪在形成过程中"很难准确预测其具体形态和波动幅度"，所以这张卡的定位是走完之后的预警，不是事前押注。
>
> 假设 C 已经走完，只看两个读数：浪 B 有没有回到调整起点，浪 C 相对浪 A 低点在哪。B 明显低于起点、C 创了新低，那是之字形，后市强度一般；B 回到起点附近、C 和 A 大致同一水平，是平台形，书里说这预示"一段时间较长的强劲波动"。
>
> 两个必须照实说的地方：一、"回到起点""创了新低"这些边界怎么算，原书没有给量化容差，得你事先约定一个口径；二、"平台形 = 强势"这条，书里能指认的实证其实只有 1933 年 7 月到 1934 年 7 月那一例大浪 4，属于事后标注、没有频率统计。所以强度档位只能当预警参考，不能当幅度或点位预测用，更不构成入场指令。另外如果你说的"跌下来"里是个收敛三角形，那要走 `triangle-alternation` 那张卡，不在这四分类里。

## 这些 skill 是怎么生成出来的

这套 skill 使用 **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** 的 RIA-TV++ 流水线生成，整个流程分六个阶段：

1. **整书理解（Adler 分析）**——用 Mortimer Adler 的分析阅读法，对全书做结构、解释、批判、应用四步拆解
2. **并行提取**——同时派多个专项提取器（框架、原则、案例、反例、术语），从原文中提取候选方法论单元
3. **三重验证筛选**——每个候选必须通过三项检验：书内至少有 2 处独立佐证（跨域）、能回答书中未明说的新问题（预测力）、不是常识（独特性）
4. **RIA++ 构造**——按 R（原文引用）/ I（用自己的话重写）/ A1（书中案例）/ A2（未来触发场景）/ E（可执行步骤）/ B（边界与盲点）六个维度结构化
5. **Zettelkasten 链接**——找出能力卡之间的依赖、对比、组合关系，生成能力索引与路由表
6. **触发与输出测试**——为每张卡设计触发盲测题（含诱饵题：该触发时要触发，不该触发时要沉默）与输出评测场景，未通过的卡回炉重做，回炉后再做回归验证

这本书的蒸馏难点在于"作者主张"与"证据强度"必须分开标注：原书全部浪标都画在既成走势上，且"预测到日和小时"的承诺被点评者判定不可兑现，所以每张卡都带边界与盲点段，把"书里说了什么"和"这条有多可信"分两栏写。

## 测试与验证

本仓库连生成过程的测试材料一起发布：`evals/test-prompts.json` 是固定用例集，`evals/test-results.md` 是逐项判卷结果——包含方法、分项通过数与关键执行质量抽查，不是只留一句"全部通过"。

- **盲测方法**：3 个独立 sub-agent（T1/T2/T3，未参与蒸馏）只持路由表与对应能力卡作答，主流程对照预设预期判卷
- **用例集实际条数**：`evals/test-prompts.json` 共 41 条 = 13 条触发 + 7 条诱饵 + 6 条边界 + 15 条实际执行
- **判卷记录的分项通过数**（照 `evals/test-results.md` 原文）：should_trigger 22 / 22、should_not_trigger 6 / 6（零误激活）、edge_case 8 / 8、output_case 15 / 15
- **计数口径差异照实说明**：判卷记录自述总用例数为 39，其四类分项相加为 51，与随仓库发布的用例集 41 条并不一致。这是原始材料的计数口径差异，本仓库没有调平、没有改写，也没有据此推算通过率
- **失败与回炉**：记录为无。没有修改预期答案的情况，也没有用例从分母排除
- **质量抽查**：盲测者主动发现测试数据中"浪 4 终点 105 低于浪 1 顶 110"违反重叠规则，在交付物里声明计数疑点而不是硬套流程；对不合格计数给出"判废"与备选方案对照而非单一答案

## 仓库结构

```text
wave-theory-skill/
├── README.md                      ← 你正在看的
├── README.en.md                   ← English version
├── LICENSE                        ← MIT
├── BOOK_OVERVIEW.md               ← 整书理解（Adler 四步拆解，阶段 0 产出）
├── verified.md                    ← 三重验证结论：通过验证的方法单元与证据素材清单
├── single/                        ← 单一入口模式
│   └── wave-theory-skill/
│       ├── SKILL.md               ← 入口：触发条件 + 路由表 + 加载规则
│       ├── BUILD_MANIFEST.json    ← 编译清单与文件哈希
│       └── references/
│           ├── overview.md        ← 整书概览
│           ├── capability-index.md  ← 完整意图与关键词索引（15 张卡逐条登记）
│           ├── cheatsheet.md      ← 决策规则速查
│           ├── glossary.md        ← 术语表
│           └── capabilities/      ← 15 张能力卡
├── pack/                          ← 多入口模式（compact pack）
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── wave-theory-skill-router/
│   │   ├── SKILL.md               ← 来源路由入口
│   │   └── references/            ← 15 张卡 + 索引，供 router 内部调用
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
└── evals/                          ← 触发盲测与输出评测材料
    ├── test-results.md             ← 逐项评分与质量抽查记录
    └── test-prompts.json           ← 39 条固定用例（触发 / 诱饵 / 边界 / 执行）
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

装完问一句"浪 4 走完了，帮我画通道定浪 5 的终点和清仓区"，看 agent 是否直接进入通道三步作图与三联证核对，而不是给你一段泛泛的"注意风险、控制仓位"。装的是 single 时，它会先读入口再按路由表进能力卡；装的是 pack 时，`wave-five-end-skill` 会被 description 直接命中。

## 来源

- 《波浪理论（专业解读版） The Wave Principle》[美] 拉尔夫·纳尔逊·艾略特（Ralph Nelson Elliott）著，段会青 译，张艺博 点评；原著 1938 年，中译本由人民邮电出版社出版（股票投资百年经典译丛）
- 全书蒸馏产出 15 张能力卡
- 原书样本取自 1854–1938 年美股，密集集中在 1921–1938 年道琼斯指数，没有一个 A 股案例；迁移到 A 股时浪级对应关系、成交量口径与 T+1 制度差异都需自行重新校准
- 点评者内容（`commentary-playbook` 卡内的张艺博观点、以及各卡标注【点评】的段落）不是艾略特原文，卡内已逐条标注来源等级

## 声明

本仓库只发布蒸馏后的 skill、索引与规则速查材料，不包含原书 PDF、EPUB、OCR 文件、截图或全书转写稿。能力卡中出现的原文引用仅用于标注方法论出处和保持可审计性。

书中所有数字判据（通道"附近"的容差、天量倍数、调整浪判型边界、换手率 7% 等）都是案例与经验归纳，原书未提供统计回测背书，多处阈值原书根本没有给出，使用时需按标的自行测试并声明所用口径。本仓库内容不构成投资建议。

## License

[MIT](https://opensource.org/licenses/MIT)
