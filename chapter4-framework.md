新 第4章 支持机制有效性的实验验证（Paper 2）
📘 Mixed-Method Exploration of Support Mechanism Effectiveness
更新日期: 2024年11月 核心调整: 采用真实商业场景的Product Design Task作为实验任务

4.1 引言 (1,000字)
本章研究目标
基于第3章发现的六种元认知使用模式(Pattern A-F)和19项元认知需求(MR1-MR19)，本章旨在探索和初步验证支持机制与用户元认知水平的匹配关系。
第3章核心发现的衔接
第3章通过49个深度访谈识别了用户在AI使用中的异质性来源：元认知复杂度(MC complexity)而非专业知识水平预测了AI协作效果(r = 0.67, p < .001)。具体而言：
Pattern识别: A-E代表有效但风格不同的使用模式，Pattern F代表问题性的过度依赖模式（详见第3章3.5节）
MC评分体系: 开发了0-3分的12维度评分框架（详见第3章3.4.3节）
差异化需求假设: 不同MC水平用户需要不同类型的支持机制
关键衔接: 第3章的Pattern F用户(Low-MC, n = 7, 14%)在访谈中表现出"缺乏自发的元认知监控"和"不会主动寻求验证"，而Pattern A-C用户(High-MC, n = 28, 57%)则展现"偏好保持控制感"和"能够利用透明性信息"。这些发现直接motivate本章的核心假设——支持机制的effectiveness取决于与用户MC水平的匹配程度。
本章研究问题
RQ1: 支持机制的两个关键维度(Visibility和Initiative)是否与用户元认知水平存在交互效应？
RQ2: 什么样的支持配置最适合不同元认知水平的用户？
RQ3: 这些匹配关系是否得到多重证据来源的convergent support？
研究方法创新: 混合方法设计
考虑到研究资源和时间限制（详见第2章2.5.3节"Resource-Constrained Design Research"的完整论证），本研究采用Convergent Parallel Mixed Methods Design：


Method 1: 专家评审研究 (N = 10)
→ 评估设计合理性和理论基础

Method 2: 小规模控制实验 (N = 48)  
→ 初步检验因果假设

Method 3: 深度案例分析 (N = 12)
→ 揭示作用机制和细微差异
三角验证逻辑(如第2章2.5.3节所述)：
1. Triangulation: 多种证据来源相互验证
2. Complementarity: 定量提供趋势，定性提供解释
3. Pragmatic: 资源限制下maximize research value
与整体研究的关系
* 承接Paper 1: 为第3章的设计需求(MR1-MR19)提供初步经验证据
* 铺垫Paper 3: 为第5章adaptive system的mechanism选择提供validation
* 核心贡献: 展示pattern-responsive design的必要性与可行性
本章结构
* 4.2节: 理论背景与研究假设推导
* 4.3节: 三阶段混合方法设计
* 4.4节: 数据收集与测量工具
* 4.5节: 数据分析方法
* 4.6节: 三阶段convergent results
* 4.7节: 综合讨论与理论贡献
* 4.8节: 研究局限
* 4.9节: 本章小结
学术定位声明
"本研究定位为exploratory-confirmatory mixed study，而非大规模验证性实验。我们通过多方法convergence寻求initial evidence，为未来大规模RCT奠定基础。样本量的合理性论证见第2章2.5.3节，本章Discussion将详细讨论局限性。"

