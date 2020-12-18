# AWS::IAM::Group<a name="aws-properties-iam-group"></a>

Creates a new group\.

 For information about the number of groups you can create, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.

## Syntax<a name="aws-properties-iam-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iam-group-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::Group",
  "Properties" : {
      "[GroupName](#cfn-iam-group-groupname)" : String,
      "[ManagedPolicyArns](#cfn-iam-group-managepolicyarns)" : [ String, ... ],
      "[Path](#cfn-iam-group-path)" : String,
      "[Policies](#cfn-iam-group-policies)" : [ Policy, ... ]
    }
}
```

### YAML<a name="aws-properties-iam-group-syntax.yaml"></a>

```
Type: AWS::IAM::Group
Properties: 
  [GroupName](#cfn-iam-group-groupname): String
  [ManagedPolicyArns](#cfn-iam-group-managepolicyarns): 
    - String
  [Path](#cfn-iam-group-path): String
  [Policies](#cfn-iam-group-policies): 
    - Policy
```

## Properties<a name="aws-properties-iam-group-properties"></a>

`GroupName`  <a name="cfn-iam-group-groupname"></a>
The name of the group to create\. Do not include the path in this value\.  
The group name must be unique within the account\. Group names are not distinguished by case\. For example, you cannot create groups named both "ADMINS" and "admins"\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the group name\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
If you specify a name, you must specify the `CAPABILITY_NAMED_IAM` value to acknowledge your template's capabilities\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities)\.  
Naming an IAM resource can cause an unrecoverable error if you reuse the same template in multiple Regions\. To prevent this, we recommend using `Fn::Join` and `AWS::Region` to create a Region\-specific name, as in the following example: `{"Fn::Join": ["", [{"Ref": "AWS::Region"}, {"Ref": "MyResourceName"}]]}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ManagedPolicyArns`  <a name="cfn-iam-group-managepolicyarns"></a>
The Amazon Resource Name \(ARN\) of the IAM policy you want to attach\.  
For more information about ARNs, see [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-iam-group-path"></a>
 The path to the group\. For more information about paths, see [IAM Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
This parameter is optional\. If it is not included, it defaults to a slash \(/\)\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of either a forward slash \(/\) by itself or a string that must begin and end with forward slashes\. In addition, it can contain any ASCII character from the \! \(`\u0021`\) through the DEL character \(`\u007F`\), including most punctuation characters, digits, and upper and lowercased letters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `(\u002F)|(\u002F[\u0021-\u007F]+\u002F)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policies`  <a name="cfn-iam-group-policies"></a>
Adds or updates an inline policy document that is embedded in the specified IAM group\. To view AWS::IAM::Group snippets, see [Declaring an IAM Group Resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-iam-group)\.  
The name of each inline policy for a role, user, or group must be unique\. If you don't choose unique names, updates to the IAM identity will fail\. 
For information about limits on the number of inline policies that you can embed in a group, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: List of [Policy](aws-properties-iam-policy-2.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-iam-group-return-values"></a>

### Ref<a name="aws-properties-iam-group-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `GroupName`\. For example: `mystack-mygroup-1DZETITOWEKVO`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-iam-group-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-iam-group-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the specified `AWS::IAM::Group` resource\. For example: `arn:aws:iam::123456789012:group/mystack-mygroup-1DZETITOWEKVO`\.

## Examples<a name="aws-properties-iam-group--examples"></a>

### Group<a name="aws-properties-iam-group--examples--Group"></a>

In this example, create a group named "MyGroup"\.

#### JSON<a name="aws-properties-iam-group--examples--Group--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyGroup" : {
         "Type" : "AWS::IAM::Group"
      }      
   }            
}
```

#### YAML<a name="aws-properties-iam-group--examples--Group--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyGroup:
    Type: AWS::IAM::Group
```

## See also<a name="aws-properties-iam-group--seealso"></a>
+ To view `AWS::IAM::Group` template example snippets, see [Declaring an IAM Group Resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-iam-group)\. 
+  [CreateGroup](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateGroup.html) in the *AWS Identity and Access Management API Reference* 

