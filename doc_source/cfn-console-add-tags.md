# Setting AWS CloudFormation Stack Options<a name="cfn-console-add-tags"></a>

After specifying [parameters](parameters-section-structure.md) that are defined in the template, you can set additional options for your stack\.

You can set the following stack options:

**Tags**  
Tags are arbitrary key\-value pairs that can be used to identify your stack for purposes such as cost allocation\. For more information about what tags are and how they can be used, see [Tagging Your Resources](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) in the *Amazon EC2 User Guide*\.  
A **Key** consists of any alphanumeric characters or spaces\. Tag keys can be up to 127 characters long\. A **Value** consists of any alphanumeric characters or spaces\. Tag values can be up to 255 characters long\.

**Permissions**  
An existing AWS Identity and Access Management \(IAM\) service role that AWS CloudFormation can assume\.  
Instead of using your account credentials, AWS CloudFormation uses the role's credentials to create your stack\. For more information, see [AWS CloudFormation Service Role](using-iam-servicerole.md)\.

**Notification Options**  
A new or existing Amazon Simple Notification Service topic where notifications about stack events are sent\.  
If you create an Amazon SNS topic, you must specify a name and an email address, where stack event notifications are sent\.

**Timeout**  
The number of minutes before stack creation times out\. If the stack could not be created before the time expires, creation fails due to timeout and the stack is rolled back\. By default, the stack creation never times out\.

**Rollback on failure**  
Specifies whether the stack should be rolled back if stack creation fails\. Typically, you want to accept the default value of **Yes**\. Select **No** if you want the stack's state retained even if creation fails, such as when you are debugging a stack template\.

**Stack policy**  
Defines the resources that you want to protect from unintentional updates during a stack update\. By default, all resources can be updated during a stack update\. For more information, see [Prevent Updates to Stack Resources](protect-stack-resources.md)\.

**Enable termination protection**  
Prevents a stack from being accidently deleted\. If a user attempts to delete a stack with termination protection enabled, the deletion fails and the stack\-\-including its status\-\-remains unchanged\. For more information, see [Protecting a Stack From Being Deleted](using-cfn-protect-stacks.md)\.

**To set stack options**

1. On the **Options** screen of the **Create Stack** wizard, you can specify tags or set additional options by expanding the **Advanced** section\.

1. When you have entered all of your stack options, click **Next Step** to proceed with [reviewing your stack](cfn-using-console-create-stack-review.md)\.