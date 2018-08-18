# Creating Stacks Using Change Sets<a name="cfn-console-create-stacks-changesets"></a>

To preview how a AWS CloudFormation stack will be configured before creating the stack, create a change set\. This functionality allows you to examine various configurations and make corrections and changes to your stack before executing the change set\.

## Creating a Change Set for a New Stack<a name="cfn-console-create-stacks-changesets-create-new-stack"></a>

To create a change set for a new stack, submit the configuration that you want to use by providing a template, input parameter values, or both\.

**To create a change set \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), choose **Create Stack**, and then choose **Create Change Set for New Stack**\.  
![\[The Create Change Set for New Stack option in the Create Stack menu.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cfn-console-create-changeset-for-new-stack.png)

1. On the **Select Template** page, specify the location of your template\.
   + For a template stored locally, choose **Upload a template to Amazon S3**\. **Choose File** to navigate to the file, choose the file, and then choose **Next**\.
   + For a template stored in an Amazon S3 bucket, choose **Specify an Amazon S3 URL**\. Type or paste the URL for the template, and then choose **Next**\.

     If your template is stored in a versioning\-enabled bucket, you can specify a specific version, for example: `https://s3.amazonaws.com/templates/myTemplate.template?versionId=123ab1cdeKdOW5IH4GAcYbEngcpTJTDW`

     For more information, see [Managing Objects in a Versioning\-Enabled Bucket](http://docs.aws.amazon.com/AmazonS3/latest/user-guide/managing-objects-versioned-bucket.html) in the *Amazon Simple Storage Service Console User Guide*\.

1. On the **Specify Details** page, configure the following items:
   + Type the **Stack name**\.
   + \(Optional\) To identify your change set, type its **Name** and **Description**\.
   + If your template contains parameters, type the parameter values in the **Parameters** section\.

   When you finish, choose **Next**\.

1. \(Optional\) On the **Options** page, update the stack's service role, the stack tags, and the stack's Amazon SNS notification topic, and then choose **Next**\.

1. On the **Review** page, review the proposed configuration\.

   If the template includes AWS Identity and Access Management \(IAM\) resources, select **I acknowledge that this template may create IAM resources** to acknowledge that AWS CloudFormation might create IAM resources if you execute this change set\. IAM resources can modify permissions in your AWS account\. Review these resources to ensure that you allow the correction actions\. For more information, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.

   When you finish, choose **Create change set**\.

   While AWS CloudFormation begins to create the change set, the status of the change set is **CREATE\_IN\_PROGRESS**\. When AWS CloudFormation completes the creation progress, it sets its status to **CREATE\_COMPLETE**\. In the **Changes** section, AWS CloudFormation lists the proposed configuration of your stack\.  
![\[Preview of the change set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cfn-console-create-changeset-for-new-stack-preview.png)

   If AWS CloudFormation fails to create the change set and reports the **CREATE\_FAILED** status, fix the error displayed in the **Status** field, and then create a new change set\. At this stage, you can try various configurations and make corrections and changes to your stack before executing the next change set\.

1. To create a new stack using the change set, choose **Execute**, and then choose **Execute** again\.

   When you create a change set, AWS CloudFormation launches a stack and reports the **REVIEW\_IN\_PROGRESS** status until you execute the change set\.