- ((63e1be2b-71da-4234-b080-51a634e5794b))
- 高性能计算集群采用==将计算任务分配到集群的不同计算节点==而提高计算能力，因而主要应用在科学计算领域。
- HPC集群特别适合于在计算中各计算节点之间发生**大量数据通讯**的计算作业，比如一个节点的中间结果或影响到其它节点计算结果的情况。
- [[Beowulf集群]]
	- 比较流行的HPC采用Linux操作系统和其它一些免费软件来完成并行运算。这一集群配置通常被称为 Beowulf集群。这类集群通常运行特定的程序以发挥 HPC cluster的并行能力。这类程序一般应用特定的运行库, 比如专为科学计算设计的MPI库。