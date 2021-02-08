# Creating a change set<a name="using-cfn-updating-stacks-changesets-create"></a>

To create a change set for a running stack, submit the changes that you want to make by providing a modified template, new input parameter values, or both\. AWS CloudFormation generates a change set by comparing your stack with the changes you submitted\.

You can either modify a template [before creating the change set](using-cfn-updating-stacks-get-template.md) or during change set creation\.

------
#### [ Create a change set for nested stacks \(console\) ]

**To create a change set for nested stacks \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, choose the running stack for which you want to create a change set\.

1. In the stack details pane, choose **Stack actions**, and then choose **Create change set for current stack**\.

1. On the **Create change set for *stack\-name*** page, do one of the following to modify input parameter values, specify the location of an updated template, or modify the template:    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-create.html)

1. If your template contains parameters, on the **Specify stack details** page, enter or modify applicable input parameter values, and then choose **Next**\.

   If you're reusing the stack's template, AWS CloudFormation populates each parameter with the current value in the stack, with the exception of parameters declared with the `NoEcho` attribute\. To use existing values for those parameters, select **Use existing value**\.

   For more information about using `NoEcho` to mask sensitive information, as well as using dynamic parameters to manage secrets, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

1. On the **Configure stack options** page, update the stack's tags, IAM service role, stack policy, rollback configuration, Amazon SNS notification topic \(if applicable\), or change sets and then choose **Next**\.
**Note**  
Change sets for nested stacks are **Enabled** by default, which will create change sets for all nested stacks specified in your template\. For more information about change sets for nested stacks, see [Change sets for nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/change-sets-for-nested-stacks.html)\.

1. On the **Review *stack\-name*** page, review the changes for this change set\.

   If the template includes AWS Identity and Access Management \(IAM\) resources, select **I acknowledge that AWS CloudFormation might create IAM resources**\. IAM resources can modify permissions in your AWS account; review these resources to ensure that you're permitting only the actions that you intend\. For more information, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\.

1. Choose **Create change set**\. Specify a name for the change set and optionally specify a description of the change set to identify its purpose\. Then, choose **Create change set**\.

   You're redirected to the **Changes** tab of the change set's details page\. While AWS CloudFormation generates the change set, the status of the change set is **CREATE\_IN\_PROGRESS**\. After it has created the change set, AWS CloudFormation sets the status to **CREATE\_COMPLETE**\. In the **Changes** section, AWS CloudFormation lists all of the changes that it will make to your stack\. For more information, see [Viewing a change set](using-cfn-updating-stacks-changesets-view.md)\.  
![\[The details page for the nested change set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-nested-stacks-change-sets-details.png)

   If AWS CloudFormation fails to create the change set \(reports `FAILED` status\), fix the error displayed in the **Status** field, and then recreate the change set\.

------
#### [ Create a change set \(console\) ]

**To create a change set \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, choose the running stack for which you want to create a change set\.

1. In the stack details pane, choose **Stack actions**, and then choose **Create change set for current stack**\.

1. On the **Create change set for *stack\-name*** page, do one of the following to modify input parameter values, specify the location of an updated template, or modify the template:    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-create.html)

1. If your template contains parameters, on the **Specify stack details** page, enter or modify applicable input parameter values, and then choose **Next**\.

   If you're reusing the stack's template, AWS CloudFormation populates each parameter with the current value in the stack, with the exception of parameters declared with the `NoEcho` attribute\. To use existing values for those parameters, select **Use existing value**\.

   For more information about using `NoEcho` to mask sensitive information, as well as using dynamic parameters to manage secrets, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

1. On the **Configure stack options** page, update the stack's tags, IAM service role, stack policy, rollback configuration, Amazon SNS notification topic \(if applicable\), or change sets and then choose **Next**\.
**Note**  
Change sets for nested stacks are **Enabled** by default, which will create change sets for all nested stacks specified in your template\. To create a change set for the current stack only, choose **Disabled**\. For more information about change sets for nested stacks, see [Change sets for nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/change-sets-for-nested-stacks.html)\.

1. On the **Review *stack\-name*** page, review the changes for this change set\.

   If the template includes AWS Identity and Access Management \(IAM\) resources, select **I acknowledge that AWS CloudFormation might create IAM resources**\. IAM resources can modify permissions in your AWS account; review these resources to ensure that you're permitting only the actions that you intend\. For more information, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\.

1. Choose **Create change set**\. Specify a name for the change set and optionally specify a description of the change set to identify its purpose\. Then, choose **Create change set**\.

   You're redirected to the **Changes** tab of the change set's details page\. While AWS CloudFormation generates the change set, the status of the change set is **CREATE\_IN\_PROGRESS**\. After it has created the change set, AWS CloudFormation sets the status to **CREATE\_COMPLETE**\. In the **Changes** section, AWS CloudFormation lists all of the changes that it will make to your stack\. For more information, see [Viewing a change set](using-cfn-updating-stacks-changesets-view.md)\.  
![\[The details page for the change set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-change-sets-details.png)

   If AWS CloudFormation fails to create the change set \(reports `FAILED` status\), fix the error displayed in the **Status** field, and then recreate the change set\.

------

**To create a change set \(AWS CLI\)**
+ Run the [aws cloudformation create\-change\-set](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-change-set.html) command\.

  You submit your changes as command options\. You can specify new parameter values, a modified template, or both\. For example, the following command creates a change set named `SampleChangeSet` for the `SampleStack` stack\. The change set uses the current stack's template, but with a different value for the `Purpose` parameter:

  ```
  aws cloudformation create-change-set --stack-name arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000
  --change-set-name SampleChangeSet --use-previous-template --parameters ParameterKey="InstanceType",UsePreviousValue=true ParameterKey="KeyPairName",UsePreviousValue=true ParameterKey="Purpose",ParameterValue="production"
  ```