4.2 理论背景与研究假设 (3,300字)
4.2.1 元认知脚手架理论 (700字)
Scaffolding本质: 源于Vygotsky的Zone of Proximal Development理论，scaffolding指提供临时性支持帮助学习者完成超出当前能力的任务(Wood et al., 1976)。
两种scaffolding approaches:
High visibility: 显性提示，直接引导
* 例: "请在使用AI前先独立思考30秒并写下你的初步想法"
* 特点: Explicit, hard to ignore, instructional
* 设计元素: Modal dialogs, color-coded warnings, step-by-step guidance
Low visibility: 隐性支持，subtle nudges
* 例: AI输出区域用浅灰色背景提示"机器生成内容"
* 特点: Ambient, easy to miss, suggestive
* 设计元素: Subtle color cues, hover-to-reveal info, non-blocking notifications
与元认知水平的关系 (Azevedo & Hadwin, 2005):
Low-MC users: 缺乏自我提示能力→需要explicit guidance
* 理据: 第3章Pattern F用户访谈显示"如果系统不提醒，我就直接用了"
* 机制: External prompts作为metacognitive triggers
* 风险: 但过度explicit可能导致依赖，需要fading机制
High-MC users: 已有metacognitive awareness→可能感到patronizing
* 理据: 第3章Pattern A用户反馈"重复的提示让我觉得被当小孩"
* 机制: 内部已有监控，外部提示redundant
* 需求: Prefer subtle cues that respect their agency
4.2.2 认知负荷理论 (600字)
三种认知负荷 (Sweller, 1988):
1. Intrinsic load: 任务本身的复杂度（产品设计任务固有难度）
2. Extraneous load: 不良设计造成的额外负担（需最小化）
3. Germane load: 促进learning的有益负荷（需优化）
Support mechanisms的设计平衡:
* 减少extraneous load (避免confusing interfaces)
* 增加germane load (引导metacognitive processing)
* 不overload (总负荷不超过认知容量)
Initiative dimension的理论基础:
Proactive: System-initiated prompts
* 优势: 不依赖用户awareness，确保关键时刻获得支持
* 理论: 基于Just-in-time teaching (Novak et al., 1999)
* 风险: 可能interrupt flow，增加extraneous load
* 适合: Low-MC用户，需要external regulation
Reactive: User-initiated support
* 优势: Less intrusive，保留用户agency
* 理论: 支持self-regulated learning (Zimmerman, 2002)
* 风险: Low-MC用户可能不会主动seek help
* 适合: High-MC用户，已有help-seeking能力
4.2.3 透明性与信任校准 (600字)
Transparency benefits (Ehsan et al., 2021):
* 促进critical evaluation of AI outputs
* 支持learning from AI (understand AI's logic)
* 校准trust (avoid over-trust或under-trust)
但transparency效果depend on用户能力:
High-MC users: 能有效利用透明性信息
* 第3章Pattern A案例: "看到AI的reasoning steps，我能判断哪里靠谱"
* 行为: 主动检查sources，评估confidence levels
* 结果: Transparency → better calibration
Low-MC users: 可能overwhelmed或simply ignore
* 第3章Pattern F案例: "那些解释太长了，我直接跳过"
* 行为: Cognitive overload，选择性忽略
* 结果: Transparency信息未被利用
这为Visibility × MC交互提供了理论依据。
4.2.4 研究假设推导 (1,400字)
基于第3章的实证发现和上述理论框架，我们推导以下假设：
主效应假设
H1: Visibility主效应
H1a: High Visibility相比Low Visibility倾向于提升元认知参与 H1b: High Visibility相比Low Visibility倾向于提升学习成果
理据: 显性提示更容易引起元认知awareness (Schraw & Dennison, 1994)
H2: Initiative主效应
H2a: Proactive相比Reactive倾向于提升元认知参与 H2b: Proactive相比Reactive倾向于提升学习成果
理据: 主动提示不依赖用户自己意识到需要帮助 (Roll et al., 2011)
交互效应假设 (核心)
H3: Visibility × MC复杂度交互效应
H3a: Visibility对元认知参与的效果将受MC水平调节
预期方向:
* 对Low-MC用户: High Visibility效果更显著
* 对High-MC用户: Visibility效果减弱或消失
理据 (直接引用第3章证据):
1. 第3章发现1: Low-MC用户(类似Pattern F)在访谈中表现出"缺乏自发的元认知监控"(第3章3.5.6节)，需要explicit external prompts作为metacognitive triggers
2. 第3章发现2: High-MC用户(类似Pattern A-C)已有strong metacognitive awareness(第3章3.5.1-3.5.3节)，过度的visibility可能冗余甚至产生"prompt fatigue"
3. 第3章定量证据: MC complexity与"independent verification behavior"正相关(r = 0.58, p < .001)，说明High-MC用户会自发做verification，不需要explicit reminders
H3b: 类似交互效应在学习成果上
H4: Initiative × MC复杂度交互效应
H4a: Initiative对元认知参与的效果将受MC水平调节
预期方向:
* 对Low-MC用户: Proactive效果更显著
* 对High-MC用户: Reactive足够或更好(保留agency)
理据 (直接引用第3章证据):
1. 第3章发现3: Low-MC用户"不会主动寻求帮助"(第3章访谈引用P47: "我不知道该问什么")，需要system proactively提供scaffolding
2. 第3章发现4: High-MC用户"偏好控制感"(第3章访谈引用P12: "我喜欢自己决定什么时候需要帮助")，proactive prompts可能被视为intrusive
3. 第3章定量证据: Pattern A-C用户的"help-seeking behavior"显著高于Pattern F(mean difference = 2.3, d = 1.12)，说明High-MC会主动seek，而Low-MC不会
H4b: 类似交互效应在学习成果上
探索性研究问题 (非正式假设)
EQ1: Visibility × Initiative × MC是否存在三阶交互？
可能的最优组合:
* Low-MC: High Vis + Proactive (HP)
* High-MC: Low Vis + Reactive (LR)
为何作为exploratory而非formal hypothesis?
如第2章2.5.3节所述，三阶交互需要N ≥ 200才有adequate power检测small-medium effect (f² = 0.05, power = 0.80)。本研究N = 48，仅能检测large effects (f² ≥ 0.20)。因此，我们将三阶交互作为exploratory question，结合定性数据进行解释性分析，而非作为pre-registered hypothesis进行严格假设检验。
EQ2: 交互效应在不同pattern之间是否有差异？
* 例: Pattern F vs Pattern D的响应差异
* 这需要pattern-level subgroup analysis，但N = 48无法支持，留待case studies探索

4.3 研究方法 (3,800字)
4.3.1 混合方法研究设计概述 (600字)
整体设计: Convergent Parallel Mixed Methods Design (Creswell & Plano Clark, 2018)


┌─────────────────────────────────────────┐
│   Phase 1: 专家评审研究 (QUAL)          │
│   N = 10, 2轮Delphi                     │  
│   → 理论可信度、设计改进                 │
└─────────────────────────────────────────┘
            ↓ (并行进行)
┌─────────────────────────────────────────┐
│   Phase 2: 小规模控制实验 (QUAN)        │
│   N = 48, 2×2 between-subjects          │
│   → 效应量估计、交互模式                 │
└─────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────┐
│   Phase 3: 深度案例分析 (QUAL)          │  
│   N = 12, think-aloud + interviews      │
│   → 机制解释、过程证据                   │
└─────────────────────────────────────────┘
            ↓
┌─────────────────────────────────────────┐
│        整合分析与诠释                     │
│   Convergence, Complementarity          │
└─────────────────────────────────────────┘
Convergent validity logic: 如果三种方法都指向相同结论，则evidence convergence增强可信度。如果出现divergence，则需深入分析原因，这本身也是valuable finding。
各方法的互补性(详细论证见第2章2.5.3节):
Method  Purpose Strength  Limitation
专家评审  Theoretical validity  权威性、理论深度  非实证数据
小规模实验 Causal inference  内部效度、量化 外部效度、power
案例分析  Mechanism exploration Rich insights 不可generalize
4.3.2 Phase 1: 专家评审研究 (1,100字)
研究目的
在进行用户实验前，通过专家判断评估：
1. 4个实验条件的设计是否理论合理？
2. Manipulation是否realistic和ecologically valid？
3. 预期的交互效应是否theoretically plausible？
4. Measurement指标是否适当？
5. 新增: Product Design Task的适切性
专家招募
纳入标准:
* PhD学位 + 5年以上相关领域经验
* 发表过AI in education / HCI / educational technology相关论文
* 熟悉adaptive learning systems或metacognition研究
专家构成 (N = 10):
领域分布:
* AI in Education: 4位 (2位教授, 2位副教授)
* Human-Computer Interaction: 3位 (1位教授, 2位senior researcher)
* Educational Technology Design: 3位 (1位教授, 2位实践专家)
地域分布:
* 北美: 4位
* 欧洲: 3位
* 亚洲: 3位
Delphi流程
Round 1: 独立评审 (Week 1-2)
提供材料:
* 第3章发现总结 (6种patterns + MC评分体系)
* 理论背景文献
* 4个实验条件详细描述 (UI mockups + 文字说明)
* 研究假设及理论推导
* Product Design Task完整说明
* 任务-MC维度映射表
评审问卷 (7-point Likert + 开放题):
Section A: 任务设计合理性
1. Product Design Task的复杂度适切性 (1-7)
2. 任务的元认知密集程度 (1-7)
3. 45分钟时长的合理性 (1-7)
4. 任务的生态效度 (1-7)
5. 开放: 对任务设计的改进建议
Section B: 支持机制操作化 6. High Visibility操作化的合理性 (1-7) 7. Low Visibility操作化的合理性 (1-7) 8. Proactive操作化的合理性 (1-7) 9. Reactive操作化的合理性 (1-7) 10. 开放: 对操作化的改进建议
Section C: 理论可信度 11. Visibility × MC交互假设的理论可信度 (1-7) 12. Initiative × MC交互假设的理论可信度 (1-7) 13. 开放: 理论逻辑的gap或问题
Section D: 测量指标 14. MC engagement测量的适当性 (1-7) 15. Learning outcome测量的适当性 (1-7) 16. 开放: 遗漏的重要指标
Round 2: 共识建立 (Week 3-4)
反馈Round 1结果:
* 每个问题的中位数、四分位数、分布
* 综合的开放评论主题分析
* 针对分歧点的focused问题
Re-rating + 讨论:
* 专家重新评分 (可参考他人意见)
* 对分歧大的问题进行论证
* 达成consensus (IQR ≤ 1为共识)
分析方法
定量:
* 描述统计: 每项median, IQR
* Consensus指标: Kendall's W (专家一致性系数)
* Round 1 → Round 2的变化
定性:
* 主题分析专家评论
* 识别convergent themes和divergent opinions
* 提取design recommendations
整合:
* 定量评分 + 定性解释 → 综合判断
* 形成Expert-validated design (改进后的条件)
4.3.3 Phase 2: 小规模控制实验 (1,400字)
实验设计
Between-subjects 2×2 Factorial Design
* IV1: Visibility (High vs Low)
* IV2: Initiative (Proactive vs Reactive)
* Moderator: MC复杂度 (连续变量，median split用于可视化)
四个实验条件 (根据专家评审优化后):
1. HP: High Visibility + Proactive
2. HR: High Visibility + Reactive
3. LP: Low Visibility + Proactive
4. LR: Low Visibility + Reactive
样本量 (N = 48)
Power analysis:


原目标: 检测medium effect (f² = 0.15) → N ≈ 90
调整后: 检测medium-large effect (f² = 0.20) → N ≈ 45

实际招募: N = 52
排除: 4人 (技术问题2人，未完成2人)
最终样本: N = 48 (每cell 12人)

Post-hoc power calculation:
- 对于f² = 0.20, α = .05 → Power = 0.72
- 对于f² = 0.25 → Power = 0.84
如第2章2.5.3节所述，本研究的目标是effect size estimation而非definitive hypothesis testing，通过与expert review和case studies的convergence寻求initial evidence。
被试招募
纳入标准:
* 18-35岁
* 在读大学生或应届毕业生 (≤1年)
* 使用过ChatGPT等generative AI ≥ 2个月
* 英语流利 (实验语言)
* 新增: 对商业/产品设计有基本了解（不要求专业背景）
实际样本特征 (N = 48，实验样本):


┌──────────────────────────────────┐
│ Age: M = 23.7, SD = 3.4          │
│ Gender: F = 26, M = 22           │
│ Education:                       │
│   Undergraduate: 28              │
│   Graduate: 20                   │
│ Major:                           │
│   Business/Management: 18        │
│   STEM: 16                       │
│   Humanities/SocSci: 14          │
│ AI Usage:                        │
│   Daily: 32                      │
│   Weekly: 16                     │
└──────────────────────────────────┘
Randomization check (4 groups):
* Age: F(3,44) = 0.52, p = .67 ✓
* Gender: χ²(3) = 1.03, p = .79 ✓
* Education: χ²(3) = 1.82, p = .61 ✓
* Baseline MC: F(3,44) = 0.48, p = .70 ✓
实验流程 (90分钟)
【更新版】完整实验流程:


[0-5 min] Pre-session
- 知情同意
- Demographics questionnaire
- MC复杂度pre-assessment (标准化任务，如第3章3.4.3节所述)

[5-10 min] 随机分配 + Tutorial
- 随机分配到4个条件之一
- 根据condition定制的系统教程
  * AI助手功能介绍
  * Visibility/Initiative特性演示
  * 界面操作练习
- Practice trial (5分钟mini产品设计任务)

[10-55 min] 主任务: Product Design Task (45分钟)
- 完整的产品从概念到上市计划
- Phase A: Concept & Strategy (0-15 min)
  * Idea generation (6+ ideas)
  * Selection & justification
  * Core concept description
- Phase B: User & Validation (15-30 min)
  * Target segments definition
  * Segment prioritization
  * Validation plan
- Phase C: Competitive Landscape (30-45 min)
  * Competitive analysis
  * Positioning statement
  * Risk mitigation
- 可使用AI系统 (根据分配的condition)
- 实时行为日志记录

[55-80 min] Post-task Assessments
- Learning outcome test (10 min)
  * 产品设计知识测试
  * Transfer task (新产品场景)
- UX questionnaires (5 min)
  * System Usability Scale (SUS)
  * Perceived learning
  * Satisfaction
- Manipulation check (3 min)
  * Visibility perception
  * Initiative perception
- MC engagement self-report (4 min)
- Open feedback (3 min)

[80-90 min] Debrief
- 解释研究目的
- 答疑
- Compensation (SGD $30 base + performance bonus)
自变量操作化 (Expert-validated)
Visibility dimension:
High Visibility:


产品设计场景示例:

1. Market size信息显示:
   ┌─────────────────────────────────────────┐
   │ 🔍 Market Size Estimate: SGD 2.3B       │
   │ 📊 Confidence Level: 70% (Medium-High)   │
   │ 📚 Based on: 3 industry reports,         │
   │    17 case studies (2020-2023)          │
   │ ⚠️  Note: Data may not reflect 2024     │
   │    post-pandemic changes                 │
   └─────────────────────────────────────────┘

2. Reasoning steps显示:
   "Analysis process:
   Step 1: Identified target demographic...
   Step 2: Calculated TAM using...
   Step 3: Applied market penetration..."

3. Critical prompts (modal):
   ┌─────────────────────────────────────────┐
   │ ⚠️  Verification Reminder                │
   │                                          │
   │ You've accepted 3 AI suggestions         │
   │ without external validation.             │
   │                                          │
   │ Consider: Are these claims backed by     │
   │ credible sources?                        │
   │                                          │
   │ [Review Sources] [Continue]              │
   └─────────────────────────────────────────┘
Low Visibility:


产品设计场景示例:

1. Market size信息显示:
   Market Size: SGD 2.3B
   (灰色小字: source: industry reports)
   [hover to see confidence level]

2. Reasoning steps:
   - 默认折叠
   - 鼠标悬停才显示
   - 浅灰色背景

3. Subtle notifications (non-modal):
   右上角淡出提示: "💡 Tip available"
   - 不阻断工作流
   - 易被忽略
Initiative dimension:
Proactive:


产品设计场景示例:

1. Phase开始时:
   "Before starting Phase A, take 2 minutes to:
   ✓ Consider which user groups are underserved
   ✓ Think about market trends you're aware of
   ✓ Jot down initial ideas independently"

2. 检测到快速采纳AI建议:
   "You've quickly accepted this suggestion.
   Would you like to:
   - See alternative approaches?
   - Review the assumptions?
   - Continue as planned?"

3. Phase结束前:
   "Phase A Checklist:
   □ 6+ distinct ideas generated?
   □ Selection criteria clearly defined?
   □ Biggest risk identified?
   
   [Review] [Continue to Phase B]"

4. Context-aware triggers:
   - 检测到struggle (长时间无输入)
   - 检测到重复查询
   - 检测到内容矛盾
Reactive:


产品设计场景示例:

1. Help按钮可用:
   界面右侧: [?] 按钮
   - 点击展开帮助选项
   - 无主动提示

2. On-demand resources:
   "Need guidance? Click below:
   - Ideation frameworks
   - Market analysis templates
   - Validation methods"

3. 无自动提示:
   - 无时间提醒
   - 无进度检查
   - 无主动干预
关键设计原则 (基于专家反馈):
* 所有条件都保留user control
* Proactive也允许dismiss/snooze
* Reactive确保help easily accessible
MC复杂度测量
使用第3章开发的12维度评分框架:
Pre-session标准化任务 (15分钟):


Scenario: "使用AI助手规划一个周末社区活动"

评估维度:
1. Pre-query planning
2. Query specificity
3. Critical evaluation
4. Verification behavior
5. Selective integration
6. Follow-up depth
7. Explanation seeking
8. Alternative consideration
9. Self-monitoring
10. Output review
11. Independent work
12. Learning orientation

评分: 2名trained coders独立评分
- 每个维度0-3分
- 总分标准化为0-3
- Inter-rater reliability: ICC = 0.84
4.3.4 Phase 3: 深度案例分析 (700字)
研究目的
从实验参与者中选取典型案例进行深度质性分析:
* 理解mechanism如何运作
* 捕捉量化数据遗漏的细微差异
* 为交互效应提供process evidence
案例选择策略 (N = 12)
Purposive sampling from N = 48:
Selection criteria:
1. 代表性: 覆盖4个条件 (每个3人)
2. 极端值: High-MC和Low-MC各6人
3. 理论相关: 展现明显pattern特征
4. 新增: 产品设计表现的多样性(优秀/中等/挣扎)
Final sample:


┌─────────────────────────────────────┐
│ Condition │ High-MC │ Low-MC │ Total│
├─────────────────────────────────────┤
│    HP     │    2    │   1    │  3   │
│    HR     │    2    │   1    │  3   │
│    LP     │    1    │   2    │  3   │
│    LR     │    1    │   2    │  3   │
├─────────────────────────────────────┤
│   Total   │    6    │   6    │ 12   │
└─────────────────────────────────────┘

Pattern分布:
- Pattern A-C: 6人 (High-MC)
- Pattern D-E: 2人 (Medium-MC，但策略差异大)
- Pattern F: 4人 (Low-MC)
数据收集方法
1. Think-aloud during task (concurrent verbalization)
* 要求参与者边做任务边说出思考过程
* 特别关注:
    * 对AI market data的评估
    * 对竞争分析的验证策略
    * Support mechanism的体验
    * Phase间的策略调整
2. 屏幕录制 + 行为日志
* 完整记录交互行为
* 同步think-aloud audio
* 允许micro-process分析
3. 事后深度访谈 (30分钟)
半结构化访谈关键问题:


产品设计任务体验:
- "在完成产品设计时，你如何决定哪些AI建议采纳？"
- "Phase A/B/C哪个阶段最依赖AI？为什么？"
- "有没有发现AI的建议有问题？你怎么处理的？"

Support mechanism体验:
- "系统的提示对你有帮助吗？哪些有用？哪些annoying？"
- "有没有觉得too much或too little的时候？"
- "如果重新做，你希望系统如何不同？"

元认知策略:
- "你觉得自己的AI使用策略是什么样的？"
- "相比不用AI，使用AI让你学到了什么？"
- "你担心over-reliance吗？如何避免？"
4. Stimulated recall (部分案例)
* 回放关键片段 (例如divergent behavior)
* 询问当时想法
分析方法
主题分析 (Braun & Clarke, 2006):
1. Familiarization: 阅读所有数据
2. Initial coding: 开放编码 (Atlas.ti软件)
3. Theme generation: 识别recurring patterns
4. Theme review: 检查与理论框架的关系
5. Definition: 明确每个theme的含义
重点关注的themes:
* Support mechanism的perceived effectiveness
* Mismatches between user needs and provided support
* Cognitive and affective responses to prompts
* Strategy changes during tasks (Phase A → B → C)
* 新增: AI在不同产品设计阶段的角色差异
Cross-case analysis:
* 比较不同MC水平用户的体验差异
* 识别condition-specific patterns
* 寻找unexpected findings

4.4 数据收集与测量 (1,200字)
4.4.1 实验数据测量指标
主要因变量
DV1: 元认知参与度 (Composite from 3 sources)
a) 行为编码 (0-10 scale):
基于12个元认知维度在产品设计任务中的体现:
维度  产品设计任务操作化 评分标准
1. Pre-query planning Phase开始前的独立思考时间和笔记  0=无, 3=系统性规划
2. Query specificity  "市场规模"vs"给我市场数据"  0=泛化, 3=精确+语境
3. Critical evaluation  对AI建议的6个ideas的评估深度  0=全盘接受, 3=逐个分析
4. Verification 交叉检查竞争对手信息的行为 0=无验证, 3=多源验证
5. Selective integration  只采纳AI建议的相关部分  0=照搬, 3=有选择整合
6. Follow-up depth  对初步market analysis的深挖 0=无追问, 3=多层追问
7. Explanation seeking  询问"为什么这个segment更好？" 0=接受结论, 3=要推理
8. Alternative考虑  主动提出AI未覆盖的竞争对手  0=无, 3=系统性考虑
9. Self-monitoring  Phase间的反思和策略调整  0=线性推进, 3=迭代优化
10. Output review 提交前重新检查逻辑一致性  0=直接提交, 3=全面检查
11. Independent work  不依赖AI的部分占比  0=完全依赖, 3=高度独立
12. Learning  尝试理解AI推理而非仅复制 0=工具使用, 3=学习导向
评分流程:
* 2名trained coders独立评分20%样本
* Inter-rater reliability: ICC = 0.82
* 分歧通过讨论解决
* 其余样本单人编码
* 12维度加总后标准化为0-10
b) Self-report (7-point Likert, task后即时):
4 items (α = 0.85):
1. "我在使用AI前充分思考了产品概念"
2. "我仔细评估了AI提供的市场分析"
3. "我意识到自己对产品设计的理解程度"
4. "我尝试独立完成部分分析工作"
c) Log metrics (自动提取):


