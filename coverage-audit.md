# coverage-audit.md — 覆盖审计（阶段 1.5）

基准：BOOK_OVERVIEW.md 原书关键任务清单（task-01~16，来自阶段 0，不从旧 verified 反推）。
核查方式：全量扫描候选池（446 条）+ 验证裁决（stage1.5/*-verdicts.md）对照本表。

| task_id | 任务 | 原文位置 | 主要候选（id） | decision | 最终去向（能力卡/参考） |
|---|---|---|---|---|---|
| task-01 | 判定一轮运动终点（浪5定位/平仓） | 第三章末+图11；第七章2-7；第八章 | f-p1-11, f-p3-04, f-p3-05, p-p1-25/27, p-p2-03/09/10, p-p3-04/23/24, c-p1-17 | verified | cap.wave-five-end-skill（通道法+终点判定） |
| task-02 | 浪2后预画通道锁定框架 | 第三章图7-9 | f-p1-11, p-p1-24/26, p-p3-03/24, c-p1-13~15 | verified | cap.wave-five-end-skill |
| task-03 | 单标的独立数浪+九级浪级标注 | 第一章末；第四章表1、图12-14 | f-p2-01, f-p1-03, p-p2-01/02, p-p1-07/29/30, c-p2-01~03, c-p1-08 | verified | cap.wave-labeling-skill |
| task-04 | 驱动/调整浪分解与当前浪位判定 | 第三章图3-5 | f-p1-05/06/09/10, p-p1-10/14~22, c-p1-09~12 | verified | cap.wave-labeling-skill |
| task-05 | 第五浪终结信号验证（破线+天量） | 第五章图17-19；第八章规则5-6 | f-p2-04, p-p2-11/12/13/14, p-p3-30/31, c-p2-07/08/09 | verified | cap.wave-five-end-skill |
| task-06 | 调整浪四分类+强度预期 | 第五章图20-29、35-41 | f-p2-10/11, p-p2-16/17/31/32, c-p2-11~21/35~41 | verified | cap.correction-classifier-skill |
| task-07 | 延长浪识别+两次反转推演 | 第五章(1)-(8)+图32+表2 | f-p2-07/08/09, p-p2-15/18~28, c-p2-22~32, x-p2-07/08 | verified | cap.extension-reversal |
| task-08 | 量能裁决歧义走势 | 第五章图43+第六章 | f-p2-12/16, p-p2-34/53~58/64, c-p2-43, x-p2-21/22 | verified | cap.volume-adjudication |
| task-09 | 三角形完整判别 | 第五章图44-51 | f-p2-13/14, p-p2-35~44, c-p2-44~51, x-p2-12~15 | verified | cap.triangle-alternation |
| task-10 | 20条图法读图自查 | 第七章1-20条 | p-p3-01~20, f-p3-05/06, c-p3-01/02, x-p3-02 | verified | cap.chart-rules-20 |
| task-11 | 六条递归卖出规则 | 第八章规则1-6 | f-p3-01, p-p3-23/26~31/33, c-p3-06~11, x-p3-08/09 | verified | cap.recursive-hold-skill |
| task-12 | 熊市阶段诊断+长线建仓点 | 第九章图62-68；第八章开篇 | f-p3-02/03, p-p3-34~39, c-p3-12~19, x-p3-03/11~13 | verified | cap.bear-diagnosis-skill |
| task-13 | 多周期+图表尺度配合 | 第七章9-13；图19 | f-p2-05/06, p-p2-14/52/58, p-p3-09~13, c-p2-09/52/53, x-p2-06 | verified | cap.multi-timeframe |
| task-14 | 非价格序列波浪化 | 第七章16-18；第十章 | f-p3-07/10, p-p3-16/17/18/40/41, c-p3-03/22~31, c-p1-02 | verified | cap.non-price-series |
| task-15 | 跨市场/跨序列同步监测 | 第七章1/19/20；表3 | f-p3-08, p-p3-01/19/20/42, c-p3-01/02/32/33, p-p1-29/30 | verified | cap.cross-market-sync |
| task-16 | 波段操作机会 | 第一章373%段；第六章 | f-p2-06/22, p-p1-09, p-p2-47/62/66/68, c-p1-06 | verified | cap.commentary-playbook（点评者经验，明确标注）+ cap.multi-timeframe |

## 任务级缺口登记（不虚报零遗漏）

1. **止损规则**：全书未提供（task-11 尚缺条件，阶段0已记录）→ 能力卡 B 段声明"本书不含止损规程"。
2. **量能阈值量化**：艾略特未给大小阈值；点评者 7% 为无出处经验值（p-p2-64/x-p2-24 已标）→ 卡内标"经验值无出处"。
3. **幅度算法**：延长浪/终点无点位算法（f-p3-13 斐波那契为点评经验、needs_review；f-p2-19 比率构造缺失 needs_review）→ needs-review.md 跟踪。
4. **浪2终点确认标准 / 拐点取值口径**（收盘价 vs 最高最低价）：点评者提出，原书未决（x-p1-19）→ 卡内声明。
5. **"浪3最长"口径冲突**（p-p1-23 图注 vs 延长浪规则）→ needs-review.md 跟踪。
6. **1928.11.28 vs 1928.11 表述差异、原文年份笔误（1937→1938）**：转写/原书层面已标注，随卡引用时使用更正值。

## 结论

16/16 关键任务均有 verified 候选及明确去向；无未解释遗漏。3 条 needs_review 均已登记并跟踪，不影响任务覆盖结论。
