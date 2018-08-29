# Using CloudFormer to Create AWS CloudFormation Templates from Existing AWS Resources<a name="cfn-using-cloudformer"></a>

CloudFormer is a template creation beta tool that creates an AWS CloudFormation template from existing AWS resources in your account\. You select any supported AWS resources that are running in your account, and CloudFormer creates a template in an Amazon S3 bucket\.

**Note**  
Use CloudFormer to produce templates that you can use as a starting point\. Not all AWS resources or resource properties are supported\. \.

The following list outlines the basic procedure for using CloudFormer:

1. Provision and configure the required resources using your existing processes and tools\.

1. Create and launch a CloudFormer stack\.

   CloudFormer is an AWS CloudFormation stack\. You run CloudFormer by launching the stack from your AWS environment\. It runs on a t2\.medium Amazon EC2 instance and requires no other resources\.

1. Use CloudFormer to create a template using your existing AWS resources and save the template to an Amazon S3 bucket\.

1. Delete the CloudFormer stack\. 

   You usually don't need CloudFormer beyond this point, so you can avoid additional charges by deleting the stack\.

1. Use the template to launch a new stack, as needed\.

The following topics describes how to use CloudFormer by walking you through a basic scenario \(a simple website on an Amazon EC2 instance\) that creates a template with multiple resources\. However, this example is just one of many possible scenarios; CloudFormer can create a template from any collection of supported AWS resources\.

## Step 1: Create a CloudFormer Stack<a name="launch-cloudformer"></a>

CloudFormer is itself an AWS CloudFormation stack, so the first step is to create and launch the stack from the AWS CloudFormation [console](https://console.aws.amazon.com/cloudformation)\.

**To create a CloudFormer stack using the AWS CloudFormation Console**

1.  Log in to the AWS CloudFormation console and click **Create New Stack** to launch the stack creation wizard\. For instructions on how to log in, see [Logging in to the AWS CloudFormation Console](cfn-console-login.html)\. 

1. In the **Choose a template** section, select **Select a sample template** and then select **CloudFormer** from the drop\-down list\.

1. Click **Next** to specify the stack name and input parameters\.

1. Specify a name for the CloudFormer stack in the **Name** field\.

1. In the **Parameters** section, type a password and user name that you'll use to log in to CloudFormer, and then click **Next**\.
**Important**  
You can't use special characters for the password \(such as `; & ! " £ $ % ^ ( ) / \`\) or leave the password blank\.

1. Click **Next**\.

   For CloudFormer, you don't need to specify any additional options\.

1. Review the information about the stack and select **I acknowledge that this template may create IAM resources**\.

1. After you finish reviewing the stack information, click **Create** to start creating the CloudFormer stack\.

   CloudFormer is an AWS CloudFormation stack, so it must go through the normal stack creation process, which can take a few minutes\.

## Step 2: Launch the CloudFormer Stack<a name="launch-cloudformer-stack"></a>

After the CloudFormer stack's status is **CREATE\_COMPLETE**, you can launch the stack\.

**To launch the CloudFormer stack**

1. Click the CloudFormer stack's entry in the AWS CloudFormation Console, and select the **Outputs** tab in the stack information pane\. 

1. In the **Value** column, click the URL to launch the CloudFormer tool\.

1. Type the user name and password that you specified when you created the CloudFormer stack\.

When you log in to CloudFormer, it displays the first page of the tool in your browser, where you can start to create your template, as described in the next section\.

![\[The CloudFormer tool\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformer-welcome-screen.png)

**Note**  
The CloudFormer stack launches a t2\.medium Amazon EC2 instance\. You'll delete this stack at the end of the walkthrough after the template is created\.

After you create a CloudFormer stack, it is added to the collection of stacks in your account\. To create another template, just launch the CloudFormer stack again\.

## Step 3: Use CloudFormer to Create a Template<a name="cfn-using-cloudformer-create-template"></a>

Before you start using CloudFormer to create a template, first ensure that your account has all the AWS resources that you want to include in your template\. This walkthrough assumes that your account has: 
+ An Amazon EC2 instance \(`AWS::EC2::Instance`\)\. 
+ An Amazon EC2 security group \(`AWS::EC2::SecurityGroup`\)\. You should associate the security group with the instance\. 
+ An Elastic IP Address \(`AWS::EC2::EIP`\)\. You should associate the address with the instance\. 

**To use CloudFormer to create a template from your AWS resources**

1. Under **Select the AWS Region**, select the template's region from the list, and click **Create Template**\. The tool must first analyze your account, so it might take a few minutes before the **Intro** page is displayed\.

1.  On the **Intro** page, enter a description for your template\.

   Note that you can use this page to select resources with a filter or select all resources in your account\. However, this walkthrough specifies resources manually, so leave the **Resource Name Filter** field blank, clear the **Select all resources in your account** checkbox, and then click **Continue**\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformer-intro.png)

1. The following pages are for resources that are not used by this walkthrough, so just examine the page for future reference and click **Continue**\. In order:

   1. **DNS Names** allows you to include Route 53 records\. 

   1. The **Virtual Private Clouds** allows you to include Amazon VPCs\.

   1. **Virtual Private Cloud Network Topologies** allows you to include Amazon VPC subnets, gateways, DHCP configurations, and VPN connections\.

   1. **Virtual Private Cloud Security Configuration** allows you to include network ACLS and route tables\.

1. **Network Resources** allows you to include Elastic Load Balancing load balancers, Elastic IP Addresses, CloudFront distributions, and Amazon EC2 network interfaces\. Select the Elastic IP address you want to include in the template and click **Continue**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformer-eip.png)

