# Smart Link
将offer编组，使用一个针对组的投放链接，系统自动将click引导到最优的offer。
为了完成这个过程，FuseClick研发了一整套完备的功能，包含Smart Offer Group, Auto-Recruiter, Auto-Remover, Smart Testing 等。
![SmartLink](../image/SmartLink.jpg)

## Smart Group
Smart Group包含多个offer，根据广告主、offer类别、流量国家、运营商等属性选择offer加入组内。

## Auto-Recruiter
offer的自动化编组。自动定时搜索offer，将符合条件的offer加入组内。
可以为每个Smart Group单独设置Recruiter规则，说明offer需要满足的条件，例如泰国、iOS系统、Game类别。
每次有offer加入，系统会记录日志方便查看。

### 按属性平均加入
如果系统内offer特别多，您又不想这些offer全部加入Smart Group，可以设定每次Recruiter执行时，加入的offer总数。
更进一步，可以按照某个属性（例如： 国家），平均加入offer。
比如设置每次加入50个offer，符合条件的offer覆盖了10个国家，那么每个国家就会加入5个offer。

## Auto-Remover
对于性能不好的offer，避免浪费流量，需要将其移除。
可以设置对接受了超过一定量的offer,如果CR低于期望值，将其从组内移除，也可以同时停止这个offer。
当某个offer被移除时，系统会记录日志方便查看。

## Smart Testing
对于新offer，其CR、EPC等指标都没有，如果都按照这些指标为click优选offer，新offer将无法获得点击。
Smart Testing 根据组内的新offer的多少，自动将相应比例的流量跳转到这些新offer上。对这些offer进行测试。当测试的点击足够多, 测试自动结束。

## Smart Link
当系统接受到一个smart link 的点击时，系统执行以下操作：
* 在Smart Group组内搜索符合点击特征（国家、操作系统、运行商等）的offer
* 将这些offer按照EPC性能排序
* 获取排序较高的一部分offer（TOP N，例如 TOP 5），在其中随机、或按权重选择一个，作为click的目标offer。
采用 TOP-N 算法，避免了流量过于集中到某个offer，也使得头部offer都有机会获得流量，最大化收益。