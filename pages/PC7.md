-
- ![PC7.pdf](../assets/PC7_1676341151951_0.pdf)
- [[PCAM]]设计过程
	- [[划分]]
	- [[通讯]]
	- [[组合]]
	- [[映射]]
	- ((63eaf010-ad8b-47db-a7f7-d5393d5c5381))
- ## 划分方法描述
  tags:: 划分
	- ((63eaf059-3b0c-4f6a-a0b3-18e32c936b80))
	- 先进行数据分解(称[[域分解]])，再进行计算功
	  能的分解(称[[功能分解]])；
	- 使数据集和计算集互不相交;
	- 划分阶段==忽略处理器数目和目标机器的体
	  系结构==
	- [[域分解]]
	- [[功能分解]]
	- [[划分判据]]
		- 划分是否具有灵活性？
		- 划分是否避免了冗余计算和存储？
		- 划分任务尺寸是否大致相当？
		- 任务数与问题尺寸是否成比例？
		- 功能分解是一种更深层次的分解，是否合理？
- ## 通讯方法描述
	- tags:: 通讯
	- 通讯是[[PCAM]]设计过程的重要阶段
	- [[划分]]产生的诸任务，一般**不能完全独立执行**，需要在任务间进行数据交流；从而产生了通讯
	- [[功能分解]]确定了诸任务之间的数据流
	- 诸任务是并发执行的，通讯则限制了这种并发性
	- [[局部-全局通讯]]
	- [[结构化-非结构化通讯]]
	- [[静态-动态通讯]]
	- [[同步-异步通讯]]
	- [[通讯判据]]
		- 所有任务是否执行==大致相当==的通讯?
		- 是否==尽可能的局部通讯==？
		- 通讯操作是否能==并行执行==?
		- 同步任务的计算能否==并行执行==？
- ## 组合
  tags:: 组合
	- 组合是==由抽象到具体的过程==，是将组合的任务能在一类并行机上有效的执行
	- 合并小尺寸任务，减少任务数。**如果任务数恰好等于处理器数，则也完成了映射过程**
	- 通过增加任务的[[粒度]]和重复计算，可以减少通讯成本
	- 保持映射和扩展的灵活性，降低软件工程成本
	- [[表面-容积效应]]
	- [[重复计算]]
	- [[组合判据]]
		- 增加粒度是否减少了通讯成本？
		- 重复计算是否已权衡了其得益？
		- 是否保持了灵活性和可扩放性？
		- 组合的任务数是否与问题尺寸成比例?
		- 是否保持了类似的计算和通讯？
		- 有没有减少并行执行的机会？
- ## 映射
  tags:: 映射
	- ((63ec92b7-4645-4299-8897-89e6f8828bf5))
	- 每个任务要==映射到具体的处理器==，定位到运行机器上；
	- 任务数大于处理器数时，存在负载平衡和任务调度问题；
	- 映射的目标：减少算法的执行时间
	- **并发**的任务 映射到 **不同的处理器**
	- 任务之间**存在高通讯**的 映射到 **同一处理器**
	- 映射实际是一种权衡，属于==NP完全问题==
	- [[负载平衡算法]]
	- [[任务调度算法]]
	- [[映射判据]]
		- 采用集中式负载平衡方案，是否存在通讯瓶颈？
		- 采用动态负载平衡方案，调度策略的成本如何？
- # 小结
- ((63eca39c-ebb8-4fe4-bcab-625576df4dee))
-
-