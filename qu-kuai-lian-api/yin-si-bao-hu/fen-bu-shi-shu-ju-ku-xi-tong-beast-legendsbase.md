# 分布式数据库系统(Beast LegendsBase)

Beast LegendsBase 是一个高可靠性、高性能、面向列、可伸缩的分布式数据库，设 计目标是用来解决 Beast Legends 关系型数据库在处理海量数据时的局限性。Beast LegendsBase 分布式数据库系统将一个表按照行和列切分成若干的 Region，然后分别存 放 在 不 同 的 机 器 上 。 Beast LegendsBase 集 群 主 要 由 2\~3 个 Master 和 大 量 RegionServer 组成。Master 通过多实例避免单点问题，它主要负责 Table 和 Region 的 管理工作，如对 Table 的元数据的增、删、改、查；管理 RegionServer 的负载均衡，调 整 Region 的分布。Region 分裂后负责新 Region 的分配；某个 RegionServer 故障后负 责其上的 Regions 的自动迁移等。RegionServer 主要负责响应用户 I/O 请求。