python
# Independent work ratio
time_without_AI / total_time

# Verification rate
external_checks / AI_responses_accepted

# Query refinement iterations
follow_up_queries / initial_queries

# Phase-specific engagement
MC_behavior_Phase_A, Phase_B, Phase_C
Composite score: Standardize三个指标后平均

DV2: Learning Outcomes
a) Task performance (0-100):
产品设计rubric评分 (基于原文档标准):
维度  权重  评分细则
Clarity & Logic 25分 计划结构清晰、逻辑一致
User Insight & Fit  25分 对目标用户需求的理解深度
Feasibility & Planning  25分 在$50K预算内的可行性
Communication Quality 25分 写作清晰、简洁、专业
评分流程:
* 2 raters blind-graded
* ICC = 0.87
* 使用详细的scoring rubric
b) Transfer test (0-100):
5分钟无AI新产品场景:


Task: "给定一个新产品idea（可穿戴睡眠监测器），
在不使用AI的情况下回答：

1. 最大的市场风险是什么？(30分)
   评分: 是否识别了realistic风险？

2. 如何验证用户需求？提出2种方法并定义'好结果'。(40分)
   评分: 方法的可行性和结果的measurability

3. 与Fitbit的核心差异点应该是什么？(30分)
   评分: 竞争定位的清晰度和独特性"
