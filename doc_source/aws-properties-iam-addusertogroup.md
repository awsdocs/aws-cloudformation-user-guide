# AWS::IAM::UserToGroupAddition<a name="aws-properties-iam-addusertogroup"></a>

Adds the specified user to the specified group\.

## Syntax<a name="aws-properties-iam-addusertogroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iam-addusertogroup-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::UserToGroupAddition",
  "Properties" : {
      "[GroupName](#cfn-iam-addusertogroup-groupname)" : String,
      "[Users](#cfn-iam-addusertogroup-users)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-properties-iam-addusertogroup-syntax.yaml"></a>

```
Type: AWS::IAM::UserToGroupAddition
Properties : 
﻿  [GroupName](#cfn-iam-addusertogroup-groupname) : String
﻿  [Users](#cfn-iam-addusertogroup-users) : 
    - String
```

## Properties<a name="aws-properties-iam-addusertogroup-properties"></a>

`GroupName`  <a name="cfn-iam-addusertogroup-groupname"></a>
The name of the group to update\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Users`  <a name="cfn-iam-addusertogroup-users"></a>
A list of the names of the users that you want to add to the group\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-properties-iam-addusertogroup-return-values"></a>

### Ref<a name="aws-properties-iam-addusertogroup-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For example:

 `{ "Ref": "MyUserToGroupAddition" }` 

For the `AWS::IAM::UserToGroupAddition` resource with the logical ID `MyUserToGroupAddition`, `Ref` will return the AWS resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-properties-iam-addusertogroup--seealso"></a>
+ To view `AWS::IAM::UserToGroupAddition` template example snippets, see [Add Users to a Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-iam-addusertogroup)\. 
+  [AddUserToGroup](https://docs.aws.amazon.com/IAM/latest/APIReference/API_AddUserToGroup.html) in the *AWS Identity and Access Management API Reference* 