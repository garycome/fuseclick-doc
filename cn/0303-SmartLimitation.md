# Smart Limitation 的多种用法
在线推广时，运营部门的日常就是对接、测试、调优，对数据是最为敏感的，从各种维度、聚合数据中发现各种花式的效果比对，从而去伪存真，提升效益。
FuseClick 的 Smart Limitation 功能，可以自动完成筛选、过滤、优化工作。

# 设定 CR 阈值，自动关停低效 Campaign
当 Campaign 的流量超过某个基准值，如果CR低于阈值或转化少于设定值，系统自动将Campaign转为Block状态。   
其中，设定流量基准值相当于给定对流量的采用，样本量足够才会具有统计意义，以免发生误停的现象。  
 ```for all campaigns, if clicks > 100000 and cr < 0.02% then block campaign``` 



