# Smart Limitation 的多种用法
在线推广时，运营部门的日常就是对接、测试、调优，对数据是最为敏感的，从各种维度、聚合数据中发现各种花式的效果比对，从而去伪存真，提升效益。
FuseClick 的 Smart Limitation 功能，可以自动完成筛选、过滤、优化工作。

# 设定阈值，自动关停低效 Campaign
当 Campaign 的流量超过某个基准值，如果CR低于阈值或转化少于设定值，系统自动将Campaign转为Block状态。   
其中，设定流量基准值相当于给定对流量的采用，样本量足够才会具有统计意义，以免发生误停的现象。  
以下是一些规则实例。  
1. for all campaigns, in 7 days, if clicks > 100000 and cr < 0.02%, then block campaign  
2. for campaigns of offer5, if daily clicks > 25000 and daily conversions < 2, then block campaign  
3. for campaigns of affiliate200, in 15 days, if clicks > 300000 and cr < 0.05%, then block campaign

# 设定阈值，自动屏蔽子渠道
大的渠道汇聚了一些子渠道的流量，如果简单地在Campaign层面做优化，会把不同子渠道的流量混合在一起处理，粒度不够精细。 
此时，可以使用针对子渠道的规则，对Campaign内的流量进行过滤和筛选。    
![smart_limitation_sub_affiliate_rule](../image/smart_limitation_sub_affiliate_rule.png)    
图中示例规则，对 #79 渠道的Campaign，如果某个子渠道的点击数超过20万而CR低于0.02%，系统自动屏蔽该Campaign下的该子渠道的流量，而其他子渠道流量正常。  
经过一段时间的优化，已知某些子渠道流量收益好，可以利用Parameter Rule功能，开启**子渠道白名单**，系统只接受这些子渠道的流量，其他的会自动屏蔽。

# 实现 Daily Click CAP
系统基准功能中，包含有 Offer 和 Campaign 的 Budget CAP 和 Conversion CAP，用来设定支付给渠道的成本上限和转化数量限制。  
除了按照总量限制外，也还可以按照天/周/月等区间限制。  
利用Smart Limitation规则，运营可以对 Click 也进行 CAP 限制，只需在规则中，不设置 Conversion 或 CR 条件，仅设置 Click CAP 数量即可。这样，可以限制系统接收某个 Campaign、或某个子渠道的 Daily Click 数量或总数。   

|CAP对象|Daily|Weekly|Monthly|Overall|    
| --- | --- | --- | --- | --- |  
|Budget|Y|Y|Y|Y|    
|Conversion|Y|Y|Y|Y|    
|Click|Y|-|-|Y|
  
当广告主对于CR有要求，或者对流量总量有限制时，使用 Smart Limitation 功能设置反映这些要求的规则，可以减轻运营人员的工作负担，而且这些规则在后台自动运行，全年无休。  



