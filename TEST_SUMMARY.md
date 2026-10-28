# Stage 4 压力测试摘要

本文件汇总《波浪理论（专业解读版）》能力包在阶段 4（触发与输出压力测试）留下的用例、结构与结果记录。用例类数字由脚本对本仓库内的用例文件逐文件实测得出（累加值、去重值、按 type 的分类计数均为直接统计）；通过情况照录归档中的判卷记录原文。

## 测试范围

- **skill 数量**：15 张能力卡（`bundle/cards/` 15 个文件，编译后 `single/` 与 `pack/` 各 15 份 `references/capabilities/`）。可发现入口：single 模式 1 个（`wave-theory-skill`），pack 模式 8 个（1 个 router + 7 个晋级独立 skill）。
- **test-prompts 文件数量**：全仓库实测 9 个 `test-prompts.json` —— `single/wave-theory-skill/` 1 个（入口级全量用例），`pack/` 下 8 个 skill 目录各 1 个（其中 `pack/wave-theory-skill-router/` 那份是入口级用例的逐字节副本，7 个晋级 skill 各带本能力相关的子集用例）。
- **用例条数**：按 9 个文件累加共 100 条；去重后为 41 条独立用例，编号 T1-A*/T1-B*/T1-C*、T2-*、T3-*，按三个盲测批次（T1/T2/T3）分组。`pack/` 下 8 份用例全部取自这 41 条（router 是整份副本，7 个晋级 skill 是子集），因此累加值远大于独立用例数。
- **覆盖类型**：

| 类型 | 条数（按文件累加） | 条数（去重后） | 说明 |
|---|---|---|---|
| should_trigger | 34 | 13 | 该触发时要触发，并路由到正确的能力卡 |
| should_not_trigger | 14 | 7 | 诱饵题（KDJ 金叉、市盈率 ROE、MACD 顶背离、荐股、斐波那契数列、英超夺冠、波浪理论作者与年代），应保持沉默 |
| edge_case | 15 | 6 | 边界处理：只有浪 1 浪 2 且浪 3 未走完却要精确价位（T1-C1）、调整浪 B 反弹创新高（T1-C2）、极清淡市用缩量/放量裁决歧义（T2-C1）、日线与 60 分钟冲突时哪个为准（T2-C2）、僵尸股数浪（T3-C1）、把点评经验当艾略特原文引用（T3-C2） |
| output_case | 37 | 15 | 每张能力卡一条，要求产出完整交付物（通道判定记录、数浪标注表、持有卖出表、调整判别卡、量能裁决、三角清单、顶态判定、熊市诊断、图表配置、20 条清单、同步判读、序列方案、闸门结论、心法标注等） |
| **合计** | **100** | **41** | — |

- **覆盖度**：去重后 41 条用例共涉及 15 个不同 capability 字段，与 15 张能力卡一一对应，无卡片缺用例。

## 结构检查

以下为对本仓库当前文件实测的结果（2026-10-29 于本仓库目录逐项检查）：

- **JSON 可解析性**：全仓库 9 个 `test-prompts.json` 逐个交给 JSON 解析器验证，**9/9 全部可解析，可解析数等于文件数**。`single/wave-theory-skill/test-prompts.json` 顶层字段为 `skill` / `version` / `mode` / `test_date` / `method` / `test_cases`，`test_cases` 长度 41；7 个晋级 skill 的文件顶层字段为 `skill` / `version` / `test_cases`（无 `mode`），`test_cases` 长度分别为 `wave-five-end-skill` 3、`wave-labeling-skill` 2、`recursive-hold-skill` 3、`correction-classifier-skill` 4、`failure-irregular-top-skill` 1、`bear-diagnosis-skill` 2、`applicability-gate-skill` 3；`pack/wave-theory-skill-router/test-prompts.json` 与 single 入口那份逐字节一致（SHA-256 相同），长度同为 41。
- **frontmatter**：9 个 `SKILL.md`（single 入口 1 个 + pack 入口 8 个）全部以 `---` 开头，且都含 `name:` 与 `description:` 两个必需字段；9 个 `name:` 的值均与所在目录名一致；single 入口另带 `cangjie.*` 生成元数据（变体、bundle-id、能力数 15、入口数 1）。
- **六段完整性**：`bundle/cards/` 的 15 张卡全部具备 `## R —`（原文依据）、`## I —`（方法论自述）、`## A1 —`（书中案例）、`## A2 —`（未来触发场景）、`## E —`（可执行步骤）、`## B —`（边界与盲点）六个段落，缺段数为 0；编译后的 `single/.../references/capabilities/` 15 份与 `pack/wave-theory-skill-router/references/capabilities/` 15 份同样六段齐全（各 15/15）。
- **引用长度**：卡片内以 `> "…"` 形式标记的原文引用共 42 条，其中 1 条超过 120 字（第三章通道三步作图规程的整段引用，属规程性长引，已标注章节与图号）。
- **编译清单**：`single/wave-theory-skill/BUILD_MANIFEST.json`、`pack/BUILD_MANIFEST.json`、`pack/capability-destinations.json` 均在位。

## 结果

- skills: 15
- test_json: 9（可解析 9）
- 用例条数：按文件累加 100 条，去重后 41 条独立用例
- 通过情况：**本仓库根目录的判卷记录（`test-results.md`）记载为四类全过、零失败、无回炉**——should_trigger 22/22、should_not_trigger 6/6、edge_case 8/8、output_case 15/15，合计 39 条，并注明「无修改预期答案的情况；无用例从分母排除」。
- **口径不一致，照实记录**：该判卷记录的分类计数为 22 + 6 + 8 + 15 = 39 条，而本仓库 `test-prompts.json` 实测为累加 100 条（34 / 14 / 15 / 37）、去重后 41 条（13 / 7 / 6 / 15）。两者条数与分类分布都对不上，无法判定哪一份是最新口径，因此本摘要**不据以换算通过率、也不推算百分比**；上列的 22/22 等分数按判卷记录原文照录，仅说明「判卷记录声称该批用例全过」，不等同于对当前 41 条用例的通过结论。
- **未记录项**：`test-results.md` 未记录逐条用例的单独判定表，也未附盲测原始记录——`PIPELINE_STATE.md` 提到的 `stage4/raw-T1.md`、`raw-T2.md`、`raw-T3.md` 在归档目录中并不存在（归档的 `Bundle/runs/` 下只有两次编译运行的 `output-decision.*` 与 `staging-validation.log`），故无法对单条用例复核。

## 可接入 darwin-skill 的后续动作

- 这 41 条独立用例（9 个文件去重后）可直接作为 darwin-skill 的回归样本（ratcheting 基线）：触发类（should_trigger / should_not_trigger）用于守住路由与沉默边界，边界类（edge_case）用于守住判停与降级行为，输出类（output_case）用于守住每张卡的交付物完整性。
- 接入前建议先做一件事：把判卷记录与用例文件的条数口径对齐（39 vs 41），否则 ratcheting 的基线分母不稳定，回归时会出现「分母变了但没人改题」的假波动。
- 输出类用例目前只写 `expected_behavior` 的自然语言预期，没有可机器判定的断言（如必备字段、必备段落）。若要接入自动评分，需先为 15 条 output_case 补上结构化断言，否则只能人工判卷。
- 归档中提到的进化入口为 `darwin evolve books/wave-theory-skill/`（以 `test-prompts.json` 做 ratcheting），该命令未在本仓库内验证执行。
