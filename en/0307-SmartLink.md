# Smart Link of FuseClick

Smart Link is a tracking link for one Smart Group, which contains a number of selected offers. 
FuseClick tracking system redirects each click of a Smart Link to one of those offers as the best selection in the Smart Group. 
![SmartLink](../image/SmartLink.jpg)

Smart link feature consists of tools which allow you to configure your smart offer groups, setup the automation rules and Smart testing.

## Smart Group

Smart group creation is the first step in the process. 
You can add offers to the smart group by filters, such as advertisers, categories, countries, OS, and carriers.

The system provides three lists of offers for each Smart Group: 
* Available Offer List, 
* Selected Offer List, 
* Removed Offer List. 
You can customize offers in the lists or remove the offers from the Smart Group.

## Auto-Recruit
Configure Auto-recruit and Auto-remove automation tool.
You can add the rules for Auto-recruit and Auto-remove, to automate the performance of the Smart link.
An Auto-Recruit rule combines multiple criteria (e.g., Country: Thailand & Device OS: iOS &Category: Game). 
FuseClick traffic computing system runs recruiting jobs periodically and smartly. 
The system adds available offers to the Smart Group according to Auto-Recruit rule all the time.
You can maintain a specified rule for each Smart Group. 
It is possible to configure an interval for all Smart Groups and then the system will run recruit jobs periodically. 
Once an offer is recruited, the system will record a log for the action. 
The specific details you can go to Smart Link -> Smart Offer Groups -> Add Recruit Rule to customize.

## Auto-Removal
The FuseClick system provides Auto-Remove feature to remove poor performing offers from the smart group automatically based on the criteria. 
You can set different Auto-Remove rules with a combination of multiple requirements, including countries, OS, and carriers. 
Once the offer is removed, the system will record the log data of the action. 
Go to Smart Link -> Settings -> Offer Auto-Remove Rules, you can set an Auto-Remove scenario like this: 
if the total number of clicks on an offer is more than 10,000 and the conversions (or EPC, CR) are less than 10, the back-end system will remove the offer from the group. 
FuseClick system can also pause the offer according to the rule apart from removing.

## Smart Testing
For new offers recruited, statistics such as clicks or conversions are not available. 
If the system treats them as the same as those older offers, these new offers will not receive any traffic. That’s where the smart testing tool comes in to picture. 
The smart testing tool calculates the percentage of the new offers in the Smart Group and distributes the corresponding proportion of traffic to these new offers to generate performance data. 
The user is able to assign a number in the rule to limit testing clicks to new offers. Once that number is reached, the system will end the test to the offers automatically. 
The specific details you can go to Smart Link -> Settings to customize.

## Smart Link Log
This log displays all the details about each action taken by Smart link against the smart rules.
