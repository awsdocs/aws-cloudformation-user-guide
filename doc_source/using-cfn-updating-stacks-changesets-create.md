# Creating a Change Set<a name="using-cfn-updating-stacks-changesets-create"></a>

To create a change set for a running stack, submit the changes that you want to make by providing a modified template, new input parameter values, or both\. AWS CloudFormation generates a change set by comparing your stack with the changes you submitted\.

To modify a template, for example to add a new resource to your stack, modify a copy of the current template before creating the change set\. For more information, see [Modifying a Stack Template](using-cfn-updating-stacks-get-template.md)\.

**To create a change set \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), from the list of stacks, select the running stack for which you want to create a change set\.

1. Choose **Actions**, and then choose **Create Change Set**\.  
![\[The Create Change Set For Current Stack option in the Actions menu.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-changeset-create.png)

1. If you modified the stack template, specify the location of the updated template\. If not, select **Use current template**\.
   + For a template stored locally on your computer, select **Upload a template to Amazon S3**\. Choose **Choose File** to navigate to the file and select it, and then click **Next**\.
   + For a template stored in an Amazon S3 bucket, select **Specify an Amazon S3 URL**\. Enter or paste the URL for the template, and then click **Next**\.

     If you have a template in a versioning\-enabled bucket, you can specify a specific version of the template, such as `https://s3.amazonaws.com/templates/myTemplate.template?versionId=123ab1cdeKdOW5IH4GAcYbEngcpTJTDW`\. For more information, see [Managing Objects in a Versioning\-Enabled Bucket](http://docs.aws.amazon.com/AmazonS3/latest/user-guide/managing-objects-versioned-bucket.html) in the *Amazon Simple Storage Service Console User Guide*\.

1. On the **Specify Details** page, type information about the change set and, if necessary, modify the parameter values that you want to change, and then choose **Next**\.

   In the **Specify Details** section, specify a name for the change set\. You can also specify a description of the change set to identify its purpose\.

   If your template contains parameters, in the **Parameters** section, change applicable parameter values\. If you're reusing the stack's template, AWS CloudFormation populates each parameter with the current value in the stack,with the exception of parameters declared with the `NoEcho` attribute\. To use existing values for those parameters, select **Use existing value**\.

1. On the **Options** page, you can update the stack's service role, the stack tags, or the stack's Amazon SNS notification topic, as applicable, and then choose **Next**\.

1. Review the changes for this change set\.

   If the template includes AWS Identity and Access Management \(IAM\) resources, select **I acknowledge that this template may create IAM resources** to acknowledge that AWS CloudFormation might create IAM resources if you execute this change set\. IAM resources can modify permissions in your AWS account; review these resources to ensure that you're permitting only the actions that you intend\. For more information, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.

1. Choose **Create change set**\.

   You're redirected to the change set's detail page\. While AWS CloudFormation generates the change set, the status of the change set is **CREATE\_IN\_PROGRESS**\. After it has created the change set, AWS CloudFormation sets the status to **CREATE\_COMPLETE**\. In the **Changes** section, AWS CloudFormation lists all of the changes that it will make to your stack\. For more information, see [Viewing a Change Set](using-cfn-updating-stacks-changesets-view.md)\.  
![\[The details page for the change set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-changeset-details.png)

   If AWS CloudFormation fails to create the change set \(reports `FAILED` status\), fix the error displayed in the **Status** field, and recreate the change set\.

**To create a change set \(AWS CLI\)**
+ Run the [aws cloudformation create\-change\-set](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-change-set.html) command\.

  You submit your changes as command options\. You can specify new parameter values, a modified template, or both\. For example, the following command creates a change set named `SampleChangeSet` for the `SampleStack` stack\. The change set uses the current stack's template, but with a different value for the `Purpose` parameter:

  ```
  aws cloudformation create-change-set --stack-name arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000
  --change-set-name SampleChangeSet --use-previous-template --parameters ParameterKey="InstanceType",UsePreviousValue=true ParameterKey="KeyPairName",UsePreviousValue=true ParameterKey="Purpose",ParameterValue="production"
  ```