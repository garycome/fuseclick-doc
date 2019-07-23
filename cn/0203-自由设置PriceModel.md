# 一个单子，渠道送量，自己也买量，运营需要利器？

从广告主那边接了一个直客的单子，下发给一些优质渠道去跑，公司内部也有media buyer 团队从DSP上直接买量。

两种推广方式采用不同的成本计算方式，对于渠道使用CPI计算，media buyer使用CPM计算。运营需要把这两种推广方式的数据汇总到一起，查看、分析、调整。

使用FuseClick，可以自动运营、管理上述场景。

在系统内，设置单子的Revenue Type为CPI，表示从广告主按CPI方式获得收益；将单子分发给渠道，设置Payout Type为CPI，流出公司利润差额，设定价格；将单子推送给Media Buyer，设置Payout Type为CPM，设定价格为买量的CPM价格。

![MultiplePriceModel](../image/fuseclick_mutliple_price_model.png)

当系统接收到来自DSP平台的impression报送时，按CPM价格计算Media Buyer团队的成本；当系统接到归属到渠道的转化时，按Payout CPI价格计算应支付给渠道的支出。

系统自动将这两种支出汇总为单子的Cost，来自广告主的CPI Revenue是单子的总Revenue，使得运营一站式管理这些业务。

另外，系统还可以自动、定期对单子进行检测；对推广Campaign进行监控，自动屏蔽效果不佳的渠道、子渠道等，从而提高运营效益。



