# Skill 地图 — 波浪理论

一句话说明：这是 15 张能力卡的入口地图——先在能力总表里按意图定位卡，再看依赖关系决定补读哪一张，最后按加载顺序执行；完整规格见 [`bundle/verified.yaml`](./bundle/verified.yaml)。

## 能力总表

| capability_id | slug | 中文标题 | 重要度 | 去向 |
|---|---|---|---|---|
| `cap.elliott-wave.wave-five-end-skill` | `wave-five-end-skill` | 第五浪终点定位与终结判定（通道法三步+三联证） | critical | promoted → 独立 skill |
| `cap.elliott-wave.wave-labeling-skill` | `wave-labeling-skill` | 波浪计数与九级浪级标注规范 | critical | promoted → 独立 skill |
| `cap.elliott-wave.recursive-hold-skill` | `recursive-hold-skill` | 六条递归持有卖出规则 | critical | promoted → 独立 skill |
| `cap.elliott-wave.correction-classifier-skill` | `correction-classifier-skill` | 调整浪四分类判别与强度预警 | high | promoted → 独立 skill |
| `cap.elliott-wave.extension-reversal` | `extension-reversal` | 延长浪识别与两次反转推演 | high | router → 路由入口 |
| `cap.elliott-wave.volume-adjudication` | `volume-adjudication` | 量能验证与形态歧义裁决 | high | router → 路由入口 |
| `cap.elliott-wave.triangle-alternation` | `triangle-alternation` | 三角形判别与交替规则 | medium | router → 路由入口 |
| `cap.elliott-wave.failure-irregular-top-skill` | `failure-irregular-top-skill` | 失败浪与不规则顶应对 | high | promoted → 独立 skill |
| `cap.elliott-wave.bear-diagnosis-skill` | `bear-diagnosis-skill` | 熊市阶段诊断与长线建仓点确认 | critical | promoted → 独立 skill |
| `cap.elliott-wave.multi-timeframe` | `multi-timeframe` | 多周期研判与图表尺度规则 | medium | router → 路由入口 |
| `cap.elliott-wave.chart-rules-20` | `chart-rules-20` | 波浪图20条总纲清单 | medium | router → 路由入口 |
| `cap.elliott-wave.cross-market-sync` | `cross-market-sync` | 跨市场同步监测 | medium | router → 路由入口 |
| `cap.elliott-wave.non-price-series` | `non-price-series` | 非价格序列波浪化三招 | medium | router → 路由入口 |
| `cap.elliott-wave.applicability-gate-skill` | `applicability-gate-skill` | 波浪理论适用域闸门与使用姿态 | high | promoted → 独立 skill |
| `cap.elliott-wave.commentary-playbook` | `commentary-playbook` | 点评者实战心法（点评者，非艾略特原文） | low | router → 路由入口 |

- **promoted → 独立 skill**（7 张）：在 pack 模式下各自是一个带 `SKILL.md` 的独立目录，可被 description 直接命中；在 single 模式下仍是入口内部的一张卡。
- **router → 路由入口**（8 张）：pack 模式下只存在于 `wave-theory-skill-router/references/capabilities/`，由路由表按意图加载。

## 依赖关系（also_read）

下表列出 `verified.yaml` 中每张卡声明的 `also_read`，即在主卡执行完之后建议补读的卡（方向按 yaml 记录，未做对称展开）：

| 主卡 | 建议补读（also_read） |
|---|---|
| `wave-five-end-skill` | `recursive-hold-skill`、`failure-irregular-top-skill`、`volume-adjudication`、`multi-timeframe`、`wave-labeling-skill` |
| `wave-labeling-skill` | `wave-five-end-skill`、`applicability-gate-skill`、`recursive-hold-skill` |
| `recursive-hold-skill` | `wave-five-end-skill`、`bear-diagnosis-skill` |
| `correction-classifier-skill` | `triangle-alternation`、`recursive-hold-skill`、`wave-labeling-skill` |
| `extension-reversal` | `volume-adjudication`、`failure-irregular-top-skill` |
| `volume-adjudication` | `extension-reversal`、`wave-five-end-skill`、`multi-timeframe` |
| `triangle-alternation` | `correction-classifier-skill`、`wave-labeling-skill` |
| `failure-irregular-top-skill` | `extension-reversal`、`bear-diagnosis-skill`、`wave-five-end-skill` |
| `bear-diagnosis-skill` | `failure-irregular-top-skill`、`recursive-hold-skill`、`correction-classifier-skill` |
| `multi-timeframe` | `wave-five-end-skill`、`chart-rules-20` |
| `chart-rules-20` | `multi-timeframe`、`applicability-gate-skill` |
| `cross-market-sync` | `non-price-series`、`bear-diagnosis-skill` |
| `non-price-series` | `cross-market-sync` |
| `applicability-gate-skill` | `commentary-playbook`、`wave-labeling-skill` |
| `commentary-playbook` | `applicability-gate-skill`、`volume-adjudication` |

几条成环的强依赖，实际使用时按这个顺序读：

- **坐标系 → 终点 → 持仓**：`wave-labeling-skill` → `wave-five-end-skill` → `recursive-hold-skill`（数浪是画通道的前提，通道落点是持有规则的前提）
- **终点异常形态**：`volume-adjudication`（先裁决歧义）→ `extension-reversal`（延长浪两次反转）／`failure-irregular-top-skill`（失败浪与不规则顶）
- **调整与形态**：`wave-labeling-skill` → `correction-classifier-skill` ⇄ `triangle-alternation`
- **闸门与心法**：`applicability-gate-skill` ⇄ `commentary-playbook`（点评者经验必须标注非艾略特原文）

## 加载顺序

1. **先读入口 `SKILL.md`**：single 模式读 `single/wave-theory-skill/SKILL.md`，pack 模式读 `pack/wave-theory-skill-router/SKILL.md`。入口里有「触发与不触发」「核心原则」「能力路由表」「加载规则」「边界与判停」五段，概览类问题读到核心原则即可回答，不必加载能力卡。
2. **按路由表加载 1 张卡**：拿用户意图去匹配路由表的「用户意图」列，命中后只加载对应的那一张卡（`references/capabilities/<slug>.md`）。
3. **最多补读 1 张**：任务确实跨域时（例如既要在浪 5 终点平仓、又要判断这是不是不规则顶），按上表的 `also_read` 再加载 1 张，总数不超过 2 张。
4. **非能力类查询走索引**：书名/作者/章节/整书概览 → `references/overview.md`；术语 → `references/glossary.md`；决策规则速查 → `references/cheatsheet.md`；路由表未覆盖的意图 → `references/capability-index.md`。
5. **判停**：路由表与索引都无法命中的意图，明确告知超出本书范围；数浪出现多个自洽矛盾方案且无法用通道/量能/周期裁决时，停止下结论并如实呈现分歧。
