# AWS::IAM::InstanceProfile<a name="aws-resource-iam-instanceprofile"></a>

The `AWS::IAM::InstanceProfile` resource creates an AWS Identity and Access Management \(IAM\) instance profile that can be used with IAM roles for EC2 instances\.

For more information about IAM roles, see [Working with Roles](http://docs.aws.amazon.com/IAM/latest/UserGuide/WorkingWithRoles.html) in the *AWS Identity and Access Management User Guide*\.

**Topics**
+ [Syntax](#aws-resource-iam-instanceprofile-syntax)
+ [Properties](#w3ab2c21c10d754c11)
+ [Return Values](#w3ab2c21c10d754c13)

## Syntax<a name="aws-resource-iam-instanceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-instanceprofile-syntax.json"></a>

```
{
   "Type": "AWS::IAM::InstanceProfile",
   "Properties": {
      "[Path](#cfn-iam-instanceprofile-path)": String,
      "[Roles](#cfn-iam-instanceprofile-roles)": [ IAM Roles ],
      "[InstanceProfileName](#cfn-iam-instanceprofile-instanceprofilename)": String
   }
}
```

### YAML<a name="aws-resource-iam-instanceprofile-syntax.yaml"></a>

```
Type: "AWS::IAM::InstanceProfile"
Properties: 
  [Path](#cfn-iam-instanceprofile-path): String
  [Roles](#cfn-iam-instanceprofile-roles):
    - IAM Roles 
  [InstanceProfileName](#cfn-iam-instanceprofile-instanceprofilename): String
```

## Properties<a name="w3ab2c21c10d754c11"></a>

`Path`  <a name="cfn-iam-instanceprofile-path"></a>
The path associated with this IAM instance profile\. For information about IAM paths, see [Friendly Names and Paths](http://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html#Identifiers_FriendlyNames) in the *AWS Identity and Access Management User Guide*\.  
By default, AWS CloudFormation specifies `/` for the path\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Roles`  <a name="cfn-iam-instanceprofile-roles"></a>
The name of an existing IAM role to associate with this instance profile\. Currently, you can assign a maximum of one role to an instance profile\.  
*Required*: Yes  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceProfileName`  <a name="cfn-iam-instanceprofile-instanceprofilename"></a>
The name of the instance profile that you want to create\. This parameter allows \(per its [regex pattern](http://wikipedia.org/wiki/regex)\) a string consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: `= , . @ -`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d754c13"></a>

### Ref<a name="w3ab2c21c10d754c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyProfile" }
```

For the `IAM::InstanceProfile` with the logical ID `MyProfile`, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d754c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
Returns the Amazon Resource Name \(ARN\) for the instance profile\. For example:  

```
{"Fn::GetAtt" : ["MyProfile", "Arn"] }
```
This returns a value such as `“arn:aws:iam::1234567890:instance-profile/MyProfile-ASDNSDLKJ”`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.