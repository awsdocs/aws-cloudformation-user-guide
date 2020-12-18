# AWS::IAM::InstanceProfile<a name="aws-resource-iam-instanceprofile"></a>

 Creates a new instance profile\. For information about instance profiles, go to [About Instance Profiles](https://docs.aws.amazon.com/IAM/latest/UserGuide/AboutInstanceProfiles.html)\.

 For information about the number of instance profiles you can create, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-instanceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-instanceprofile-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::InstanceProfile",
  "Properties" : {
      "[InstanceProfileName](#cfn-iam-instanceprofile-instanceprofilename)" : String,
      "[Path](#cfn-iam-instanceprofile-path)" : String,
      "[Roles](#cfn-iam-instanceprofile-roles)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-iam-instanceprofile-syntax.yaml"></a>

```
Type: AWS::IAM::InstanceProfile
Properties: 
  [InstanceProfileName](#cfn-iam-instanceprofile-instanceprofilename): String
  [Path](#cfn-iam-instanceprofile-path): String
  [Roles](#cfn-iam-instanceprofile-roles): 
    - String
```

## Properties<a name="aws-resource-iam-instanceprofile-properties"></a>

`InstanceProfileName`  <a name="cfn-iam-instanceprofile-instanceprofilename"></a>
The name of the instance profile to create\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Path`  <a name="cfn-iam-instanceprofile-path"></a>
 The path to the instance profile\. For more information about paths, see [IAM Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
This parameter is optional\. If it is not included, it defaults to a slash \(/\)\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of either a forward slash \(/\) by itself or a string that must begin and end with forward slashes\. In addition, it can contain any ASCII character from the \! \(`\u0021`\) through the DEL character \(`\u007F`\), including most punctuation characters, digits, and upper and lowercased letters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `(\u002F)|(\u002F[\u0021-\u007F]+\u002F)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Roles`  <a name="cfn-iam-instanceprofile-roles"></a>
The name of the role to associate with the instance profile\. Only one role can be assigned to an EC2 instance at a time, and all applications on the instance share the same role and permissions\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iam-instanceprofile-return-values"></a>

### Ref<a name="aws-resource-iam-instanceprofile-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "MyProfile" }` 

For the `AWS::IAM::InstanceProfile` resource with the logical ID `MyProfile`, Ref returns the name of the instance profile\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iam-instanceprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iam-instanceprofile-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the instance profile\. For example:  
 `{"Fn::GetAtt" : ["MyProfile", "Arn"] }`   
This returns a value such as `arn:aws:iam::1234567890:instance-profile/MyProfile-ASDNSDLKJ`\.

## Examples<a name="aws-resource-iam-instanceprofile--examples"></a>

### IAM Instance Profile<a name="aws-resource-iam-instanceprofile--examples--IAM_Instance_Profile"></a>

In this example, the InstanceProfile resource refers to the role by specifying its name, "MyRole"\.

#### JSON<a name="aws-resource-iam-instanceprofile--examples--IAM_Instance_Profile--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyInstanceProfile": {
         "Type": "AWS::IAM::InstanceProfile",
         "Properties": {
            "Path": "/",
            "Roles": [ {
               "Ref": "MyRole"
            } ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-iam-instanceprofile--examples--IAM_Instance_Profile--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MyInstanceProfile: 
    Type: "AWS::IAM::InstanceProfile"
    Properties: 
      Path: "/"
      Roles: 
        - 
          Ref: "MyRole"
```

## See also<a name="aws-resource-iam-instanceprofile--seealso"></a>
+  [CreateInstanceProfile](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateInstanceProfile.html) in the *AWS Identity and Access Management API Reference* 