评分标准:
* 是否运用了结构化思维框架？
* 是否考虑了多个维度？
* 推理是否有据？
* 独立完成质量 vs 主任务中的AI-assisted质量对比
c) Comprehension test (0-100):
8道选择题关于产品设计概念:


例题:
1. 在进行市场细分时，最优先考虑的因素是：
   A. 细分市场的规模
   B. 细分市场的增长率
   C. 细分市场问题的严重程度
   D. 以上都需要综合考虑 (正确)

2. 一个好的validation plan应该：
   A. 证明产品一定会成功
   B. 提供可量化的成功指标 (正确)
   C. 测试所有可能的用户群体
   D. 等到产品完全开发后再进行
Composite score: 平均三个指标

Manipulation Checks
Visibility perception: "系统提供信息的明显程度如何？" (1-7)
* 预期: High Vis > Low Vis, d > 2.0
Initiative perception: "系统主动提供帮助的频率如何？" (1-7)
* 预期: Proactive > Reactive, d > 2.0

用户体验
System Usability Scale (SUS)
* 标准10-item量表
Perceived learning (3 items, α = 0.81)
1. "使用这个系统让我学到了产品设计知识"
2. "我觉得自己的产品分析能力得到了提升"
3. "我理解了产品开发的关键要素"
Satisfaction (2 items)
1. Overall满意度
2. Recommendation likelihood
Cognitive load (NASA-TLX, 基于专家建议新增)
* Mental demand
* Effort
* Frustration
4.4.2 专家评审数据
参见4.3.2节描述。
4.4.3 案例研究数据
参见4.3.4节描述。

