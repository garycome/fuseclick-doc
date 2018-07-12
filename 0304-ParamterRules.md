# 参数过滤规则
## 功能
系统提供多种方式进行渠道对Offer的访问权限的控制。
例如为广告主或offer，设置渠道黑名单、白名单，或者利用 Smart Limitation 功能按效果自动控制Campaign状态等。

但是，实际运营中的情况确是如下类型：渠道的某些子渠道的质量高低不一致，广告主希望流量质量越高越好。
这就需要一个更细粒度的条件对子渠道质量进行管控。 Blocked Parameters功能即可满足，该功能从子渠道的流量参数值考虑，对其进行质量管控。

![BlockParameters](./image/BlockParameters.jpg)


## 设置
针对不同Offer或者Campaign分别设置Blocked Parameters规则。
可选参数范围：
* 子渠道 Sub Affiliate ID
* Affiliate Sub ID 1（即s1）
* Affiliate Sub ID 2（即s2）
* Affiliate Sub ID 3（即s3）
* Affiliate Sub ID 4（即s4）
* Affiliate Sub ID 5（即s5）

选择参数并给出其对应的参数值，若进入系统的流量中携带有该参数，且值与设置的参数值之一相同，则该流量会被拒绝。

除上述6种参数外，系统还提供一个 Device ID 规则，即流量进入系统时携带的Device ID为空值，也会被拒绝。

## 样例：屏蔽子渠道
渠道通过Sub Affiliate ID传递其子渠道值，当该渠道发现他的某些子渠道的流量质量过低或者较差，可以通过Blocked Parameters功能进行过滤。
即在 Blocked Parameters 中添加上 Sub Affiliate ID 并配上想要屏蔽的子渠道ID或者名称，后续该子渠道的流量就会被拒绝。

## 样例：屏蔽Device ID为空的流量
如果某个 Offer 要求所有流量必须带有设备ID，可以在Blocked Parameters 中设置Device ID且值为空，则代表Device ID 为空的流量将会被屏蔽。

通过上述规则，可以提高到达广告主系统的流量质量。




