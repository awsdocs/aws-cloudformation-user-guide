# Prevent updates to stack resources<a name="protect-stack-resources"></a>

When you create a stack, all update actions are allowed on all resources\. By default, anyone with stack update permissions can update all of the resources in the stack\. During an update, some resources might require an interruption or be completely replaced, resulting in new physical IDs or completely new storage\. You can prevent [stack resources](aws-template-resource-type-ref.md) from being unintentionally updated or deleted during a stack update by using a stack policy\. A stack policy is a JSON document that defines the update actions that can be performed on designated resources\. 

After you set a stack policy, all of the resources in the stack are protected by default\. To allow updates on specific resources, you specify an explicit `Allow` statement for those resources in your stack policy\. You can define only one stack policy per stack, but, you can protect multiple resources within a single policy\. A stack policy applies to all AWS CloudFormation users who attempt to update the stack\. You can't associate different stack policies with different users\. 

A stack policy applies only during stack updates\. It doesn't provide access controls like an AWS Identity and Access Management \(IAM\) policy\. Use a stack policy only as a fail\-safe mechanism to prevent accidental updates to specific stack resources\. To control access to AWS resources or actions, use IAM\.

**Topics**
+ [Example stack policy](#stack-policy-intro-example)
+ [Defining a stack policy](#stack-policy-reference)
+ [Setting a stack policy](#protect-stack-resources-protecting)
+ [Updating protected resources](#protect-stack-resources-updating)
+ [Modifying a stack policy](#protect-stack-resources-modifying)
+ [More example stack policies](#stack-policy-samples)

## Example stack policy<a name="stack-policy-intro-example"></a>

The following example stack policy prevents updates to the `ProductionDatabase` resource:

```
{
  "Statement" : [
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    },
    {
      "Effect" : "Deny",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "LogicalResourceId/ProductionDatabase"
    }
  ]
}
```

When you set a stack policy, all resources are protected by default\. To allow updates on all resources, we add an `Allow` statement that allows all actions on all resources\. Although the `Allow` statement specifies all resources, the explicit `Deny` statement overrides it for the resource with the `ProductionDatabase` logical ID\. This `Deny` statement prevents all update actions, such as replacement or deletion, on the `ProductionDatabase` resource\.

The `Principal` element is required, but supports only the wild card \(`*`\), which means that the statement applies to all [principals](https://docs.aws.amazon.com/general/latest/gr/glos-chap.html#principal)\.

**Note**  
During a stack update, AWS CloudFormation automatically updates resources that depend on other updated resources\. For example, AWS CloudFormation updates a resource that references an updated resource\. AWS CloudFormation makes no physical changes, such as the resource's ID, to automatically updated resources, but if a stack policy is associated with those resources, you must have permission to update them\.

## Defining a stack policy<a name="stack-policy-reference"></a>

 When you create a stack, no stack policy is set, so all update actions are allowed on all resources\. To protect stack resources from update actions, define a stack policy and then set it on your stack\. A stack policy is a JSON document that defines the AWS CloudFormation stack update actions that AWS CloudFormation users can perform and the resources that the actions apply to\. You set the stack policy when you create a stack, by specifying a text file that contains your stack policy or typing it out\. When you set a stack policy on your stack, any update not explicitly allowed is denied by default\.

You define a stack policy with five elements: `Effect`, `Action`, `Principal`, `Resource`, and `Condition`\. The following pseudo code shows stack policy syntax\. 

```
{
  "Statement" : [
    {
      "Effect" : "Deny_or_Allow",
      "Action" : "update_actions",
      "Principal" : "*",
      "Resource" : "LogicalResourceId/resource_logical_ID",
      "Condition" : {
        "StringEquals_or_StringLike" : {
          "ResourceType" : [resource_type, ...]
        }
      }
    }  
  ]
}
```

`Effect`  
Determines whether the actions that you specify are denied or allowed on the resource\(s\) that you specify\. You can specify only `Deny` or `Allow`, such as:  

```
"Effect" : "Deny"
```
If a stack policy includes overlapping statements \(both allowing and denying updates on a resource\), a `Deny` statement always overrides an `Allow` statement\. To ensure that a resource is protected, use a `Deny` statement for that resource\.

Action  
Specifies the update actions that are denied or allowed:    
Update:Modify  
Specifies update actions during which resources might experience no interruptions or some interruptions while changes are being applied\. All resources maintain their physical IDs\.  
Update:Replace  
Specifies update actions during which resources are recreated\. AWS CloudFormation creates a new resource with the specified updates and then deletes the old resource\. Because the resource is recreated, the physical ID of the new resource might be different\.  
Update:Delete  
Specifies update actions during which resources are removed\. Updates that completely remove resources from a stack template require this action\.  
Update:\*  
Specifies all update actions\. The asterisk is a wild card that represents all update actions\.
The following example shows how to specify just the replace and delete actions:  

```
"Action" : ["Update:Replace", "Update:Delete"]
```
To allow all update actions except for one, use `NotAction`\. For example, to allow all update actions except for `Update:Delete`, use `NotAction`, as shown in this example:  

```
{
  "Statement" : [
    {
      "Effect" : "Allow",
      "NotAction" : "Update:Delete",
      "Principal": "*",
      "Resource" : "*"
    }
  ]
}
```
For more information about stack updates, see [AWS CloudFormation stack updates](using-cfn-updating-stacks.md)\.

Principal  
The `Principal` element specifies the entity that the policy applies to\. This element is required but supports only the wild card \(`*`\), which means that the policy applies to all [principals](https://docs.aws.amazon.com/general/latest/gr/glos-chap.html#principal)\.

Resource  
Specifies the logical IDs of the resources that the policy applies to\. To specify [types of resources](aws-template-resource-type-ref.md), use the `Condition` element\.  
To specify a single resource, use its logical ID\. For example:  

```
"Resource" : ["LogicalResourceId/myEC2instance"]
```
You can use a wild card with logical IDs\. For example, if you use a common logical ID prefix for all related resources, you can specify all of them with a wild card:  

```
"Resource" : ["LogicalResourceId/CriticalResource*"]
```
You can also use a `Not` element with resources\. For example, to allow updates to all resources except for one, use a `NotResource` element to protect that resource:  

```
{
  "Statement" : [
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "NotResource" : "LogicalResourceId/ProductionDatabase"
    }
  ]
}
```
When you set a stack policy, any update not explicitly allowed is denied\. By allowing updates to all resources except for the `ProductionDatabase` resource, you deny updates to the `ProductionDatabase` resource\.

Conditions  
Specifies the [resource type](aws-template-resource-type-ref.md) that the policy applies to\. To specify the logical IDs of specific resources, use the `Resource` element\.  
You can specify a resource type, such as all EC2 and RDS DB instances, as shown in the following example:  

```
{
  "Statement" : [
  {
    "Effect" : "Deny",
    "Principal" : "*",
    "Action" : "Update:*",
    "Resource" : "*",
    "Condition" : {
      "StringEquals" : {
        "ResourceType" : ["AWS::EC2::Instance", "AWS::RDS::DBInstance"]
      }
    }
  },
  {
    "Effect" : "Allow",
    "Principal" : "*",
    "Action" : "Update:*",
    "Resource" : "*"
  }
  ]
}
```
The `Allow` statement grants update permissions to all resources and the `Deny` statement denies updates to EC2 and RDS DB instances\. The `Deny` statement always overrides allow actions\.  
You can use a wild card with resource types\. For example, you can deny update permissions to all Amazon EC2 resources—such as instances, security groups, and subnets—by using a wild card, as shown in the following example:  

```
"Condition" : {
  "StringLike" : {
    "ResourceType" : ["AWS::EC2::*"]
  }
}
```
You must use the `StringLike` condition when you use wild cards\.

## Setting a stack policy<a name="protect-stack-resources-protecting"></a>

You can use the console or AWS CLI to apply a stack policy when you create a stack\. You can also use the AWS CLI to apply a stack policy to an existing stack\. After you apply a stack policy, you can't remove it from the stack, but you can use the AWS CLI to modify it\.

Stack policies apply to all AWS CloudFormation users who attempt to update the stack\. You can't associate different stack policies with different users\.

For information about writing stack policies, see [Defining a stack policy](#stack-policy-reference)\. 

**To set a stack policy when you create a stack \(console\)**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. On the **CloudFormation Stacks** page, choose **Create stack**\.

1. In the Create Stack wizard, on the **Configure stack options** page, expand the **Advanced** section and then choose **Stack policy**\.

1. Specify the stack policy:
   + To write a policy directly in the console, choose **Enter stack policy** and then type the stack policy directly in the text field\.
   + To use a policy defined in a separate file, choose **Upload a file**, then **Choose file** to select the file containing the stack policy\.

**To set a stack policy when you create a stack \(CLI\)**
+ Use the `[aws cloudformation create\-stack](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)` command with the `--stack-policy-body` option to type in a modified policy or the `--stack-policy-url` option to specify a file containing the policy\. 

**To set a stack policy on an existing stack \(CLI only\)**
+ Use the `[aws cloudformation set\-stack\-policy](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-stack-policy.html)` command with the `--stack-policy-body` option to type in a modified policy or the `--stack-policy-url` option to specify a file containing the policy\.
**Note**  
To add a policy to an existing stack, you must have permission to the AWS CloudFormation `SetStackPolicy` action\.

## Updating protected resources<a name="protect-stack-resources-updating"></a>

To update protected resources, create a temporary policy that overrides the stack policy and allows updates on those resources\. Specify the override policy when you update the stack\. The override policy doesn't permanently change the stack policy\.

 To update protected resources, you must have permission to use the AWS CloudFormation `SetStackPolicy` action\. For information about setting AWS CloudFormation permissions, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\.

**Note**  
During a stack update, AWS CloudFormation automatically updates resources that depend on other updated resources\. For example, AWS CloudFormation updates a resource that references an updated resource\. AWS CloudFormation makes no physical changes, such as the resources' ID, to automatically updated resources, but if a stack policy is associated with those resources, you must have permission to update them\.

**To update a protected resource \(console\)**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. Select the stack that you want to update, choose **Stack actions**, and then choose **Update stack**\.

1. If you *haven't* modified the stack template, select **Use current template**, and then click **Next**\. If you have modified the template, select **Replace current template** and specify the location of the updated template in the **Specify template** section:
   + For a template stored locally on your computer, select **Upload a template file**\. Choose **Choose File** to navigate to the file and select it, and then click **Next**\.
   + For a template stored in an Amazon S3 bucket, select **Amazon S3 URL**\. Enter or paste the URL for the template, and then click **Next**\.

     If you have a template in a versioning\-enabled bucket, you can specify a specific version of the template, such as `https://s3.amazonaws.com/templates/myTemplate.template?versionId=123ab1cdeKdOW5IH4GAcYbEngcpTJTDW`\. For more information, see [Managing objects in a versioning\-enabled bucket](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/managing-objects-versioned-bucket.html) in the *Amazon Simple Storage Service Console User Guide*\.

1. If your template contains parameters, on the **Specify stack details** page, enter or modify the parameter values, and then choose **Next**\.

   AWS CloudFormation populates each parameter with the value that is currently set in the stack except for parameters declared with the `NoEcho` attribute\. You can use current values for those parameters by choosing **Use existing value**\.

   For more information about using `NoEcho` to mask sensitive information, as well as using dynamic parameters to manage secrets, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

1. Specify an override stack policy\.

   1. On the **Configure stack options** page, in the **Advanced options** section, select **Stack policy**\.

   1. Select **Upload a file**\.

   1. Click **Choose file** and navigate to the file that contains the overriding stack policy or type a policy\.

   1. Choose **Next**\. 

   The override policy must specify an `Allow` statement for the protected resources that you want to update\. For example, to update all protected resources, specify a temporary override policy that allows all updates:

   ```
   {
     "Statement" : [
       {
         "Effect" : "Allow",
         "Action" : "Update:*",
         "Principal": "*",
         "Resource" : "*"
       }  
     ]
   }
   ```
**Note**  
AWS CloudFormation applies the override policy only during this update\. The override policy doesn't permanently change the stack policy\. To modify a stack policy, see [Modifying a stack policy ](#protect-stack-resources-modifying)\.

1. Review the stack information and the changes that you submitted\.

   Check that you submitted the correct information, such as the correct parameter values or template URL\. If your template contains IAM resources, choose **I acknowledge that this template may create IAM resources** to specify that you want to use IAM resources in the template\. For more information about using IAM resources in templates, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\.

   In the **Preview your changes** section, check that AWS CloudFormation will make all the changes that you expect\. For example, check that AWS CloudFormation adds, removes, and modifies the resources that you intended to add, remove, or modify\. AWS CloudFormation generates this preview by creating a change set for the stack\. For more information, see [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md)\.

1. When you are satisfied with your changes, click **Update**\.
**Note**  
At this point, you also have the option to view the change set to review your proposed updates more thoroughly\. To do so, click **View change set** instead of **Update**\. CloudFormation displays the change set generated based on your updates\. When you are ready to perform the stack update, click **Execute**\.

   CloudFormation displays the **Stack details** page for your stack\. Your stack now has a status of **UPDATE\_IN\_PROGRESS**\. After CloudFormation has successfully finished updating the stack, it sets the stack status to **UPDATE\_COMPLETE**\.

   If the stack update fails, CloudFormation; automatically rolls back changes, and sets the stack status to **UPDATE\_ROLLBACK\_COMPLETE**\.

**To update a protected resource \(CLI\)**
+ Use the `[aws cloudformation update\-stack](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html)` command with the `--stack-policy-during-update-body` option to type in a modified policy or the `--stack-policy-during-update-url` option to specify a file containing the policy\.
**Note**  
AWS CloudFormation applies the override policy only during this update\. The override policy doesn't permanently change the stack policy\. To modify a stack policy, see [Modifying a stack policy ](#protect-stack-resources-modifying)\.

## Modifying a stack policy<a name="protect-stack-resources-modifying"></a>

To protect additional resources or to remove protection from resources, modify the stack policy\. For example, when you add a database that you want to protect to your stack, add a `Deny` statement for that database to the stack policy\. To modify the policy, you must have permission to use the `SetStackPolicy` action\.

Use the AWS CLI to modify stack policies\.

**To modify a stack policy \(CLI\)**
+ Use the `[aws cloudformation set\-stack\-policy](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-stack-policy.html)` command with the `--stack-policy-body` option to type in a modified policy or the `--stack-policy-url` option to specify a file containing the policy\.

You can't delete a stack policy\. To remove all protection from all resources, you modify the policy to explicitly allow all actions on all resources\. The following policy allows all updates on all resources:

```
{
  "Statement" : [
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    }  
  ]
}
```

## More example stack policies<a name="stack-policy-samples"></a>

The following example policies show how to prevent updates to all stack resources and to specific resources, and prevent specific types of updates\.

### Prevent updates to all stack resources<a name="w7739ab1c23c17c29c21b4"></a>

To prevent updates to all stack resources, the following policy specifies a `Deny` statement for all update actions on all resources\.

```
{
  "Statement" : [
    {
      "Effect" : "Deny",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    }  
  ]
}
```

### Prevent updates to a single resource<a name="w7739ab1c23c17c29c21b6"></a>

The following policy denies all update actions on the database with the `MyDatabase` logical ID\. It allows all update actions on all other stack resources with an `Allow` statement\. The `Allow` statement doesn't apply to the `MyDatabase` resource because the `Deny` statement always overrides allow actions\.

```
{
  "Statement" : [
    {
      "Effect" : "Deny",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "LogicalResourceId/MyDatabase"
    },
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    }
  ]
}
```

You can achieve the same result as the previous example by using a default denial\. When you set a stack policy, AWS CloudFormation denies any update that is not explicitly allowed\. The following policy allows updates to all resources except for the `ProductionDatabase` resource, which is denied by default\.

```
{
  "Statement" : [
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "NotResource" : "LogicalResourceId/ProductionDatabase"
    }
  ]
}
```

**Important**  
There is risk in using a default denial\. If you have an `Allow` statement elsewhere in the policy \(such as an `Allow` statement that uses a wildcard\), you might unknowingly grant update permission to resources that you don't intend to\. Because an explicit denial overrides any allow actions, you can ensure that a resource is protected by using a `Deny` statement\.

### Prevent updates to all instances of a resource type<a name="w7739ab1c23c17c29c21b8"></a>

The following policy denies all update actions on the RDS DB instance resource type\. It allows all update actions on all other stack resources with an `Allow` statement\. The `Allow` statement doesn't apply to the RDS DB instance resources because a `Deny` statement always overrides allow actions\.

```
{
  "Statement" : [
    {
      "Effect" : "Deny",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*",
      "Condition" : {
        "StringEquals" : {
          "ResourceType" : ["AWS::RDS::DBInstance"]
        }
      }
    },
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    }
  ]
}
```

### Prevent replacement updates for an instance<a name="w7739ab1c23c17c29c21c10"></a>

The following policy denies updates that would cause a replacement of the instance with the `MyInstance` logical ID\. It allows all update actions on all other stack resources with an `Allow` statement\. The `Allow` statement doesn't apply to the `MyInstance` resource because the `Deny` statement always overrides allow actions\.

```
{
  "Statement" : [
    {
      "Effect" : "Deny",
      "Action" : "Update:Replace",
      "Principal": "*",
      "Resource" : "LogicalResourceId/MyInstance"
    },
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    }
  ]
}
```

### Prevent updates to nested stacks<a name="w7739ab1c23c17c29c21c12"></a>

The following policy denies all update actions on the AWS CloudFormation stack resource type \(nested stacks\)\. It allows all update actions on all other stack resources with an `Allow` statement\. The `Allow` statement doesn't apply to the AWS CloudFormationstack resources because the `Deny` statement always overrides allow actions\.

```
{
  "Statement" : [
    {
      "Effect" : "Deny",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*",
      "Condition" : {
        "StringEquals" : {
          "ResourceType" : ["AWS::CloudFormation::Stack"]
        }
      }
    },
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    }
  ]
}
```