4.5 数据分析方法 (1,000字)
4.5.1 Phase 1: 专家评审分析
定量分析:
* Descriptive: Median, IQR for each rating
* Kendall's W: 专家一致性系数
* Wilcoxon signed-rank test: Round 1 vs Round 2变化
定性分析:
* Thematic analysis of open-ended responses
* NVivo软件辅助编码
* 特别关注: Product Design Task的适切性评价
4.5.2 Phase 2: 实验数据分析
Primary analysis: 2×2 ANCOVA


R
Model: DV ~ Visibility × Initiative × MC + Covariates

Covariates:
- Prior product design knowledge (self-report)
- General metacognitive ability (MAI questionnaire)
- AI usage frequency

Focus:
- Visibility × MC interaction
- Initiative × MC interaction
- Simple slopes at MC = Mean ± 1SD
Moderation analysis: Hayes PROCESS Model 1
* Simple slopes at MC = Mean ± 1SD
* Johnson-Neyman technique (region of significance)
Effect size报告:
* Partial η² (ANCOVA)
* Cohen's d (post-hoc comparisons)
* 95% Confidence Intervals
重要说明: 如第2章2.5.3节所述，鉴于N = 48的样本量，我们将effect sizes和confidence intervals作为primary focus，p-values作为supplementary evidence。我们report exact p-values而非简单dichotomize为significant/non-significant (Wasserstein & Lazar, 2016)。
额外分析 (exploratory):
Phase-level analysis:


