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
经过一段时间的优化，已知某些子渠道流量收益好，可以利用Parameter Rule功能，开启子渠道白名单，系统只接受这些子渠道的流量，其他的会自动屏蔽。

# 实现 Daily Click CAP
系统有 Budget CAP 和 Conversion CAP，设定支付给渠道的成本上限和转化数量限制，CAP 的时间范围可以是 Daily、Weekly、Monthly或者 Overall。  
  
|CAP对象|Daily|Weekly|Monthly|Overall|    
| --- | --- | --- | --- | --- |  
|Budget|Y|Y|Y|Y|    
|Conversion|Y|Y|Y|Y|    
|Click|Y|Y|Y|Y|  
