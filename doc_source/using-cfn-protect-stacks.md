# Protecting a stack from being deleted<a name="using-cfn-protect-stacks"></a>

You can prevent a stack from being accidentally deleted by enabling termination protection on the stack\. If a user attempts to delete a stack with termination protection enabled, the deletion fails and the stack\-\-including its status\-\-remains unchanged\. You can enable termination protection on a stack when you create it\. Termination protection on stacks is disabled by default\. You can set termination protection on a stack with any status except **DELETE\_IN\_PROGRESS** or **DELETE\_COMPLETE**\.

Enabling or disabling termination protection on a stack sets it for any nested stacks belonging to that stack as well\. You cannot enable or disable termination protection directly on a nested stack\. If a user attempts to directly delete a nested stack belonging with a stack that has termination protection enabled, the operation fails and the nested stack remains unchanged\.

However, if a user performs a stack update that would delete the nested stack, AWS CloudFormation deletes the nested stack accordingly\.

Termination protection is different than disabling rollback\. Termination protection applies only to attempts to delete stacks, while disabling rollback applies to auto rollback when stack creation fails\.

**To enable termination protection when creating a stack**
+ On the **Specify stack options** page of the **Create stack** wizard, under **Advanced options**, expand the **Termination Protection** section and select **Enable**\.

  For more information, see [Setting AWS CloudFormation stack options](cfn-console-add-tags.md) in [Creating a stack on the AWS CloudFormation console](cfn-console-create-stack.md)\.

**To enable or disable termination protection on an existing stack**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\. 

1. Select the stack that you want\.
**Note**  
If **NESTED** is displayed next to the stack name, the stack is a nested stack\. You can only change termination protection on the root stack to which the nested stack belongs\.

1. In the stack details pane, select **Stack actions** and then **Edit termination protection**\.

   CloudFormation displays the **Edit termination protection** dialog box\.

1. Choose **Enable** or **Disable**, and then select **Save**\.

**To enable or disable termination protection on a nested stack**

If **NESTED** is displayed next to the stack name, the stack is a nested stack\. You can only change termination protection on the root stack to which the nested stack belongs\. To change termination protection on the root stack:

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\.

1. Select the nested stack that you want\.

1. In the **Stack info** pane, in the **Overview** section, select the stack name listed as **Root stack**\.

   AWS CloudFormation displays the stack details for the root stack\.

1. Choose **Stack actions** and then choose **Edit Termination Protection**\.

   CloudFormation displays the **Edit termination protection** dialog box\.

1. Choose **Enable** or **Disable**, and then select **Save**\.

**To enable or disable termination protection using the command line**
+ Use the [update\-termination\-protection](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-termination-protection.html) command\.

## Controlling who can change termination protection on stacks<a name="protect-stacks-perms"></a>

To enable or disable termination protection on stacks, a user requires permission to the `cloudformation:UpdateTerminationProtection` action\. For example, the policy below allows users to enable or disable termination protection on stacks\.

For more information on specifying permissions in AWS CloudFormation, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\.

**Example A sample policy that grants permissions to change stack termination protection**  

```
{
    "Version":"2012-10-17",
    "Statement":[{
        "Effect":"Allow",
        "Action":[
            "cloudformation:UpdateTerminationProtection"
        ],
        "Resource":"*"
    }]
}
```