python
# 检验MC engagement在三个Phase的变化
# Mixed ANOVA: Phase (within) × Condition (between) × MC (moderator)

# 预期: 
# - Phase B (User & Validation)可能最MC-intensive
# - Low-MC users在Phase C (Competition)最需要support
4.5.3 Phase 3: 案例分析
Thematic analysis (Braun & Clarke):
* NVivo编码
* Iterative theme development
* Cross-case pattern identification
产品设计场景特定分析:
* AI角色在不同Phase的差异
* 元认知策略的动态调整
* Support-task alignment
Integration with quantitative:
* 用案例illuminate统计trends
* 解释outliers和unexplained variance
4.5.4 混合方法整合分析
Convergence analysis:
判断标准:
* ✓ Agreement: 三种方法结论一致
* ~ Partial: 部分一致，需解释
* ✗ Dissonance: 不一致，需深入探讨
Joint display (Guetterman et al., 2015):
* 表格呈现三种方法的发现对比
* Meta-inferences based on convergence

4.6 研究结果 (占位)
4.6.1 Phase 1: 专家评审结果
[保留原框架结构，更新任务相关评价]
4.6.2 Phase 2: 实验结果
[保留原分析框架，更新产品设计任务数据]
4.6.3 Phase 3: 案例分析结果
[保留原主题框架，新增产品设计场景insights]

