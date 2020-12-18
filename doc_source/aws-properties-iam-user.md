# AWS::IAM::User<a name="aws-properties-iam-user"></a>

Creates a new IAM user for your AWS account\.

 For information about limitations on the number of IAM users you can create, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.

## Syntax<a name="aws-properties-iam-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iam-user-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::User",
  "Properties" : {
      "[Groups](#cfn-iam-user-groups)" : [ String, ... ],
      "[LoginProfile](#cfn-iam-user-loginprofile)" : LoginProfile,
      "[ManagedPolicyArns](#cfn-iam-user-managepolicyarns)" : [ String, ... ],
      "[Path](#cfn-iam-user-path)" : String,
      "[PermissionsBoundary](#cfn-iam-user-permissionsboundary)" : String,
      "[Policies](#cfn-iam-user-policies)" : [ Policy, ... ],
      "[Tags](#cfn-iam-user-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserName](#cfn-iam-user-username)" : String
    }
}
```

### YAML<a name="aws-properties-iam-user-syntax.yaml"></a>

```
Type: AWS::IAM::User
Properties: 
  [Groups](#cfn-iam-user-groups): 
    - String
  [LoginProfile](#cfn-iam-user-loginprofile): 
    LoginProfile
  [ManagedPolicyArns](#cfn-iam-user-managepolicyarns): 
    - String
  [Path](#cfn-iam-user-path): String
  [PermissionsBoundary](#cfn-iam-user-permissionsboundary): String
  [Policies](#cfn-iam-user-policies): 
    - Policy
  [Tags](#cfn-iam-user-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserName](#cfn-iam-user-username): String
```

## Properties<a name="aws-properties-iam-user-properties"></a>

`Groups`  <a name="cfn-iam-user-groups"></a>
A list of groups to which you want to add the user\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoginProfile`  <a name="cfn-iam-user-loginprofile"></a>
 Creates a password for the specified user, giving the user the ability to access AWS services through the AWS Management Console\. For more information about managing passwords, see [Managing Passwords](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_ManagingLogins.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: [LoginProfile](aws-properties-iam-user-loginprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedPolicyArns`  <a name="cfn-iam-user-managepolicyarns"></a>
A list of Amazon Resource Names \(ARNs\) of the IAM managed policies that you want to attach to the user\.  
For more information about ARNs, see [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-iam-user-path"></a>
 The path for the user name\. For more information about paths, see [IAM Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
This parameter is optional\. If it is not included, it defaults to a slash \(/\)\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of either a forward slash \(/\) by itself or a string that must begin and end with forward slashes\. In addition, it can contain any ASCII character from the \! \(`\u0021`\) through the DEL character \(`\u007F`\), including most punctuation characters, digits, and upper and lowercased letters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `(\u002F)|(\u002F[\u0021-\u007F]+\u002F)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PermissionsBoundary`  <a name="cfn-iam-user-permissionsboundary"></a>
The ARN of the policy that is used to set the permissions boundary for the user\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policies`  <a name="cfn-iam-user-policies"></a>
Adds or updates an inline policy document that is embedded in the specified IAM user\. To view AWS::IAM::User snippets, see [Declaring an IAM User Resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-iam-user)\.  
The name of each policy for a role, user, or group must be unique\. If you don't choose unique names, updates to the IAM identity will fail\. 
For information about limits on the number of inline policies that you can embed in a user, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: List of [Policy](aws-properties-iam-policy-1.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iam-user-tags"></a>
A list of tags that you want to attach to the newly created user\. Each tag consists of a key name and an associated value\. For more information about tagging, see [Tagging IAM Identities](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html) in the *IAM User Guide*\.  
If any one of the tags is invalid or if you exceed the allowed number of tags per user, then the entire request fails and the user is not created\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-iam-user-username"></a>
The name of the user to create\. Do not include the path in this value\.  
This parameter allows \(per its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-\. The user name must be unique within the account\. User names are not distinguished by case\. For example, you cannot create users named both "John" and "john"\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the user name\.  
If you specify a name, you must specify the `CAPABILITY_NAMED_IAM` value to acknowledge your template's capabilities\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities)\.  
Naming an IAM resource can cause an unrecoverable error if you reuse the same template in multiple Regions\. To prevent this, we recommend using `Fn::Join` and `AWS::Region` to create a Region\-specific name, as in the following example: `{"Fn::Join": ["", [{"Ref": "AWS::Region"}, {"Ref": "MyResourceName"}]]}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-properties-iam-user-return-values"></a>

### Ref<a name="aws-properties-iam-user-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `UserName`\. For example: `mystack-myuser-1CCXAFG2H2U4D`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-iam-user-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-iam-user-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the specified `AWS::IAM::User` resource\. For example: `arn:aws:iam::123456789012:user/mystack-myuser-1CCXAFG2H2U4D`\.

## Examples<a name="aws-properties-iam-user--examples"></a>

### User<a name="aws-properties-iam-user--examples--User"></a>

In this example, create a user named "MyUser"\.

#### JSON<a name="aws-properties-iam-user--examples--User--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources" : {
     "MyUser" : {
       "Type" : "AWS::IAM::User",
       "Properties" : {
         "LoginProfile": {
           "Password": { "Ref" : "MyPassword" }
         }
       }
    }
  }
}
```

#### YAML<a name="aws-properties-iam-user--examples--User--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyUser:
    Type: AWS::IAM::User
    Properties:
      LoginProfile:
        Password:
          Ref: MyPassword
```

## See also<a name="aws-properties-iam-user--seealso"></a>
+ To view `AWS::IAM::User` template example snippets, see [Declaring an IAM User Resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html#scenario-iam-user)\. 
+  [CreateUser](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateUser.html) in the *AWS Identity and Access Management API Reference* 

