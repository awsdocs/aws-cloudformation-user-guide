# Create a New Stack Set<a name="stacksets-getting-started-create"></a>

You can create a stack set in either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\.

**To create a stack set by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. At the top of the page, choose **StackSets**, and then choose **Create stack set**\.  
![\[StackSets home page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_home.png)

1. On the **Select template** page of the **Create stack set** wizard, choose **Select a sample template from the following templates**\.  
![\[StackSets Select Template wizard page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/create_stack_set_selecttemplate.png)

1. Choose the **Enable AWS Config** sample template, and then choose **Next**\.  
![\[StackSets sample Enable AWS Config template\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/create_stack_set_cloudtrail.png)

1. On the **Specify details** page of the wizard, provide the following information\.

   1. Provide a name for the stack set\. Stack set names must begin with an alphabetical character, and contain only letters, numbers, and hyphens\. In this walkthrough, we use the name **my\-awsconfig\-stackset**\.  
![\[Specify Details page, first section\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_specify_details1.png)

   1. You are prompted to specify values for parameters that are used by AWS Config\. For more information about these parameters, see [Setting up AWS Config with the Console](http://docs.aws.amazon.com/config/latest/developerguide/gs-console.html) in the *AWS Config Developer Guide*\. In this walkthrough, we will leave default settings for all AWS Config parameters\.

1. In the **Delivery Channel Configuration** area, you can configure the delivery channel for updates and notifications\. For more information about the delivery channel in AWS Config, see [Managing the Delivery Channel](http://docs.aws.amazon.com/config/latest/developerguide/manage-delivery-channel.html) in the *AWS Config Developer Guide*\. For the purposes of this walkthrough, we are leaving default settings in this area\.

1. In the **Delivery Notifications** area, you can configure Amazon Simple Notification Service \(SNS\) updates by email, based on log content\. For the purposes of this walkthrough, we are not configuring Amazon SNS updates\.

1. When you are finished specifying parameters for AWS Config, choose **Next**\.

1. On the **Set deployment options** page, provide the accounts and regions into which you want stacks in your stack set deployed\. AWS CloudFormation deploys stacks in the specified accounts within the first region, then moves on to the next, and so on, as long as a region's deployment failures do not exceed a specified failure tolerance\.  
![\[Set Deployment Options page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_setdepoptions.png)

   1. In the **Accounts** area, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\.

   1. In the **Regions** area, choose US West \(Oregon\) Region and then choose **Add**\. Repeat for the US East \(N\. Virginia\) Region\. US West \(Oregon\) Region should be first in the **Deployment order** box\.

   1. In the **Preferences** area, keep the default value of **1** and **By number** for **Maximum concurrent accounts**\. This means that AWS CloudFormation deploys your stack in only one account at one time\. Keep **Failure tolerance** at the default value of **0**, and keep the **By number** default option\. This means that a maximum of one stack deployment can fail in one of your specified regions before AWS CloudFormation stops deployment in the current region, and cancels deployment in remaining regions\. Choose **Next**\.

1. On the **Tags** page, add a tag by specifying a key and value pair\. In this walkthrough, we create a tag called **Stage**, with a value of **Test**\. Tags that you apply to stack sets are applied to all resources that are created by your stacks\. For more information about how tags are used in AWS, see [Using Cost Allocation Tags](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\. After you specify the key\-value pair, choose **\+** to save the tag\. Choose **Next**\.  
![\[Tags page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_create_tags.png)

1. On the **Review** page, review your choices and your stack set's properties\. To make changes, choose **Edit** in the area in which you want to change properties\. Before you can create the stack set, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are creating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM Resources in AWS CloudFormation Templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready to create your stack set, choose **Create**\.  
![\[Acknowledge required capabilities\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_create_capabilities.png)

1. AWS CloudFormation starts creating your stack set\. View the progress and status of the creation of the stacks in your stack set in the Properties page that opens when you choose **Create**\.

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