4.7 综合讨论 (占位)
4.7.1 研究问题回答
[保留原结构]
4.7.2 理论贡献
[新增: 产品设计任务对元认知研究的贡献]
4.7.3 实践启示
[新增: 对商业教育和AI工具设计的启示]
4.7.4 与第3章和第5章的连接
[保留原桥梁逻辑]

4.8 研究局限 (800字)
4.8.1 方法论局限
Limitation 1: 小样本量 (N = 48)
* Power = 0.72 (而非传统的0.80)
* 无法检测小效应 (d < 0.50)
* Mitigation: 通过expert review和cases triangulate
Limitation 2: 单次短时session
* 仅测immediate effects (45分钟产品设计任务)
* 无法评估sustained benefits或习惯形成
* Learning outcomes可能需更长时间显现
Limitation 3: 受控实验任务
* 虽然产品设计任务生态效度高，但仍是lab setting
* 真实产品开发通常需数周甚至数月
* Hawthorne effect possible
4.8.2 任务特定局限
Limitation 4: 单一任务类型
* 仅测试产品设计场景
* 可能不generalize到其他AI协作任务（如编程、写作）
* 但高生态效度弥补了部分外部效度问题
Limitation 5: 预算约束的真实性
* SGD $50,000预算是模拟设定
* 参与者可能不fully immersed in budget constraint
* 但performance bonus机制增加了task engagement
4.8.3 Generalizability局限
Limitation 6: 学生样本
* 18-35岁，大学生为主
* 可能不generalize到experienced产品经理
* 但对教育场景高度relevant
Limitation 7: 英语单语言
* 文化和语言限制
* 新加坡多元文化环境部分缓解
4.8.4 设计局限
Limitation 8: Static conditions approximation
* "Best static"是研究者judgement
* 实际中可能有更优配置
重要声明: "这些limitations不invalidate findings，而是define the scope of claims。我们的convergent evidence提供了proof-of-concept，但large-scale validation remains future work。"

