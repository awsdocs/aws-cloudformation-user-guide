# AWS CloudFormation best practices<a name="best-practices"></a>

Best practices are recommendations that can help you use AWS CloudFormation more effectively and securely throughout its entire workflow\. Learn how to plan and organize your stacks, create templates that describe your resources and the software applications that run on them, and manage your stacks and their resources\. The following best practices are based on real\-world experience from current AWS CloudFormation customers\.

**Planning and organizing**  
+ [Organize your stacks by lifecycle and ownership](#organizingstacks)
+ [Use cross\-stack references to export shared resources](#cross-stack)
+ [Use IAM to control access](security-best-practices.md#use-iam-to-control-access)
+ [Reuse templates to replicate stacks in multiple environments](#reuse)
+ [Verify quotas for all resource types](#limits) 
+ [Use nested stacks to reuse common template patterns](#nested)

**Creating templates**  
+ [Do not embed credentials in your templates](security-best-practices.md#creds)
+ [Use AWS\-specific parameter types](#parmtypes)
+ [Use parameter constraints](#parmconstraints)
+ [Use AWS::CloudFormation::Init to deploy software applications on Amazon EC2 instances](#cfninit)
+ [Use the latest helper scripts](#helper-scripts)
+ [Validate templates before using them](#validate)

**Managing stacks**  
+ [Manage all stack resources through AWS CloudFormation](#donttouch)
+ [Create change sets before updating your stacks](#cfn-best-practices-changesets)
+ [Use stack policies](#stackpolicy)
+ [Use AWS CloudTrail to log AWS CloudFormation calls](security-best-practices.md#cloudtrail)
+ [Use code reviews and revision controls to manage your templates](#code)
+ [Update your Amazon EC2 Linux instances regularly](#update-ec2-linux)

## Organize your stacks by lifecycle and ownership<a name="organizingstacks"></a>

Use the lifecycle and ownership of your AWS resources to help you decide what resources should go in each stack\. Initially, you might put all your resources in one stack, but as your stack grows in scale and broadens in scope, managing a single stack can be cumbersome and time consuming\. By grouping resources with common lifecycles and ownership, owners can make changes to their set of resources by using their own process and schedule without affecting other resources\.

For example, imagine a team of developers and engineers who own a website that is hosted on autoscaling instances behind a load balancer\. Because the website has its own lifecycle and is maintained by the website team, you can create a stack for the website and its resources\. Now imagine that the website also uses back\-end databases, where the databases are in a separate stack that are owned and maintained by database administrators\. Whenever the website team or database team needs to update their resources, they can do so without affecting each other's stack\. If all resources were in a single stack, coordinating and communicating updates can be difficult\.

For additional guidance about organizing your stacks, you can use two common frameworks: a multi\-layered architecture and service\-oriented architecture \(SOA\)\.

A layered architecture organizes stacks into multiple horizontal layers that build on top of one another, where each layer has a dependency on the layer directly below it\. You can have one or more stacks in each layer, but within each layer, your stacks should have AWS resources with similar lifecycles and ownership\.

With a service\-oriented architecture, you can organize big business problems into manageable parts\. Each of these parts is a service that has a clearly defined purpose and represents a self\-contained unit of functionality\. You can map these services to a stack, where each stack has its own lifecycle and owners\. All of these services \(stacks\) can be wired together so that they can interact with one another\.

## Use cross\-stack references to export shared resources<a name="cross-stack"></a>

When you organize your AWS resources based on lifecycle and ownership, you might want to build a stack that uses resources that are in another stack\. You can hard\-code values or use input parameters to pass resource names and IDs\. However, these methods can make templates difficult to reuse or can increase the overhead to get a stack running\. Instead, use cross\-stack references to export resources from a stack so that other stacks can use them\. Stacks can use the exported resources by calling them using the `Fn::ImportValue` function\.

For example, you might have a network stack that includes a VPC, a security group, and a subnet\. You want all public web applications to use these resources\. By exporting the resources, you allow all stacks with public web applications to use them\. For more information, see [Walkthrough: Refer to resource outputs in another AWS CloudFormation stack](walkthrough-crossstackref.md)\.

## Verify quotas for all resource types<a name="limits"></a>

Before launching a stack, ensure that you can create all the resources that you want without hitting your AWS account limits\. If you hit a limit, AWS CloudFormation won't create your stack successfully until you increase your quota or delete extra resources\. Each service can have various limits that you should be aware of before launching a stack\. For example, by default, you can only launch 200 AWS CloudFormation stacks per region in your AWS account\. For more information about limits and how to increase the default limits, see [AWS service limits](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) in the *AWS General Reference*\.

## Reuse templates to replicate stacks in multiple environments<a name="reuse"></a>

After you have your stacks and resources set up, you can reuse your templates to replicate your infrastructure in multiple environments\. For example, you can create environments for development, testing, and production so that you can test changes before implementing them into production\. To make templates reusable, use the parameters, mappings, and conditions sections so that you can customize your stacks when you create them\. For example, for your development environments, you can specify a lower\-cost instance type compared to your production environment, but all other configurations and settings remain the same\. For more information about parameters, mappings, and conditions, see [Template anatomy](template-anatomy.md)\.

## Use nested stacks to reuse common template patterns<a name="nested"></a>

As your infrastructure grows, common patterns can emerge in which you declare the same components in each of your templates\. You can separate out these common components and create dedicated templates for them\. That way, you can mix and match different templates but use nested stacks to create a single, unified stack\. Nested stacks are stacks that create other stacks\. To create nested stacks, use the [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html) resource in your template to reference other templates\.

For example, assume that you have a load balancer configuration that you use for most of your stacks\. Instead of copying and pasting the same configurations into your templates, you can create a dedicated template for the load balancer\. Then, you just use the [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html) resource to reference that template from within other templates\. If the load balancer template is updated, any stack that is referencing it will use the updated load balancer \(only after you update the stack\)\. In addition to simplifying updates, this approach lets you use exports to create and maintain components that you might not be necessarily familiar with\. All you need to do is reference their templates\.

## Use AWS\-specific parameter types<a name="parmtypes"></a>

If your template requires inputs for existing AWS\-specific values, such as existing Amazon Virtual Private Cloud IDs or an Amazon EC2 key pair name, use AWS\-specific parameter types\. For example, you can specify a parameter as type `AWS::EC2::KeyPair::KeyName`, which takes an existing key pair name that is in your AWS account and in the region where you are creating the stack\. AWS CloudFormation can quickly validate values for AWS\-specific parameter types before creating your stack\. Also, if you use the AWS CloudFormation console, AWS CloudFormation shows a drop\-down list of valid values, so you don't have to look up or memorize the correct VPC IDs or key pair names\. For more information, see [Parameters](parameters-section-structure.md)\.

## Use parameter constraints<a name="parmconstraints"></a>

With constraints, you can describe allowed input values so that AWS CloudFormation catches any invalid values before creating a stack\. You can set constraints such as a minimum length, maximum length, and allowed patterns\. For example, you can set constraints on a database user name value so that it must be a minimum length of eight character and contain only alpha\-numeric characters\. For more information, see [Parameters](parameters-section-structure.md)\.

## Use AWS::CloudFormation::Init to deploy software applications on Amazon EC2 instances<a name="cfninit"></a>

When you launch stacks, you can install and configure software applications on Amazon EC2 instances by using the cfn\-init helper script and the `AWS::CloudFormation::Init` resource\. By using `AWS::CloudFormation::Init`, you can describe the configurations that you want rather than scripting procedural steps\. You can also update configurations without recreating instances\. And if anything goes wrong with your configuration, AWS CloudFormation generates logs that you can use to investigate issues\.

In your template, specify installation and configuration states in the `AWS::CloudFormation::Init` resource\. For a walkthrough that shows how to use cfn\-init and `AWS::CloudFormation::Init`, see [Deploying applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.

## Use the latest helper scripts<a name="helper-scripts"></a>

The [helper scripts](cfn-helper-scripts-reference.md) are updated periodically\. Be sure you include the following command in the `UserData` property of your template before you call the helper scripts to ensure that your launched instances get the latest helper scripts:

```
yum install -y aws-cfn-bootstrap
```

For more information about getting the latest helper scripts, see the [CloudFormation helper scripts reference](cfn-helper-scripts-reference.md)\.

## Validate templates before using them<a name="validate"></a>

Before you use a template to create or update a stack, you can use AWS CloudFormation to validate it\. Validating a template can help you catch syntax and some semantic errors, such as circular dependencies, before AWS CloudFormation creates any resources\. If you use the AWS CloudFormation console, the console automatically validates the template after you specify input parameters\. For the AWS CLI or AWS CloudFormation API, use the [aws cloudformation validate\-template](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/validate-template.html) command or [ValidateTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ValidateTemplate.html) action\.

During validation, AWS CloudFormation first checks if the template is valid JSON\. If it isn't, AWS CloudFormation checks if the template is valid YAML\. If both checks fail, AWS CloudFormation returns a template validation error\.

### Validate templates for organization policy compliance<a name="validate-compliance"></a>

You can also validate your template for compliance to organization policy guidelines\. AWS CloudFormation Guard \(`cfn-guard`\) is an open\-source command\-line\-interface \(CLI\) tool that provides a policy\-as\-code language to define rules that can check for both required and prohibited resource configurations\. It then enables you to validate your templates against those rules\. For example, administrators can create rules to ensure that users always create encrypted Amazon S3 buckets\.

You can use `cfn-guard` either locally, while editing templates, or automatically as part of a CI/CD pipeline to stop deployment of non\-compliant resources\.

Additionally, `cfn-guard` includes a feature, `rulegen`, that enables you to extract rules from existing compliant CloudFormation templates\.

For more information, see the [cfn\-guard](https://github.com/aws-cloudformation/cloudformation-guard) repository on GitHub\.

## Manage all stack resources through AWS CloudFormation<a name="donttouch"></a>

After you launch a stack, use the AWS CloudFormation [console](https://console.aws.amazon.com/cloudformation/home), [API](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/), or [AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/index.html) to update resources in your stack\. Do not make changes to stack resources outside of AWS CloudFormation\. Doing so can create a mismatch between your stack's template and the current state of your stack resources, which can cause errors if you update or delete the stack\. For more information, see [Walkthrough: Updating a stack](updating.stacks.walkthrough.md)\.

## Create change sets before updating your stacks<a name="cfn-best-practices-changesets"></a>

 Change sets allow you to see how proposed changes to a stack might impact your running resources before you implement them\. AWS CloudFormation doesn't make any changes to your stack until you run the change set, allowing you to decide whether to proceed with your proposed changes or create another change set\.

Use change sets to check how your changes might impact your running resources, especially for critical resources\. For example, if you change the name of an Amazon RDS database instance, AWS CloudFormation will create a new database and delete the old one; you will lose the data in the old database unless you've already backed it up\. If you generate a change set, you will see that your change will replace your database\. This can help you plan before you update your stack\. For more information, see [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md)\.

## Use stack policies<a name="stackpolicy"></a>

Stack policies help protect critical stack resources from unintentional updates that could cause resources to be interrupted or even replaced\. A stack policy is a JSON document that describes what update actions can be performed on designated resources\. Specify a stack policy whenever you create a stack that has critical resources\.

During a stack update, you must explicitly specify the protected resources that you want to update; otherwise, no changes are made to protected resources\. For more information, see [Prevent updates to stack resources](protect-stack-resources.md)\.

## Use code reviews and revision controls to manage your templates<a name="code"></a>

Your stack templates describe the configuration of your AWS resources, such as their property values\. To review changes and to keep an accurate history of your resources, use code reviews and revision controls\. These methods can help you track changes between different versions of your templates, which can help you track changes to your stack resources\. Also, by maintaining a history, you can always revert your stack to a certain version of your template\.

## Update your Amazon EC2 Linux instances regularly<a name="update-ec2-linux"></a>

On all your Amazon EC2 Linux instances and Amazon EC2 Linux instances created with AWS CloudFormation, regularly run the `yum update` command to update the RPM package\. This ensures that you get the latest fixes and security updates\.