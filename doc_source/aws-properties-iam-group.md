# AWS::IAM::Group<a name="aws-properties-iam-group"></a>

The `AWS::IAM::Group` resource creates an AWS Identity and Access Management \(IAM\) group\.

This type supports updates\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.


+ [Syntax](#aws-resource-iam-group-syntax)
+ [Properties](#aws-properties-iam-group-prop)
+ [Return Values](#aws-properties-iam-group-ref)
+ [Template Examples](#w3ab2c21c10d699c15)

## Syntax<a name="aws-resource-iam-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-group-syntax.json"></a>

```
{
   "Type": "AWS::IAM::Group",
   "Properties": {
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-groupname)": String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-managepolicyarns)": [ String, ... ],
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-path)": String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-policies)": [ Policies, ... ]
   }
}
```

### YAML<a name="aws-resource-iam-group-syntax.yaml"></a>

```
Type: "AWS::IAM::Group"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-groupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-managepolicyarns): [ String, ... ]
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-path): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-iam-group-policies):
    - Policies
```

## Properties<a name="aws-properties-iam-group-prop"></a>

`GroupName`  
A name for the IAM group\. For valid values, see the `GroupName` parameter for the [http://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateGroup.html](http://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateGroup.html) action in the *IAM API Reference*\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the group name\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
If you specify a name, you must specify the `CAPABILITY_NAMED_IAM` value to acknowledge your template's capabilities\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](using-iam-template.md#using-iam-capabilities)\.   
Naming an IAM resource can cause an unrecoverable error if you reuse the same template in multiple regions\. To prevent this, we recommend using `Fn::Join` and `AWS::Region` to create a region\-specific name, as in the following example: `{"Fn::Join": ["", [{"Ref": "AWS::Region"}, {"Ref": "MyResourceName"}]]}`\.
*Required*: No  
*Type*: String  
*Update requires*: Replacement

`ManagedPolicyArns`  
One or more managed policy ARNs to attach to this group\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Path`  
The path to the group\. For more information about paths, see [IAM Identifiers](http://docs.aws.amazon.com/IAM/latest/UserGuide/index.html?Using_Identifiers.html) in the *IAM User Guide*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Policies`  
The policies to associate with this group\. For information about policies, see [Overview of IAM Policies](http://docs.aws.amazon.com/IAM/latest/UserGuide/index.html?PoliciesOverview.html) in the *IAM User Guide*\.  
*Required: *No  
*Type*: List of [IAM Policies](aws-properties-iam-policy.md)  
*Update requires*: No interruption

## Return Values<a name="aws-properties-iam-group-ref"></a>

### Ref<a name="w3ab2c21c10d699c13b2"></a>

Specifying this resource ID to the intrinsic `Ref` function will return the `GroupName`\. For example: `mystack-mygroup-1DZETITOWEKVO`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d699c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
Returns the Amazon Resource Name \(ARN\) for the `AWS::IAM::Group` resource\. For example: `arn:aws:iam::123456789012:group/mystack-mygroup-1DZETITOWEKVO`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Template Examples<a name="w3ab2c21c10d699c15"></a>

To view AWS::IAM::Group snippets, see 