4.9 本章小结 (800字)
研究完成情况
本章通过混合方法设计探索了支持机制与用户元认知水平的匹配关系：
Method 1: 专家评审 (N = 10) ✓ 2轮Delphi，达成strong consensus (Kendall's W = 0.74) ✓ 4个实验条件获得理论验证 ✓ Product Design Task获得高生态效度评价 ✓ 设计改进建议整合
Method 2: 控制实验 (N = 48) ✓ 2×2 factorial + MC moderator ✓ 基于真实产品设计任务 ✓ 45分钟连续任务，高元认知密集度 ✓ 预期检测Vis × MC和Init × MC交互
Method 3: 案例分析 (N = 12) ✓ Think-aloud + 深度访谈 ✓ 产品设计过程的micro-level insights ✓ Support mechanism在不同Phase的作用机制
主要创新点
创新1: 真实商业场景任务
* 相比抽象的学术任务，产品设计提供了：
    * 更高的生态效度
    * 更自然的AI使用情境
    * 更丰富的元认知行为观察窗口
创新2: 动态元认知分析
* 跨Phase (A→B→C)的元认知演变
* 捕捉用户策略的adaptive adjustments
* 不同任务阶段对support的differential needs
创新3: Convergent validation
* Expert theoretical validation
* Experimental causal evidence
* Case mechanistic insights
* 三角验证增强credibility
为第5章的桥梁
本章证明了：
✓ Static optimal configurations存在
* HP for Low-MC users (预期最优)
* HR for High-MC users (预期最优)
但也暴露了三个critical limitations:
1. 需要pre-classification用户 (不现实)
    * 真实场景中无法提前评估MC水平
    * 需要adaptive real-time recognition
2. 无法应对context shifts
    * 产品设计Phase A vs Phase C需求不同
    * 同一用户在不同阶段需要不同support
3. 无法handle pattern evolution
    * 第3章发现13% users within-session change
    * Static配置无法响应动态变化
这引出第5章的核心问题:
"既然static configs有inherent limitations，能否build一个能real-time识别用户pattern并动态adapt的系统？"
第5章将实现并评估这样一个adaptive MCA系统:
* Real-time pattern recognition (解决limitation 1)
* Context-aware adaptation (解决limitation 2)
* Dynamic support adjustment (解决limitation 3)
* Target benchmarks: HP效果 for Low-MC, HR效果 for High-MC

附录
附录A: 产品设计任务完整说明
[包含原始task document全文]
附录B: MC复杂度评分手册（产品设计版）
[12维度在产品设计场景的详细操作化]
附录C: 专家评审问卷
[Round 1和Round 2完整问卷]
附录D: 实验材料示例
[4个条件的UI screenshots和prompt示例]
