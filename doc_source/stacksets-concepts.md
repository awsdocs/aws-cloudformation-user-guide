# StackSets concepts<a name="stacksets-concepts"></a>

When you use StackSets, you work with *stack sets*, *stack instances*, and *stacks*\.

**Topics**
+ [Administrator and target accounts](#stacksets-concepts-accts)
+ [Stack sets](#stacksets-concepts-stackset)
+ [Stack instances](#stacksets-concepts-stackinstances)
+ [Stack set operations](#stacksets-concepts-ops)
+ [Stack set operation options](#stackset-ops-options)
+ [Tags](#stackset-concepts-tags)
+ [Stack set and stack instance status codes](#stackset-status-codes)

## Administrator and target accounts<a name="stacksets-concepts-accts"></a>

An *administrator account* is the AWS account in which you create stack sets\. A stack set is managed by signing in to the AWS administrator account in which it was created\. A *target account* is the account into which you create, update, or delete one or more stacks in your stack set\. Before you can use a stack set to create stacks in a target account, you must set up a trust relationship between the administrator and target accounts\.

## Stack sets<a name="stacksets-concepts-stackset"></a>

A *stack set* lets you create stacks in AWS accounts across regions by using a single AWS CloudFormation template\. All the resources included in each stack are defined by the stack set's AWS CloudFormation template\. As you create the stack set, you specify the template to use, as well as any parameters and capabilities that template requires\.

After you've defined a stack set, you can create, update, or delete stacks in the target accounts and Regions you specify\. When you create, update, or delete stacks, you can also specify operation preferences, such as the order of regions in which you want the operation to be performed, the failure tolerance beyond which stack operations stop, and the number of accounts in which operations are performed on stacks concurrently\.

A stack set is a regional resource\. If you create a stack set in one Region, you cannot see it or change it in other Regions\.

**Permissions models for stack sets**

Stack sets can be created using either *self\-managed* permissions or *service\-managed* permissions\.

With *self\-managed* permissions, you create the IAM roles required by StackSets to deploy across accounts and Regions\. These roles are necessary to establish a trusted relationship between the account you're administering the stack set from and the account you're deploying stack instances to\. Using this permissions model, StackSets can deploy to any AWS account in which you have permissions to create an IAM role\.

With *service\-managed* permissions, you can deploy stack instances to accounts managed by AWS Organizations\. Using this permissions model, you don't have to create the necessary IAM roles; StackSets creates the IAM roles on your behalf\. With this model, you can also enable automatic deployments to accounts that are added to your organization in the future\.

## Stack instances<a name="stacksets-concepts-stackinstances"></a>

A *stack instance* is a reference to a stack in a target account within a Region\. A stack instance can exist without a stack; for example, if the stack could not be created for some reason, the stack instance shows the reason for stack creation failure\. A stack instance is associated with only one stack set\.

The following figure shows the logical relationships between stack sets, stack operations, and stacks\. When you update a stack set, *all* associated stack instances are updated throughout all accounts and Regions\.

![\[A single stack set can serve as the basis to create, update, or delete stacks instances and stacks across multiple accounts and Regions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack_sets_operations_stacks_sv.png)

## Stack set operations<a name="stacksets-concepts-ops"></a>

You can perform the following operations on stack sets\.

Create stack set  
Creating a new stack set includes specifying an AWS CloudFormation template that you want to use to create stacks, specifying the target accounts in which you want to create stacks, and identifying the AWS Regions in which you want to deploy stacks in your target accounts\. A stack set ensures consistent deployment of the same stack resources, with the same settings, to all specified target accounts within the Regions you choose\.

Update stack set  
When you update a stack set, you push changes out to stacks in your stack set\. You can update a stack set in one of the following ways\. Note that your template updates always affect all stacks; you cannot selectively update the template for some stacks in the stack set, but not others\.  
+ Change existing settings in the template or add new resources, such as updating parameter settings for a specific service, or adding new Amazon EC2 instances\.
+ Replace the template with a different template\.
+ Add stacks in existing or additional target accounts, across existing or additional Regions\.

Delete stacks  
When you delete stacks, you are removing a stack and all its associated resources from the target accounts you specify, within the Regions you specify\. You can delete stacks in the following ways\.  
+ Delete stacks from some target accounts, while leaving other stacks in other target accounts running\.
+ Delete stacks from some Regions, while leaving stacks in other Regions running\.
+ Delete stacks from your stack set, but save them so they continue to run independently of your stack set by choosing the **Retain Stacks** option\. Retained stacks are managed in AWS CloudFormation, outside of your stack set\.
+ Delete all stacks in your stack set, in preparation for deleting your entire stack set\.

Delete stack set  
You can delete your stack set only when there are no stack instances in it\.

## Stack set operation options<a name="stackset-ops-options"></a>

The options described in this section help to control the time and number of failures allowed to successfully perform stack set operations, and prevent you from losing stack resources\.

Maximum concurrent accounts  
This setting, available in create, update, and delete workflows, lets you specify the maximum number or percentage of target accounts in which an operation is performed at one time\. A lower number or percentage means that an operation is performed in fewer target accounts at one time\. Operations are performed in one Region at a time, in the order specified in the **Deployment order **box\. For example, if you are deploying stacks to 10 target accounts within two Regions, setting **Maximum concurrent accounts** to **50** and **By percentage** will deploy stacks to five accounts in the first Region, then the second five accounts within the first Region, before moving on to the next Region and beginning deployment to the first five target accounts\.  
When you choose **By percentage**, if the specified percentage does not represent a whole number of your specified accounts, AWS CloudFormation rounds down\. For example, if you are deploying stacks to 10 target accounts, and you set **Maximum concurrent accounts** to **25** and **By percentage**, AWS CloudFormation rounds down from deploying 2\.5 stacks concurrently \(which would not be possible\) to deploying two stacks concurrently\.   
Note that this setting lets you specify the *maximum* for operations\. For large deployments, under certain circumstances the actual number of accounts acted upon concurrently may be lower due to service throttling\. The maximum speed of deployment is 100 concurrent stack instances per stack set\. 

Failure tolerance  
This setting, available in create, update, and delete workflows, lets you specify the maximum number or percentage of stack operation failures that can occur, per Region, beyond which AWS CloudFormation stops an operation automatically\. A lower number or percentage means that the operation is performed on fewer stacks, but you are able to start troubleshooting failed operations faster\. For example, if you are updating 10 stacks in 10 target accounts within three Regions, setting **Failure tolerance** to **20** and **By percentage** means that a maximum of two stack updates in a Region can fail for the operation to continue\. If a third stack in the same Region fails, AWS CloudFormation stops the operation\. If a stack could not be updated in the first Region, the update operation continues in that Region, and then moves on to the next Region\. If two stacks cannot be updated in the second Region, the failure tolerance of 20% is reached; if a third stack in the Region fails, AWS CloudFormation stops the update operation, and does not go on to subsequent Regions\.  
When you choose **By percentage**, if the specified percentage does not represent a whole number of your stacks within each Region, AWS CloudFormation rounds down\. For example, if you are deploying stacks to 10 target accounts in three Regions, and you set **Failure tolerance** to **25** and **By percentage**, AWS CloudFormation rounds down from a failure tolerance of 2\.5 stacks \(which would not be possible\) to a failure tolerance of two stacks per Region\.

Retain stacks  
This setting, available in delete stack workflows, lets you keep stacks and their resources running even after they have been removed from a stack set\. When you retain stacks, AWS CloudFormation leaves stacks in individual accounts and Regions intact\. Stacks are disassociated from the stack set, but the stack and its resources are saved\. After a delete stacks operation is complete, you manage retained stacks in AWS CloudFormation, in the target account \(not the administrator account\) in which they were created\. Retaining stacks permanently disassociates a stack from a stack set; the stack cannot be added to the stack set again, and it cannot be added to a new stack set\.

## Tags<a name="stackset-concepts-tags"></a>

You can add tags during stack set creation and update operations by specifying key and value pairs\. Tags are useful for sorting and filtering stack set resources for billing and cost allocation\. For more information about how tags are used in AWS, see [Using cost allocation tags](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\. After you specify the key\-value pair, choose **\+** to save the tag\.You can delete tags that you are no longer using by choosing the red **X** to the right of a tag\.

Tags that you apply to stack sets are applied to all stacks, and the resources that are created by your stacks\. Tags can be added at the stack\-only level in AWS CloudFormation, but those tags might not show up in StackSets\.

Although StackSets does not currently add any system\-defined tags, you should not start the key names of any tags with the string `aws:`\.

## Stack set and stack instance status codes<a name="stackset-status-codes"></a>

AWS CloudFormation StackSets generates status codes for stack set operations and stack instances\.

The following table describes status codes for stack set operations\.


| Stack set operation status | Description | 
| --- | --- | 
|  `RUNNING`  |  The operation is currently in progress\.  | 
|  `SUCCEEDED`  |  The operation finished without exceeding the failure tolerance for the operation\.  | 
|  `FAILED`  |  The number of stacks on which the operation could not be completed exceeded the user\-defined failure tolerance\. The failure tolerance value you've set for an operation is applied for each Region during stack creation and update operations\. If the number of failed stacks within a Region exceeds the failure tolerance, the status of the operation in the Region is set to `FAILED`\. The status of the operation as a whole is also set to `FAILED`, and AWS CloudFormation cancels the operation in any remaining Regions\.  | 
|  `QUEUED`  |  `QUEUED`: \[Service\-managed permissions\] For automatic deployments that require a sequence of operations, the operation is queued to be performed\. For example: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html)  | 
|  `STOPPING`  |  The operation is in the process of stopping, at the user's request\.  | 
| STOPPED |  The operation has been stopped, at the user's request\.  | 

The following table describes status codes for stack instances within stack sets\.


| Stack instance status | Description | 
| --- | --- | 
|  `CURRENT`  |  The stack is currently up to date with the stack set\.  | 
|  `OUTDATED`  |  The stack is not currently up to date with the stack set for one of the following reasons\. [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html)  | 
|  `INOPERABLE`  |  A `DeleteStackInstances` operation has failed and left the stack in an unstable state\. Stacks in this state are excluded from further `UpdateStackSet` operations\. You might need to perform a `DeleteStackInstances` operation, with `RetainStacks` set to `true`, to delete the stack instance, and then delete the stack manually\.  | 
|  `CANCELLED`  |  The operation in the specified account and Region has been cancelled\. This is either because a user has stopped the stack set operation, or because the failure tolerance of the stack set operation has been exceeded\.  | 
|  `FAILED`  |  The operation in the specified account and Region failed\. If the stack set operation fails in enough accounts within a Region, the failure tolerance for the stack set operation as a whole might be exceeded\.  | 
|  `PENDING`  |  The operation in the specified account and Region has yet to start\.  | 
|  `RUNNING`  |  The operation in the specified account and Region is currently in progress\.  | 
|  `SUCCEEDED`  |  The operation in the specified account and Region completed successfully\.  | 