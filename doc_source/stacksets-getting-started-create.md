# Create a New Stack Set<a name="stacksets-getting-started-create"></a>

You can create a stack set in either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\.

**To create a stack set by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. At the top of the **StackSets** page, choose **Create StackSet**\.

1. Under **Prerequisite \- Prepare template**, choose **Use a sample template**\.

1. Under **Select a sample template**, from the drop\-down menu choose the **Enable AWS config** template\. Click **Next**\.  
![\[StackSets sample Enable AWS Config template\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-choose-template.png)

1. On the **Specify StackSet details** page, provide the following information\.

   1. Provide a name for the stack set\. Stack set names must begin with an alphabetical character, and contain only letters, numbers, and hyphens\. In this walkthrough, we use the name **my\-awsconfig\-stackset**\.

   1. You are prompted to specify values for parameters that are used by AWS Config\. For more information about these parameters, see [Setting up AWS Config with the Console](http://docs.aws.amazon.com/config/latest/developerguide/gs-console.html) in the *AWS Config Developer Guide*\. In this walkthrough, we will leave default settings for all AWS Config parameters\.

   1. You can configure Amazon Simple Notification Service \(SNS\) updates by email, based on log content, using the **TopicARN** and **NotificationEmail** parameters\. For the purposes of this walkthrough, we are not configuring Amazon SNS updates\.

   1. You can configure the delivery channel for updates and notifications using the **DeliveryChannelName** and **Frequency** parameters\. For more information about the delivery channel in AWS Config, see [Managing the Delivery Channel](http://docs.aws.amazon.com/config/latest/developerguide/manage-delivery-channel.html) in the *AWS Config Developer Guide*\. For the purposes of this walkthrough, we are leaving default settings in this area\.

1. When you are finished specifying parameters for AWS Config, choose **Next**\.

1. On the **Configure StackSet options** page, add a tag by specifying a key and value pair\. In this walkthrough, we create a tag called **Stage**, with a value of **Test**\. Tags that you apply to stack sets are applied to all resources that are created by your stacks\. For more information about how tags are used in AWS, see [Using Cost Allocation Tags](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\. 

   Leave **Permissions** unspecified, and choose **Next**\.  
![\[Tags page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-configure-options.png)

1. On the **Set deployment options** page, provide the accounts and regions into which you want stacks in your stack set deployed\. 

   AWS CloudFormation will deploy stacks in the specified accounts within the first region, then moves on to the next, and so on, as long as a region's deployment failures do not exceed a specified failure tolerance\.

   1. For **Accounts**, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\.

   1. For **Specify regions**, choose US East \(N\. Virginia\) Region\. Repeat for the US West \(Oregon\) Region\. Click the up arrow next to US West \(Oregon\) Region to move it to be the first entry in the list\. The order of the regions under **Specify regions** determines their deployment order\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.

        This means that AWS CloudFormation deploys your stack in only one account at one time\.
      + For **Failure tolerance**, keep the defauls of **Number** and **0**\.

        This means that a maximum of one stack deployment can fail in one of your specified regions before AWS CloudFormation stops deployment in the current region, and cancels deployment in remaining regions\.

      Choose **Next**\.  
![\[Set Deployment Options page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-set-depoy-options.png)

1. On the **Review** page, review your choices and your stack set's properties\. To make changes, choose **Edit** in the area in which you want to change properties\. Before you can create the stack set, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are creating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM Resources in AWS CloudFormation Templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready to create your stack set, choose **Submit**\.  
![\[Acknowledge required capabilities\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-review-capabilities.png)

1. AWS CloudFormation starts creating your stack set\. View the progress and status of the creation of the stacks in your stack set in the stack set details page that opens when you choose **Submit**\.  
![\[Operations tab of the StackSets details page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-detail-operations.png)

**To create a stack set by using the AWS CLI**

When you create stack sets by using AWS CLI commands, you run two separate commands: `create-stack-set` to upload your template and create the stack set container, and `create-stack-instances` to create the stacks within your stack set\. Start by running an AWS CLI command, `create-stack-set`, to upload the sample AWS CloudFormation template that enables AWS Config, and then start stack set creation\.

1. Open the AWS CLI\.

1. Run the following command\. For the `--template-url` parameter, provide the URL of the Amazon S3 bucket in which you are storing your template\. For this walkthrough, we use `my-awsconfig-stackset` as the value of the `--stack-set-name` parameter\.

   ```
   aws cloudformation create-stack-set --stack-set-name my-awsconfig-stackset --template-url https://s3.amazonaws.com/cloudformation-stackset-sample-templates-us-east-1/EnableAWSConfig.yml
   ```

1. After your `create-stack-set` command is finished, run the `list-stack-sets` command to see that your stack set has been created\. You should see your new stack set in the results\.

   ```
   aws cloudformation list-stack-sets
   ```

1. Run the `create-stack-instances` AWS CLI command to add stack instances to your stack set\. In this walkthrough, we use `us-west-2` and `us-east-1` as the values of the `--regions` parameter\.

   Set the failure tolerance and maximum concurrent accounts by setting `FailureToleranceCount` to `0` and `MaxConcurrentCount` to `1` in the `--operation-preferences` parameter, as shown in the following example\. To apply percentages instead, use `FailureTolerancePercentage` or `MaxConcurrentPercentage`\. For the purposes of this walkthrough, we are using count, not percentage\.

   ```
   aws cloudformation create-stack-instances --stack-set-name my-awsconfig-stackset --accounts '["account_ID_1","account_ID_2"]' --regions '["region_1","region_2"]' --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1
   ```
**Important**  
Wait until an operation is complete before starting another one\. You can run only one operation at a time\.

1. Verify that the stack instances were created successfully\. Run `DescribeStackSetOperation` with the `operation-id` that is returned as part of the output of step 4\.

   ```
   aws cloudformation describe-stack-set-operation --stack-set-name my-awsconfig-stackset --operation-id operation_ID
   ```