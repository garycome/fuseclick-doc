# Smart Limitation
The marketing company’s operations team is responsible for integrating with partners and improving the performance of their campaigns. They need to analyze the data online and take action as quickly as possible to promote ROI.    
FuseClick's Smart Limitation feature exactly meets the requirements of automation for the operation teams, which can analyst the data of offers, campaigns, affiliates and even the sub affiliates, then block those with poor performance automatically, and it also can be used for click CAPs. 

## Choosing Entities
You can set multiple rules in the Smart Limitation feature. Each rule represent a turning strategy for one or many offers and affiliates.  
If there are only offers selected and no affiliates, the rule will apply to all campaigns that belong to these offers. Similarly, only selecting affiliates menas  the rule will apply to all campaigns of these affiliates.

## Automation for Campaigns Performance Turning 
Two thresholds can be set in a rule, one for clicks and the other for conversions or CR. In a certain peroid(daily/weekly/two weeks/overall), when the traffic exceeds the click theshold, and the conversions(CR) is still less than the other threshold, then the campaign will be paused.  
Setting the first threshold for clicks will ensure that the sample size is statistically significant enough to avoid accidentally pausing the campaign.

## Automation for Sub-Affiliates Performance Turning
For those affiliates who have many sub-affiliates, pausing their campaign means blocking all traffic for all sub-affiliates. However, this is not the most profitable way for turning ROI.   
We need to analyze the performance of each sub-affiliate and then only block those sub-affiliates with poor performance. The operations team only needs to set the rule action as a sub-affiliate, which is "Blocking Sub-Affiliate form the Campaign". The system will do all the analysts and blocking works automatically.
![smart_limitation_sub_affiliate_rule](../image/smart_limitation_sub_affiliate_rule.png)

The other feature "Parameter Targeting" in FuseClick can be used to set the whitelist of sub-affiliate, which means only the traffic from the whitelisted sub-affiliates can be accepted.

## Implementation of Click CAP
Besides these CAP features for Budget and Conversions, the Smart Limitation feature can be used for CAP of Clicks. 
If you only set the threshold for click and no threshold for conversions or CR,  then the rule is a Click CAP Rule. The system will limit the number of daily clicks or total clicks for campaigns or sub-affiliates.

The system analyzes performance and takes action according to the Smart Limitation rules automatically and continuously. The operations team checks the rule action log and changes the rules as needed easily.
