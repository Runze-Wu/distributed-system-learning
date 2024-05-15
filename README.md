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

## 组内相关研究

### ZooKeeper规约验证

* [论文](./papers/2023-SETTA-Spec_Zookeeper.pdf)
* [代码仓库](https://github.com/Disalg-ICS-NJU/zookeeper-tla-spec)
* 规约已被Apache ZooKeeper项目接受，详见[Apache ZooKeeper TLA+规约](https://github.com/apache/zookeeper/tree/master/zookeeper-specifications)

### SandTable分布式系统模型检验

* [论文](./papers/2024-EuroSys-SandTable.pdf)
* [代码仓库](https://github.com/tangruize/SandTable)