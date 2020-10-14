# Monitor and roll back stack operations<a name="using-cfn-rollback-triggers"></a>

Rollback triggers enable you to have AWS CloudFormation monitor the state of your application during stack creation and updating, and to roll back that operation if the application breaches the threshold of any of the alarms you've specified\. For each rollback trigger you create, you specify the Cloudwatch alarm that AWS CloudFormation should monitor\. AWS CloudFormation monitors the specified alarms during the stack create or update operation, and for the specified amount of time after all resources have been deployed\. If any of the alarms goes to ALARM state during the stack operation or the monitoring period, AWS CloudFormation rolls back the entire stack operation\.

You can set a monitoring time from the default of 0 up to 180 minutes\. During this time, AWS CloudFormation monitors all the rollback triggers after the stack creation or update operation deploys all necessary resources\. If any of the alarms goes to ALARM state during the stack operation or this monitoring period, AWS CloudFormation rolls back the entire stack operation\. Then, for update operations, if the monitoring period expires without any alarms going to ALARM state, CloudFormation proceeds to dispose of old resources as usual\. If you set a monitoring time but do not specify any rollback triggers, AWS CloudFormation still waits the specified period of time before cleaning up old resources for update operations\. You can use this monitoring period to perform any manual stack validation desired, and manually cancel the stack creation or update as necessary\. If you set a monitoring time of 0 minutes, AWS CloudFormation still monitors the rollback triggers during stack creation and update operations and rolls back the operation if an alarm goes to ALARM state\. Then, for update operations with no breaching alarms, it begins disposing of old resources immediately once the operation completes\.

By default, CloudFormation only rolls back stack operations if an alarm goes to ALARM state, not INSUFFICIENT\_DATA state\. To have AWS CloudFormation roll back the stack operation if an alarm goes to INSUFFICIENT\_DATA state as well, edit the CloudWatch alarm to treat missing data as `breaching`\. For more information, see [Configuring how CloudWatch alarms treat missing data](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html#alarms-and-missing-data) in Amazon CloudWatch User Guide\.

AWS CloudFormation does not monitor rollback triggers when it rolls back a stack during an update operation\.

You can add a maximum of five rollback triggers\. To add a rollback trigger, you specify the ARN \(Amazon Resource Name\) of the CloudWatch alarm\. Currently, only **AWS::CloudWatch::Alarm** types can be used as rollback triggers\. 

If a given Cloudwatch alarm is missing, the entire stack operation fails and is rolled back\.

Be aware that access to Amazon CloudWatch requires credentials\. Those credentials must have permissions to access AWS resources, such as retrieving CloudWatch metric data about your cloud resources\. For more information, see [Authentication and access control for Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/auth-and-access-control-cw.html) in Amazon CloudWatch User Guide\.

**To add rollback triggers during stack creation or updating**

1. During [creating](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html) or [updating](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) a stack, on the **Configure stack options** page, under **Advanced options**, go to **Rollback configuration**\.

1. Specify a monitoring time between 0 and 180 minutes\. The default is 0\.

1. Enter the ARN of the Cloudwatch alarm you want to use as a rollback trigger, and click **Add CloudWatch alarm ARN**\. 

   You can add a maximum of five rollback triggers\.

**To add rollback triggers to a change set**

1. During [creating](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-create.html) or updating a change set, on the **Configure stack options** page, under **Advanced options**, go to **Rollback configuration**\.

1. Specify a monitoring time between 0 and 180 minutes\. The default is 0\.

1. Enter the ARN of the Cloudwatch alarm you want to use as a rollback trigger, and click **Add CloudWatch alarm ARN**\.

   You can add a maximum of five rollback triggers\.

**To view rollback triggers for a stack**
+ On the **Stacks** page, select the stack you wish to view from the list on the left\. On the **Stack info** tab, under **Advanced options**, expand the **Rollback configuration** section\.