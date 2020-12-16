# Walkthrough: Refer to resource outputs in another AWS CloudFormation stack<a name="walkthrough-crossstackref"></a>

To export resources from one AWS CloudFormation stack to another, create a cross\-stack reference\. Cross\-stack references let you use a layered or service\-oriented architecture\. Instead of including all resources in a single stack, you create related AWS resources in separate stacks; then you can refer to required resource outputs from other stacks\. By restricting cross\-stack references to outputs, you control the parts of a stack that are referenced by other stacks\.

For example, you might have a network stack with a VPC, a security group, and a subnet for public web applications, and a separate public web application stack\. To ensure that the web applications use the security group and subnet from the network stack, you create a cross\-stack reference that allows the web application stack to reference resource outputs from the network stack\. With a cross\-stack reference, owners of the web application stacks don't need to create or maintain networking rules or assets\.

To create a cross\-stack reference, use the `Export` output field to flag the value of a resource output for export\. Then, use the `Fn::ImportValue` intrinsic function to import the value\. For more information, see [Outputs](outputs-section-structure.md) and [`Fn::ImportValue`](intrinsic-function-reference-importvalue.md)\.

Prerequisites

Before you begin this walkthrough, check that you have [AWS Identity and Access Management \(IAM\) permissions](https://aws.amazon.com/iam/) to use all of the following services: Amazon VPC, Amazon EC2, and AWS CloudFormation\.

**Note**  
AWS CloudFormation is a free service\. However, you are charged for the AWS resources that you include in your stacks at the current rate for each one\. For more information about AWS pricing, see [the detail page for each product](http://aws.amazon.com)\.  
The following restrictions apply to cross\-stack references:  
For each AWS account, `Export` names must be unique within a region\.
You can't create cross\-stack references across regions\. You can use the intrinsic function `Fn::ImportValue` to import only values that have been exported within the same region\.
For outputs, the value of the `Name` property of an `Export` can't use `Ref` or `GetAtt` functions that depend on a resource\.  
Similarly, the `ImportValue` function can't include `Ref` or `GetAtt` functions that depend on a resource\.
You can't delete a stack if another stack references one of its outputs\.
You can't modify or remove an output value that is referenced by another stack\.

## Step 1: Use a sample template to create a network stack<a name="walkthrough-crossstackref-create-vpc-stack"></a>

The network stack contains the VPC, security group, and subnet that you will use in the web application stack\. In addition to these resources, the network stack creates an Internet gateway and routing tables to enable public access\.

**Note**  
You must create this stack before you create the web application stack\. If you create the web application stack first, it won't have a security group or subnet\.

**To create the network stack**

1. Open the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/) and choose **Create stack**\.

1. Choose **Template is ready**, and in the **Specify template** section choose **Amazon S3 URL**\. Copy and paste the following URL into the text box: `[https://s3\.amazonaws\.com/cloudformation\-examples/user\-guide/cross\-stack/SampleNetworkCrossStack\.template](https://s3.amazonaws.com/cloudformation-examples/user-guide/cross-stack/SampleNetworkCrossStack.template) ` 

   The link provides the location of the network stack template\. To see the resources that the stack will create, choose the link, which opens the template\. In the outputs section, you can see the networking resources that the sample template exports\. The names of the exported resources are prefixed with the stack's name in case you export networking resources from other stacks\. When users import networking resources, they can specify from which stack the resources are imported\.

1. After reviewing the template, choose **Next**\.

1. For **Stack name**, type **SampleNetworkCrossStack**, and then choose **Next**\.
**Note**  
Record the name of this stack\. You'll need the stack name when you launch the web application stack\.

1. Choose **Next**\. For this walkthrough, you don't need to add tags or specify advanced settings\.

1. Ensure that the stack name and template URL are correct, and then choose **Create stack**\.

   It might take several minutes for AWS CloudFormation to create your stack\. Wait until all resources have been successfully created before proceeding to create the web application stack\.

1. To monitor progress, view the stack events\. For more information, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\.

## Step 2: Use a sample template to create a web application stack<a name="walkthrough-crossstackref-create-ec2-stack"></a>

The web application stack creates an EC2 instance that uses the security group and subnet from the network stack\.

**Note**  
You must create this stack in the same region as the network stack\.

**To create the web application stack**

1. Open the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/), and choose **Create stack**\.

1. Choose **Template is ready**, and in the **Specify template** section choose **Amazon S3 URL**\. Copy and paste the following URL into the text box: [https://s3\.amazonaws\.com/cloudformation\-examples/user\-guide/cross\-stack/SampleWebAppCrossStack\.template](https://s3.amazonaws.com/cloudformation-examples/user-guide/cross-stack/SampleWebAppCrossStack.template) 

   The link provides the location of the web application template\. To see the resources that the stack will create, choose the link, which will open the template\. In the resources section, view the EC2 instance's properties\. You can see how the networking resources are imported from another stack by using the `Fn::ImportValue` function\.

1. After reviewing the template, choose **Next**\.

1. For **Stack name**, type **SampleWebAppCrossStack**\. In the **Parameters** section, use the default value for the **NetworkStackName** parameter, and then choose **Next**\.

   The sample template uses the parameter value to specify from which stack to import values\.

1. Choose **Next**\. For this walkthrough, you don't need to add tags or specify advanced settings\.

1. Ensure that the stack name and template URL are correct, and then choose **Create stack**\.

   It might take several minutes for AWS CloudFormation to create your stack\.

1. After the stack has been created, view its resources and note the instance ID\. For more information on viewing stack resources, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\.

   To verify the instance's security group and subnet, view the instance's properties in the [Amazon EC2 console](https://console.aws.amazon.com/ec2/)\. If the instance uses the security group and subnet from the `SampleNetworkCrossStack` stack, you have successfully created a cross\-stack reference\.

   Use the console to view the stack outputs and the example website URL to verify that the web application is running\. For more information, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\.

## Step 3: Clean up your resources<a name="walkthrough-crossstackref-clean-up"></a>

To ensure that you are not charged for unwanted services, delete the stacks\.

**To delete the stacks**

1. In the AWS CloudFormation console, choose the SampleWebAppCrossStack stack\.

1. Choose **Actions**, and then choose **Delete stack**\.

1. In the confirmation message, choose **Delete**\.

1. After the stack has been deleted, repeat the same steps for the SampleNetworkCrossStack stack\.
**Note**  
Wait until AWS CloudFormation completely deletes the SampleWebAppCrossStack stack\. If the EC2 instance is still running in the VPC, AWS CloudFormation won't delete the VPC in the SampleNetworkCrossStack stack\.

   All of the resources that you have previously created are deleted\.

Use the sample templates from this walkthrough to build your own cross\-referenced stacks\.