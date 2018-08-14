# AWS::IAM::User<a name="aws-properties-iam-user"></a>

The `AWS::IAM::User` type creates a user\.

**Topics**
+ [Syntax](#aws-resource-iam-user-syntax)
+ [Properties](#aws-properties-iam-user-prop)
+ [Return Values](#aws-properties-iam-user-ref)
+ [Template Examples](#w3ab2c21c10d772c13)

## Syntax<a name="aws-resource-iam-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-user-syntax.json"></a>

```
{
  "Type": "AWS::IAM::User",
  "Properties": {
    "[Groups](#cfn-iam-user-groups)": [ String, ... ],
    "[LoginProfile](#cfn-iam-user-loginprofile)": LoginProfile Type,
    "[ManagedPolicyArns](#cfn-iam-user-managepolicyarns)": [ String, ... ],
    "[Path](#cfn-iam-user-path)": String,
    "[Policies](#cfn-iam-user-policies)": [ Policies, ... ],
    "[UserName](#cfn-iam-user-username)": String
  }
}
```

### YAML<a name="aws-resource-iam-user-syntax.yaml"></a>

```
Type: "AWS::IAM::User"
Properties: 
  [Groups](#cfn-iam-user-groups):
    - String
  [LoginProfile](#cfn-iam-user-loginprofile):
    LoginProfile Type
  [ManagedPolicyArns](#cfn-iam-user-managepolicyarns):
    - String
  [Path](#cfn-iam-user-path): String
  [Policies](#cfn-iam-user-policies):
    - Policies
  [UserName](#cfn-iam-user-username): String
```

## Properties<a name="aws-properties-iam-user-prop"></a>

`Groups`  <a name="cfn-iam-user-groups"></a>
A name of a group to which you want to add the user\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LoginProfile`  <a name="cfn-iam-user-loginprofile"></a>
Creates a login profile so that the user can access the AWS Management Console\.  
*Required*: No  
*Type*: [IAM User LoginProfile](aws-properties-iam-user-loginprofile.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ManagedPolicyArns`  <a name="cfn-iam-user-managepolicyarns"></a>
One or more managed policy ARNs to attach to this user\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Path`  <a name="cfn-iam-user-path"></a>
The path for the user name\. For more information about paths, see [IAM Identifiers](http://docs.aws.amazon.com/IAM/latest/UserGuide/index.html?Using_Identifiers.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Policies`  <a name="cfn-iam-user-policies"></a>
The policies to associate with this user\. For information about policies, see [Overview of IAM Policies](http://docs.aws.amazon.com/IAM/latest/UserGuide/index.html?PoliciesOverview.html) in the *IAM User Guide*\.  
If you specify multiple polices, specify unique values for the policy name\. If you don't, updates to the IAM user will fail\.
*Required*: No  
*Type*: List of [IAM Policies](aws-properties-iam-policy.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UserName`  <a name="cfn-iam-user-username"></a>
A name for the IAM user\. For valid values, see the `UserName` parameter for the [http://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateUser.html](http://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateUser.html) action in the *IAM API Reference*\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the user name\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
If you specify a name, you must specify the `CAPABILITY_NAMED_IAM` value to acknowledge your template's capabilities\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](using-iam-template.md#using-iam-capabilities)\.   
Naming an IAM resource can cause an unrecoverable error if you reuse the same template in multiple regions\. To prevent this, we recommend using `Fn::Join` and `AWS::Region` to create a region\-specific name, as in the following example: `{"Fn::Join": ["", [{"Ref": "AWS::Region"}, {"Ref": "MyResourceName"}]]}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-properties-iam-user-ref"></a>

### Ref<a name="w3ab2c21c10d772c11b2"></a>

Specifying this resource ID to the intrinsic Ref function will return the `UserName`\. For example: `mystack-myuser-1CCXAFG2H2U4D`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d772c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
Returns the Amazon Resource Name \(ARN\) for the specified AWS::IAM::User resource\. For example: `arn:aws:iam::123456789012:user/mystack-myuser-1CCXAFG2H2U4D`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Template Examples<a name="w3ab2c21c10d772c13"></a>

To view AWS::IAM::User snippets, see: [Declaring an IAM User Resource](quickref-iam.md#scenario-iam-user)\.