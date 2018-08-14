# Updating Stacks Directly<a name="using-cfn-updating-stacks-direct"></a>

When you want to quickly deploy updates to your stack, perform a direct update\. With a direct update, you submit a template or input parameters that specify updates to the resources in the stack, and AWS CloudFormation immediately deploys them\. If you want to use a template to make your updates, you can modify the current template and store it locally or in an S3 bucket\.

For resource properties that don't support updates, you must keep the current values\. To preview the changes that AWS CloudFormation will make to your stack before you update it, use change sets\. For more information, see [Updating Stacks Using Change Sets](using-cfn-updating-stacks-changesets.md)\.

**Note**  
When updating a stack, AWS CloudFormation might interrupt resources or replace updated resources, depending on which properties you update\. For more information about resource update behaviors, see [Update Behaviors of Stack Resources](using-cfn-updating-stacks-update-behaviors.md)\.

**To update a AWS CloudFormation stack \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), from the list of stacks, select the running stack that you want to update\.

1. Choose **Actions** and then **Update Stack**\.  
![\[The Update Stack option in the Actions menu.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cfn-update-stack-initiating.png)

1. If you modified the stack template, specify the location of the updated template\. If not, select **Use current template**\.
   + For a template stored locally on your computer, select **Upload a template to Amazon S3**\. Choose **Choose File** to navigate to the file and select it, and then click **Next**\.
**Note**  
If you upload a local template file, AWS CloudFormation uploads it to an Amazon Simple Storage Service \(Amazon S3\) bucket in your AWS account\. If you don't already have an S3 bucket that was created by AWS CloudFormation, it creates a unique bucket for each Region in which you upload a template file\. If you already have an S3 bucket that was created by AWS CloudFormation in your AWS account, AWS CloudFormation adds the template to that bucket\.  
Considerations to keep in mind about S3 buckets created by AWS CloudFormation  
The buckets are accessible to anyone with Amazon S3 permissions in your AWS account\.
AWS CloudFormation creates the buckets with server\-side encryption enabled by default, thereby encrypting all objects stored in the bucket\.   
You can directly manage encryption options for buckets that AWS CloudFormation has created; for example, using the Amazon S3 console at [https://console\.aws\.amazon\.com/s3/](https://console.aws.amazon.com/s3/) , or the AWS CLI\. For more information, see [Amazon S3 Default Encryption for S3 Buckets](http://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html) in the *[Amazon Simple Storage Service Developer Guide](http://docs.aws.amazon.com/AmazonS3/latest/dev/)*\.
You can use your own bucket and manage its permissions by manually uploading templates to Amazon S3\. When you create or update a stack, specify the Amazon S3 URL of a template file\.
   + For a template stored in an Amazon S3 bucket, select **Specify an Amazon S3 URL**\. Enter or paste the URL for the template, and then click **Next**\.

     If you have a template in a versioning\-enabled bucket, you can specify a specific version of the template, such as `https://s3.amazonaws.com/templates/myTemplate.template?versionId=123ab1cdeKdOW5IH4GAcYbEngcpTJTDW`\. For more information, see [Managing Objects in a Versioning\-Enabled Bucket](http://docs.aws.amazon.com/AmazonS3/latest/user-guide/managing-objects-versioned-bucket.html) in the *Amazon Simple Storage Service Console User Guide*\.

1. If your template contains parameters, on the **Specify Parameters** page, enter or modify the parameter values, and then click **Next**\.

   AWS CloudFormation populates each parameter with the value that is currently set in the stack with the exception of parameters declared with the `NoEcho` attribute; however, you can still use current values by choosing **Use existing value**\.

1. On the **Options** page, you can update the stack's service role, enter an overriding stack policy, or update the Amazon SNS notification topic\. An overriding stack policy lets you update protected resources\. For more information, see [Prevent Updates to Stack Resources](protect-stack-resources.md)\.

   Click **Next**\.

1. Review the stack information and the changes that you submitted\.

   In the **Review** section, check that you submitted the correct information, such as the correct parameter values or template URL\. If your template contains IAM resources, select **I acknowledge that this template may create IAM resources** to specify that you want to use IAM resources in the template\. For more information about using IAM resources in templates, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.

   In the **Preview your changes** section, check that AWS CloudFormation will make all the changes that you expect\. For example, you can check that AWS CloudFormation adds, removes, and modifies the resources that you intended to add, remove, or modify\. AWS CloudFormation generates this preview by creating a change set for the stack\. For more information, see [Updating Stacks Using Change Sets](using-cfn-updating-stacks-changesets.md)\.

1. Click **Update**\.

   Your stack enters the **UPDATE\_IN\_PROGRESS** state\. After it has finished updating, the state is set to **UPDATE\_COMPLETE**\.

   If the stack update fails, AWS CloudFormation automatically rolls back changes, and sets the state to **UPDATE\_ROLLBACK\_COMPLETE**\.
**Note**  
You can cancel an update while it's in the **UPDATE\_IN\_PROGRESS** state\. For more information, see [Canceling a Stack Update](using-cfn--stack-update-cancel.md)\.

**To update a AWS CloudFormation stack \(AWS CLI\)**
+ Use the [http://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html) command to directly update a stack\. You specify the stack, and parameter values and capabilities that you want to update, and, if you want use an updated template, the name of the template\.

  The following example updates the template and input parameters for the `mystack` stack:

  ```
  PROMPT> aws cloudformation update-stack --stack-name mystack --template-url https://s3.amazonaws.com/sample/updated.template
  --parameters ParameterKey=VPCID,ParameterValue=SampleVPCID ParameterKey=SubnetIDs,ParameterValue=SampleSubnetID1\\,SampleSubnetID2
  ```

  The following example updates just the `SubnetIDs` parameter values for the `mystack` stack:

  ```
  PROMPT> aws cloudformation update-stack --stack-name mystack --use-previous-template
  --parameters ParameterKey=VPCID,UsePreviousValue=true ParameterKey=SubnetIDs,ParameterValue=SampleSubnetID1\\,UpdatedSampleSubnetID2
  ```

  The following example adds two stack notification topics to the `mystack` stack:

  ```
  PROMPT> aws cloudformation update-stack --stack-name mystack --use-previous-template
  --notification-arns "arn:aws:sns:us-east-1:12345678912:mytopic" "arn:aws:sns:us-east-1:12345678912:mytopic2"
  ```

  The following example removes all stack notification topics from the `mystack` stack:

  ```
  PROMPT> aws cloudformation update-stack --stack-name mystack --use-previous-template
  --notification-arns []
  ```