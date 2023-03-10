- ((63e3abe1-b488-40f2-95d2-ff3b5f747b2d))
- 基本概念
	- 由Valiant(1990)提出的，“块”同步模型，是一种异步[[MIMD‐DM]]模型，支持消息传递系统，块内异步并行，==块间显式同步==。
	-
- 模型参数
	- p：处理器数（**带有存储器**）
	- l：同步障时间（Barrier synchronization time）
	- g：带宽因子（time steps/packet)=$1/bandwidth$
- ## 计算过程
- 由若干==超级步==组成，每个超级步计算模式为：
	- ((63e3ac80-bc56-452d-acd8-dca6302a7d6c))
- 优缺点：
	- 强调了计算和通讯的分离，提供了一个编程环境，易于程序复杂性分析。但需要显式同步机制，限制至多h条消息的传递等。
- 与 [[APRAM模型]]区别：超级步时间是确定的，每隔一定时间就检查该阶段的任务是否完成，若完成则进行下一步，若未完成则下一超级步仍分配给这个任务。而[[APRAM模型]]则是以任务为分配单位，每当一个任务做完，再进行同步。