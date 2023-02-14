# Setting AWS CloudFormation stack options<a name="cfn-console-add-tags"></a>

After specifying [parameters](parameters-section-structure.md) that are defined in the template, you can set additional options for your stack\.

You can set the following stack options:

**Tags**  
Tags are arbitrary key\-value pairs that can be used to identify your stack for purposes such as cost allocation\. For more information about what tags are and how they can be used, see [Tagging your resources](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) in the *Amazon EC2 User Guide*\.  
A **Key** consists of any alphanumeric characters or spaces\. Tag keys can be up to 127 characters long\.  
A **Value** consists of any alphanumeric characters or spaces\. Tag values can be up to 255 characters long\.

**Permissions**  
An existing AWS Identity and Access Management \(IAM\) service role that CloudFormation can assume\.  
Instead of using your account credentials, CloudFormation uses the role's credentials to create your stack\. For more information, see [AWS CloudFormation service role](using-iam-servicerole.md)\.

**Stack failure options**  <a name="rollback"></a>
Specifies the provision failure options for all stack deployments and change set operations\. For more information, see [Stack failure options](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stack-failure-options.html)\.  
The **Roll back all stack resources** option will roll back all resources specified in the template when the stack status is `CREATE_FAILED` or `UPDATE_FAILED`\.  
For create operations, the **Preserve successfully provisioned resources** option preserves the state of successful resources, while failed resources will stay in a failed state until the next update operation is performed\.  
For update and change set operations, the **Preserve successfully provisioned resources** option preserve the state of successful resources while rolling back failed resources to the last known stable state\. Failed resources will be in an `UPDATE_FAILED` state\. Resources without a last known stable state will be deleted upon the next stack operation\.

You can also set the following advanced options for stack creation:

**Stack policy**  
Defines the resources that you want to protect from unintentional updates during a stack update\. By default, all resources can be updated during a stack update\.  
You can enter the stack policy directly as JSON, or upload a JSON file containing the stack policy\. For more information, see [Prevent updates to stack resources](protect-stack-resources.md)\.

**Rollback configuration**  
Enables you to have CloudFormation monitor the state of your stack during stack creation and updating, and to roll back that operation if the stack breaches the threshold of any of the alarms you've specified\. Specify the CloudWatch alarms that CloudFormation should monitor\. If any of the alarms goes to `ALARM` state during the stack operation or the monitoring period, CloudFormation rolls back the entire stack operation\. For more information, see [Monitor and roll back stack operations](using-cfn-rollback-triggers.md)\.

**Notification options**  
You can specify a new or existing Amazon Simple Notification Service topic where notifications about stack events are sent\.  
If you create an Amazon SNS topic, you must specify a name and an email address where stack event notifications are to be sent\.

**Stack creation options**  
The following options are included for stack creation, but aren't available as part of stack updates\.    
**Timeout**  
Specifies the amount of time, in minutes, that CloudFormation should allot before timing out stack creation operations\. If CloudFormation can't create the entire stack in the time allotted, it fails the stack creation due to timeout and rolls back the stack\.  
By default, there is no timeout for stack creation\. However, individual resources may have their own timeouts based on the nature of the service they implement\. For example, if an individual resource in your stack times out, stack creation also times out even if the timeout you specified for stack creation hasn't yet been reached\.

**To set stack options**

1. On the **Configure stack options** page of the **Create stack** wizard, you can specify tags and permissions\. Use the **Advanced options** section to set additional configuration options for your stack\.

1. When you have entered all your stack options, choose **Next Step** to proceed with [reviewing your stack](cfn-using-console-create-stack-review.md)\.