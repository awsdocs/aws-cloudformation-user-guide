# How does AWS CloudFormation work?<a name="cfn-whatis-howdoesitwork"></a>

When you create a stack, AWS CloudFormation makes underlying service calls to AWS to provision and configure your resources\. Note that AWS CloudFormation can perform only actions that you have permission to do\. For example, to create EC2 instances by using AWS CloudFormation, you need permissions to create instances\. You'll need similar permissions to terminate instances when you delete stacks with instances\. You use [AWS Identity and Access Management](https://docs.aws.amazon.com/IAM/latest/UserGuide/) \(IAM\) to manage permissions\.

The calls that AWS CloudFormation makes are all declared by your template\. For example, suppose you have a template that describes an EC2 instance with a `t1.micro` instance type\. When you use that template to create a stack, AWS CloudFormation calls the Amazon EC2 create instance API and specifies the instance type as `t1.micro`\. The following diagram summarizes the AWS CloudFormation workflow for creating stacks\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/create-stack-diagram.png)

1. You can design an AWS CloudFormation template \(a JSON or YAML\-formatted document\) in [AWS CloudFormation Designer](https://console.aws.amazon.com/cloudformation/designer) or write one in a text editor\. You can also choose to use a provided template\. The template describes the resources you want and their settings\. For example, suppose you want to create an EC2 instance\. Your template can declare an EC2 instance and describe its properties, as shown in the following example:  
**Example JSON syntax**  

   ```
   {
     "AWSTemplateFormatVersion" : "2010-09-09",
     "Description" : "A simple EC2 instance",
     "Resources" : {
       "MyEC2Instance" : {
         "Type" : "AWS::EC2::Instance",
         "Properties" : {
           "ImageId" : "ami-0ff8a91507f77f867",
           "InstanceType" : "t1.micro"
         }
       }
     }
   }
   ```  
**Example YAML syntax**  

   ```
   AWSTemplateFormatVersion: '2010-09-09'
   Description: A simple EC2 instance
   Resources:
     MyEC2Instance:
       Type: AWS::EC2::Instance
       Properties:
         ImageId: ami-0ff8a91507f77f867
         InstanceType: t1.micro
   ```

1. Save the template locally or in an S3 bucket\. If you created a template, save it with any file extension like `.json`, `.yaml`, or `.txt`\.

1. Create an AWS CloudFormation stack by specifying the location of your template file , such as a path on your local computer or an Amazon S3 URL\. If the template contains parameters, you can specify input values when you create the stack\. Parameters enable you to pass in values to your template so that you can customize your resources each time you create a stack\.

   You can create stacks by using the AWS CloudFormation [console](cfn-console-create-stack.md), [API](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html), or [AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)\.
**Note**  
If you specify a template file stored locally, AWS CloudFormation uploads it to an S3 bucket in your AWS account\. AWS CloudFormation creates a bucket for each region in which you upload a template file\. The buckets are accessible to anyone with Amazon Simple Storage Service \(Amazon S3\) permissions in your AWS account\. If a bucket created by AWS CloudFormation is already present, the template is added to that bucket\.  
You can use your own bucket and manage its permissions by manually uploading templates to Amazon S3\. Then whenever you create or update a stack, specify the Amazon S3 URL of a template file\.

AWS CloudFormation provisions and configures resources by making calls to the AWS services that are described in your template\.

After all the resources have been created, AWS CloudFormation reports that your stack has been created\. You can then start using the resources in your stack\. If stack creation fails, AWS CloudFormation rolls back your changes by deleting the resources that it created\.

## Updating a stack with change sets<a name="w7739ab1b5c17c17"></a>

When you need to update your stack's resources, you can modify the stack's template\. You don't need to create a new stack and delete the old one\. To update a stack, create a change set by submitting a modified version of the original stack template, different input parameter values, or both\. AWS CloudFormation compares the modified template with the original template and generates a change set\. The change set lists the proposed changes\. After reviewing the changes, you can execute the change set to update your stack or you can create a new change set\. The following diagram summarizes the workflow for updating a stack\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/update-stack-diagram.png)

**Important**  
Updates can cause interruptions\. Depending on the resource and properties that you are updating, an update might interrupt or even replace an existing resource\. For more information, see [AWS CloudFormation stack updates](using-cfn-updating-stacks.md)\.

1. You can modify an AWS CloudFormation stack template by using [AWS CloudFormation Designer](https://console.aws.amazon.com/cloudformation/designer) or a text editor\. For example, if you want to change the instance type for an EC2 instance, you would change the value of the `InstanceType` property in the original stack's template\.

   For more information, see [Modifying a stack template](using-cfn-updating-stacks-get-template.md)\.

1. Save the AWS CloudFormation template locally or in an S3 bucket\.

1. Create a change set by specifying the stack that you want to update and the location of the modified template, such as a path on your local computer or an Amazon S3 URL\. If the template contains parameters, you can specify values when you create the change set\.

   For more information about creating change sets, see [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md)\.
**Note**  
If you specify a template that is stored on your local computer, AWS CloudFormation automatically uploads your template to an S3 bucket in your AWS account\.

1. View the change set to check that AWS CloudFormation will perform the changes that you expect\. For example, check whether AWS CloudFormation will replace any critical stack resources\. You can create as many change sets as you need until you have included the changes that you want\.
**Important**  
Change sets don't indicate whether your stack update will be successful\. For example, a change set doesn't check if you will surpass an account [limit](cloudformation-limits.md), if you're updating a [resource](aws-template-resource-type-ref.md) that doesn't support updates, or if you have insufficient [permissions](using-iam-template.md) to modify a resource, all of which can cause a stack update to fail\.

1. Execute the change set that you want to apply to your stack\. AWS CloudFormation updates your stack by updating only the resources that you modified and signals that your stack has been successfully updated\. If the stack updates fails, AWS CloudFormation rolls back changes to restore the stack to the last known working state\.

## Deleting a stack<a name="w7739ab1b5c17c19"></a>

When you delete a stack, you specify the stack to delete, and AWS CloudFormation deletes the stack and all the resources in that stack\. You can delete stacks by using the AWS CloudFormation [console](cfn-console-delete-stack.md), [API](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeleteStack.html), or [AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/delete-stack.html)\.

If you want to delete a stack but want to retain some resources in that stack, you can use a [deletion policy](aws-attribute-deletionpolicy.md) to retain those resources\.

After all the resources have been deleted, AWS CloudFormation signals that your stack has been successfully deleted\. If AWS CloudFormation cannot delete a resource, the stack will not be deleted\. Any resources that haven't been deleted will remain until you can successfully delete the stack\.

## Additional resources<a name="w7739ab1b5c17c21"></a>
+ For more information about creating AWS CloudFormation templates, see [Template anatomy](template-anatomy.md)\.
+ For more information about creating, updating, or deleting stacks, see [Working with stacks](stacks.md)\.