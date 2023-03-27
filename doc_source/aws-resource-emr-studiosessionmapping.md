# AWS::EMR::StudioSessionMapping<a name="aws-resource-emr-studiosessionmapping"></a>

The `AWS::EMR::StudioSessionMapping` resource is an Amazon EMR resource type that maps a user or group to the Amazon EMR Studio specified by `StudioId`, and applies a session policy that defines Studio permissions for that user or group\.

## Syntax<a name="aws-resource-emr-studiosessionmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-studiosessionmapping-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::StudioSessionMapping",
  "Properties" : {
      "[IdentityName](#cfn-emr-studiosessionmapping-identityname)" : String,
      "[IdentityType](#cfn-emr-studiosessionmapping-identitytype)" : String,
      "[SessionPolicyArn](#cfn-emr-studiosessionmapping-sessionpolicyarn)" : String,
      "[StudioId](#cfn-emr-studiosessionmapping-studioid)" : String
    }
}
```

### YAML<a name="aws-resource-emr-studiosessionmapping-syntax.yaml"></a>

```
Type: AWS::EMR::StudioSessionMapping
Properties: 
  [IdentityName](#cfn-emr-studiosessionmapping-identityname): String
  [IdentityType](#cfn-emr-studiosessionmapping-identitytype): String
  [SessionPolicyArn](#cfn-emr-studiosessionmapping-sessionpolicyarn): String
  [StudioId](#cfn-emr-studiosessionmapping-studioid): String
```

## Properties<a name="aws-resource-emr-studiosessionmapping-properties"></a>

`IdentityName`  <a name="cfn-emr-studiosessionmapping-identityname"></a>
The name of the user or group\. For more information, see [UserName](https://docs.aws.amazon.com/singlesignon/latest/IdentityStoreAPIReference/API_User.html#singlesignon-Type-User-UserName) and [DisplayName](https://docs.aws.amazon.com/singlesignon/latest/IdentityStoreAPIReference/API_Group.html#singlesignon-Type-Group-DisplayName) in the *IAM Identity Center Identity Store API Reference*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IdentityType`  <a name="cfn-emr-studiosessionmapping-identitytype"></a>
Specifies whether the identity to map to the Amazon EMR Studio is a user or a group\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `GROUP | USER`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SessionPolicyArn`  <a name="cfn-emr-studiosessionmapping-sessionpolicyarn"></a>
The Amazon Resource Name \(ARN\) for the session policy that will be applied to the user or group\. Session policies refine Studio user permissions without the need to use multiple IAM user roles\. For more information, see [Create an EMR Studio user role with session policies](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-studio-user-role.html) in the *Amazon EMR Management Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StudioId`  <a name="cfn-emr-studiosessionmapping-studioid"></a>
The ID of the Amazon EMR Studio to which the user or group will be mapped\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)