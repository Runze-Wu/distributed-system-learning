# 分布式系统学习入门

本仓库收集了分布式系统学习的相关资料，

## 开源课程

### MIT 6.5840

* [课程主页](https://pdos.csail.mit.edu/6.824/index.html)

该课程是MIT的分布式系统课程，原名为6.824，课程内容通过阅读分布式系统领域经典论文来学习分布式系统的基本原理和关键技术。

#### 课程实验

其开源课程实验，通过若干次Lab以难度递增的方式来逐步实现一个基于Raft共识算法的分布式KV存储系统。

* [Raft论文](./papers/2014-ATC-Raft.pdf)
* [Lab1](https://pdos.csail.mit.edu/6.824/labs/lab-mr.html)：实现简易的MapReduce系统，
* [Lab2](https://pdos.csail.mit.edu/6.824/labs/lab-kvsrv.html)：实现简易的单机KV存储系统，仅支持单机存储。
* [Lab3](https://pdos.csail.mit.edu/6.824/labs/lab-raft.html)：实现Raft共识算法。
* [Lab4](https://pdos.csail.mit.edu/6.824/labs/lab-shard.html)：基于Raft共识算法实现分布式KV存储系统，实现服务端和客户端。
* [Lab5](https://pdos.csail.mit.edu/6.824/labs/lab-shard.html)：为分布式KV存储系统添加分片功能。

### PingCap Distributed Transaction

* [课程主页](https://learn.pingcap.cn/learner/course/750001)

该课程是PingCap公司开设的分布式事务课程，学习分布式事务的基本原理。

#### 课程实验

PingCap基于[TinySQL](https://github.com/talent-plan/tinysql)和[TinyKV](https://github.com/talent-plan/tinykv)搭建了一个简易的分布式事务系统框架，学员需要通过实验逐步实现一个基于Percolator分布式事务算法的分布式事务系统。其中TinySQL和TinyKV是PingCap开源分布式数据库[TiDB](https://github.com/pingcap/tidb)和[TiKV](https://github.com/tikv/tikv)的简化版本。

* [Percolator](./papers/2010-OSDI-Percolator.pdf)
* [Lab1](https://github.com/tiny-talent/distributed-txn/blob/master/tinykv/doc/lab1.md)：在TinyKV中实现事务相关接口。
* [Lab2](https://github.com/tiny-talent/distributed-txn/blob/master/tinysql/doc/lab2-README-zh_CN.md)：在TinySQL中实现Percolator。

## 开源项目

### MiniOB

* [项目主页](https://oceanbase.github.io/miniob/)

MiniOB是OceanBase团队开源的具有基础功能的小型关系型数据库，其中不考虑并发操作和复杂的事务管理，用于迅速了解数据库并深入学习数据库内核。

#### 数据库比赛

* [赛事主页](https://open.oceanbase.com/train)

OceanBase数据库比赛设计了一系列题目，通过实现这些题目能够对数据库内核各个模块（网络、磁盘IO、索引、SQL解析、SQL执行等）有更深入的了解。

## 组内相关研究

### 形式化规约语言 TLA+

* [TLA+主页](https://lamport.azurewebsites.net/tla/tla.html)

TLA+(Temporal Logic of Actions)是一种形式化规约语言，用于描述分布式系统的行为。TLA+由Leslie Lamport提出，通过TLA+可以描述系统的状态和状态转移，以及对系统的性质进行验证。

相关工具链：

* [TLC](https://lamport.azurewebsites.net/tla/tools.html)：TLA+配套的模型检验工具，用于验证TLA+规约的性质。
* [TLAPS](https://lamport.azurewebsites.net/tla/tlaps.html)：TLA+配套的定理证明工具。

### ZooKeeper规约验证

该工作针对分布式协同服务系统ZooKeeper和其背后的分布式共识协议Zab，使用TLA+对其核心协议和系统实现分别进行了形式化验证。

* [论文](./papers/2023-SETTA-Spec_Zookeeper.pdf)
* [代码仓库](https://github.com/Disalg-ICS-NJU/zookeeper-tla-spec)
* [研究相关的中文论文](./papers/黄彬寓-硕士毕业论文-06-12.pdf)
* 规约已被Apache ZooKeeper项目接受，详见[Apache ZooKeeper TLA+规约](https://github.com/apache/zookeeper/tree/master/zookeeper-specifications)

### SandTable分布式系统模型检验

基于系统实现的模型检验工具（DMCK）在验证分布式系统正确性方面十分有效，但DMCK又面临着严重的状态空间爆炸问题。该工作提出SandTable技术，将状态空间遍历从代码实现级提升到规范级，有效减少状态空间爆炸问题，并成功发现了多个真实分布式系统的深层漏洞。

* [论文](./papers/2024-EuroSys-SandTable.pdf)
* [代码仓库](https://github.com/tangruize/SandTable)