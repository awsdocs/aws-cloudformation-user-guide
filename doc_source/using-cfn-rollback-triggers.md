# Monitor and roll back stack operations<a name="using-cfn-rollback-triggers"></a>

Rollback triggers enable you to have AWS CloudFormation monitor the state of your application during stack creation and updating, and to roll back that operation if the application breaches the threshold of the alarms you've specified\. For each rollback trigger you create, you specify the CloudWatch alarm that CloudFormation should monitor\. CloudFormation monitors the specified alarms during the stack create or update operation, and for the specified amount of time after all resources have been deployed\. If any of the alarms goes to `ALARM` state during the stack operation or the monitoring period, CloudFormation rolls back the entire stack operation\.

You can set a monitoring time from the default of 0 up to 180 minutes\. During this time, CloudFormation monitors all the rollback triggers after the stack creation or update operation deploys all necessary resources\. If any of the alarms goes to `ALARM` state during the stack operation or this monitoring period, CloudFormation rolls back the entire stack operation\. Then, for update operations, if the monitoring period expires without any alarms going to `ALARM` state, CloudFormation proceeds to dispose of old resources as usual\. If you set a monitoring time but don't specify any rollback triggers, CloudFormation still waits the specified period of time before cleaning up old resources for update operations\. You can use this monitoring period to perform any manual stack validation desired, and manually cancel the stack creation or update as necessary\. If you set a monitoring time of 0 minutes, CloudFormation still monitors the rollback triggers during stack creation and update operations and rolls back the operation if an alarm goes to `ALARM` state\. Then, for update operations with no breaching alarms, it begins disposing of old resources immediately once the operation completes\.

By default, CloudFormation only rolls back stack operations if an alarm goes to `ALARM` state, not `INSUFFICIENT_DATA` state\. To have CloudFormation roll back the stack operation if an alarm goes to `INSUFFICIENT_DATA` state as well, edit the CloudWatch alarm to treat missing data as `breaching`\. For more information, see [Configuring how CloudWatch alarms treat missing data](AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html#alarms-and-missing-data) in Amazon CloudWatch User Guide\.

CloudFormation doesn't monitor rollback triggers when it rolls back a stack during an update operation\.

You can add a maximum of 5 rollback triggers\. To add a rollback trigger, specify the Amazon Resource Name \(ARN\) of the CloudWatch alarm\. Currently, `AWS::CloudWatch::Alarm` and `AWS::CloudWatch::CompositeAlarm` types can be used as rollback triggers\. For more information about CloudWatch alarms, see [Using Amazon CloudWatch alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html) in Amazon CloudWatch User Guide\.

If a given CloudWatch alarm is missing, the entire stack operation fails and rolls back\.

Be aware that access to Amazon CloudWatch requires credentials\. Those credentials must have permissions to access AWS resources, such as retrieving CloudWatch metric data about your resources\. For more information, see [Authentication and access control for Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/auth-and-access-control-cw.html) in Amazon CloudWatch User Guide\.

## To add rollback triggers during stack creation or updating<a name="using-cfn-rollback-triggers-create"></a>

To add rollback triggers to a stack creation or update, specify the Amazon CloudWatch alarms in the **Rollback configuration** section\.

1. During [creating](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html) or [updating](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) a stack, on the **Configure stack options** page, under **Advanced options**, expand the **Rollback configuration** section\.

1. Enter a monitoring time between `0` – `180` minutes\. The default value is `0`\.

1. Specify the ARN of the CloudWatch alarm or composite alarm you want to use as a rollback trigger, and select **Add CloudWatch alarm ARN**\.

   For example, the following is an ARN for a CloudWatch alarm or composite alarm, `arn:aws:cloudwatch:us-east-1:123456789012:alarm:MyAlarmName`\.

1. Select **Next** and review the details of your stack\.

1. After you review the stack creation settings and the estimated cost of your stack, choose **Create stack** to launch your stack\.

*Results*: You've successfully added Amazon CloudWatch alarms to your stack\.

## To add rollback triggers to a change set<a name="using-cfn-rollback-triggers-change-set"></a>

To add rollback triggers to a change set, create a change set by select your stack template and specify the Amazon CloudWatch alarms in the **Rollback configuration** section\.

1. During [creating](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-create.html) or updating a change set, on the **Configure stack options** page, under **Advanced options**, expand the **Rollback configuration** section\.

1. Enter a monitoring time between `0` – `180` minutes\. The default value is `0`\.

1. Specify the ARN of the CloudWatch alarm or composite alarm you want to use as a rollback trigger, and select **Add CloudWatch alarm ARN**\.

   For example, the following is an ARN for a CloudWatch alarm or composite alarm, `arn:aws:cloudwatch:us-east-1:123456789012:alarm:MyAlarmName`\.

1. Select **Next** and review the details of your stack\.

1. After you review the stack creation settings and the estimated cost of your stack, choose **Create change set**\.

1. Review the **Create change set** module and select **Create change set**\.

1. \(Optional\) To complete creating a new stack based on the change set, choose **Execute**, specify your rollback configuration, and then choose **Execute change set**\.

*Results*: You've successfully added Amazon CloudWatch alarms to your change set\.

## To view rollback triggers for a stack<a name="using-cfn-rollback-triggers-view"></a>

To view rollback triggers for a stack, see the **Rollback configuration** section\.

1. On the **Stacks** page, select the stack you want to view from the list on the left\.

1. On the **Stack info** tab, expand the **Rollback configuration** section\.

*Results*: Rollback triggers are displayed in the **Rollback configuration** section, if rollback triggers were specified\.

## To view rollback triggers for a change set<a name="using-cfn-rollback-triggers-view-change-set"></a>

To view rollback triggers for a change set, see the **Rollback configuration** section\.

1. On the **Stacks** page, select the stack you want to view from the list on the left\.

1. Select the **Change sets** tab, and select the change set you want to view\.

1. Select the **Input** tab, and view the **Rollback configuration** section\.

*Results*: Rollback triggers are displayed in the **Rollback configuration** section, if rollback triggers were specified\.