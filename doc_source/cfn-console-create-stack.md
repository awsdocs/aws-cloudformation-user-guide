# Creating a stack on the AWS CloudFormation console<a name="cfn-console-create-stack"></a>

Before you create a stack, you must have a template that describes what resources AWS CloudFormation will include in your stack\. For more information, see [Working with AWS CloudFormation templates](template-guide.md)\.

**Note**  
To preview the configuration of a new stack, you can [use a change set](cfn-console-create-stacks-changesets.md)\.

Creating a stack on the AWS CloudFormation console is an easy, wizard\-driven process that consists of the following steps:

1. [Starting the Create Stack wizard](#cfn-using-console-initiating-stack-creation)

1. [Selecting a stack template](cfn-using-console-create-stack-template.md)

1. [Specifying stack parameters](cfn-using-console-create-stack-parameters.md)

1. [Setting AWS CloudFormation stack options](cfn-console-add-tags.md)

1. [Reviewing your stack](cfn-using-console-create-stack-review.md)

After creating a stack, you can monitor the stack's progress, view the stack's resources and outputs, update the stack, and delete it\. Information about these actions are provided in their associated topics\.

## Starting the Create Stack wizard<a name="cfn-using-console-initiating-stack-creation"></a>

**To create a stack on the AWS CloudFormation console**

1. Log in to the AWS Management Console and select **CloudFormation** in the **Services** menu\.

1. Create a new stack by using one of the following options:
   + Click **Create Stack**\. This is the *only* option if you have a currently running stack\.
   + Click **Create Stack** on the **Stacks** page\. This option is visible only if you have no running stacks\.  
![\[The Create Stack button in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stack-stacks-create-stack.png)

Next, you [choose a stack template](cfn-using-console-create-stack-template.md)\.