1.  The **Compute Resources** page allows you to include Auto Scaling groups and Amazon EC2 instances\. Before you started creating the template, you associated an Elastic IP Address with your Amazon EC2 instance, creating a dependent resource\. When you reach **Compute Resources**, CloudFormer automatically selects dependent instances, so just ensure that your instance is selected and click **Continue**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformer-ec2.png)
**Note**  
You can manually include additional instances, as needed\. If you don't want to include an automatically selected instance, just clear the check box\.

1. The following pages are for resources that are not used by this walkthrough, so just examine the page for future reference and click **Continue**\. In order:

   1. **Storage** allows you to include Amazon EBS volumes, Amazon RDS instances, DynamoDB tables, and Amazon S3 buckets\. 

   1. **Application Services** allows you to include ElastiCache clusters, Amazon SQS queues, Amazon SimpleDB domains, and Amazon SNS topics\.

      **System Configuration** allows you to include Auto Scaling launch configurations, Amazon RDS subnet groups, ElastiCache parameter groups, and Amazon RDS parameter groups\.

1. The **Security Groups** page allows you include security groups\. Before you started creating the template, you associated an Amazon EC2 security group with your Amazon EC2 instance, creating a dependent resource\. When you reach **Security Groups**, CloudFormer automatically selects dependent security groups, so just ensure that your group is selected and click **Continue**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformer-sg.png)
**Note**  
You can manually include additional security groups—including Amazon EC2 security groups, Amazon RDS security groups, and so on—as appropriate\. If you don't want to include an automatically selected security group, just clear the check box\.

1. The **Operational Resources** page allows you to include Auto Scaling policies and CloudWatch alarms\. This walkthrough uses neither, so just click **Continue**\. 

1.  The **Summary** page serves several purposes: 
   + It allows you to review the resources you've added to your template\.

     To modify your resources, click **Back** to return to the appropriate pages and modify your selections as needed\. 
   + It allows you to change the auto\-generated logical names that were assigned to your resources\.

     To modify a logical name, click **Modify** and enter the name in the **Logical Name** field\.
   +  It allows you to specify outputs that provide necessary information, such as your site's IP address or URL\. 

     To modify an output, click **Modify** and select the appropriate output from the list\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformer-summary.png)

   Examine the resources you've selected and make any necessary changes\. You should have one Elastic IP Address, one Amazon EC2 instance, and one Amazon EC2 security group\. When you are satisfied, click **Continue** to generate the template\.

1.  The **AWS CloudFormation Template** page displays the generated template\. You can use the template to deploy your resources as a combined set with AWS CloudFormation, or as a base template for further modification\. 
**Note**  
In addition to the resources that you explicitly specified, the template includes values that are associated with those resources such as Amazon EC2 instances' Availability Zones\.

   Select an Amazon S3 bucket from the **S3 Bucket** list and click **Save Template** to save the template to the bucket and add it to the collection of stacks in your account\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformer-template.png)

   **Save Template** gives you two options:
   + **Launch Stack** saves the template to the specified Amazon S3 bucket and also launches the stack immediately\.
   + **Create Template** simply saves the template to the specified Amazon S3 bucket\.

     You can launch the stack later just like you would with any other template, for example, by using the AWS CloudFormation console\.

## Step 4: Delete the CloudFormer Stack<a name="cfn-using-cloudformer-delete-stack"></a>

Now that you have the template, you don't need the CloudFormer stack any more\. To avoid unnecessary charges to your account, select the stack in the AWS CloudFormation console and then choose **Actions** > **Delete Stack**\.