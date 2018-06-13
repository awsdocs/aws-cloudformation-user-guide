# Protecting a Stack From Being Deleted<a name="using-cfn-protect-stacks"></a>

You can prevent a stack from being accidently deleted by enabling termination protection on the stack\. If a user attempts to delete a stack with termination protection enabled, the deletion fails and the stack\-\-including its status\-\-remains unchanged\. You can enable termination protection on a stack when you create it\. Termination protection on stacks is disabled by default\. You can set termination protection on a stack with any status except **DELETE\_IN\_PROGRESS** or **DELETE\_COMPLETE**\.

Enabling or disabling termination protection on a stack sets it for any nested stacks belonging to that stack as well\. You cannot enable or disable termination protection directly on a nested stack\. If a user attempts to directly delete a nested stack belonging with a stack that has termination protection enabled, the operation fails and the nested stack remains unchanged\.

However, if a user performs a stack update that would delete the nested stack, AWS CloudFormation deletes the nested stack accordingly\.

Termination protection is different than disabling rollback\. Termination protection applies only to attempts to delete stacks, while disabling rollback applies to auto rollback when stack creation fails\.

**To enable termination protection when creating a stack**
+ Select **Enable Termination Protection** when you are creating your stack\.

  For more information, see [Setting Stack Options](cfn-console-add-tags.md) in [Creating a Stack](cfn-console-create-stack.md)\.

**To enable or disable termination protection on an existing stack**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\. Select the stack that you want\.
**Note**  
If **NESTED** is displayed next to the stack name, the stack is a nested stack\. You can only change termination protection on the root stack to which the nested stack belongs\.

1. Choose **Actions** and then **Change Termination Protection**\.

   CloudFormation displays **Enable Termination Protection** or **Disable Termination Protection**, based on the current termination protection setting for the stack\.

1. Choose **Yes, Enable** or **Yes, Disable**\.

**To enable or disable termination protection on a nested stack**

If **NESTED** is displayed next to the stack name, the stack is a nested stack\. You can only change termination protection on the root stack to which the nested stack belongs\. To change termination protection on the root stack:

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\. Select the nested stack that you want\.

1. On the **Overview** tab, click the stack name listed as **Root stack**\.

1. Choose **Other Actions** and then choose **Change Termination Protection**\.

   CloudFormation displays **Enable Termination Protection** or **Disable Termination Protection**, based on the current termination protection setting for the stack\.

1. Choose **Yes, Enable** or **Yes, Disable**\.

**To enable or disable termination protection using the command line**
+ Use the [update\-termination\-protection](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-termination-protection.html) command\.

## Controlling Who Can Change Termination Protection on Stacks<a name="protect-stacks-perms"></a>

To enable or disable termination protection on stacks, a user requires permission to the `cloudformation:UpdateTerminationProtection` action\. For example, the policy below allows users to enable or disable termination protection on stacks\.

For more information on specifying permissions in AWS CloudFormation, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.

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