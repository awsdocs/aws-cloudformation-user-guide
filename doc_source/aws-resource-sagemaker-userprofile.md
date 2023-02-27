# AWS::SageMaker::UserProfile<a name="aws-resource-sagemaker-userprofile"></a>

Creates a user profile\. A user profile represents a single user within a domain, and is the main way to reference a "person" for the purposes of sharing, reporting, and other user\-oriented features\. This entity is created when a user onboards to Amazon SageMaker Studio\. If an administrator invites a person by email or imports them from IAM Identity Center, a user profile is automatically created\. A user profile is the primary holder of settings for an individual user and has a reference to the user's private Amazon Elastic File System \(EFS\) home directory\. 

**Note**  
If you're using IAM Identity Center authentication, a user in IAM Identity Center, or a group in IAM Identity Center containing that user, must be assigned to the Amazon SageMaker Studio application from the IAM Identity Center Console to create a user profile\. For more information about application assignment, see [Assign user access](singlesignon/latest/userguide/assignuserstoapp.html)\. After assignment is complete, a user profile can be created for that user in IAM Identity Center with AWS CloudFormation\. 

## Syntax<a name="aws-resource-sagemaker-userprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-userprofile-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::UserProfile",
  "Properties" : {
      "[DomainId](#cfn-sagemaker-userprofile-domainid)" : String,
      "[SingleSignOnUserIdentifier](#cfn-sagemaker-userprofile-singlesignonuseridentifier)" : String,
      "[SingleSignOnUserValue](#cfn-sagemaker-userprofile-singlesignonuservalue)" : String,
      "[Tags](#cfn-sagemaker-userprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserProfileName](#cfn-sagemaker-userprofile-userprofilename)" : String,
      "[UserSettings](#cfn-sagemaker-userprofile-usersettings)" : UserSettings
    }
}
```

### YAML<a name="aws-resource-sagemaker-userprofile-syntax.yaml"></a>

```
Type: AWS::SageMaker::UserProfile
Properties: 
  [DomainId](#cfn-sagemaker-userprofile-domainid): String
  [SingleSignOnUserIdentifier](#cfn-sagemaker-userprofile-singlesignonuseridentifier): String
  [SingleSignOnUserValue](#cfn-sagemaker-userprofile-singlesignonuservalue): String
  [Tags](#cfn-sagemaker-userprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserProfileName](#cfn-sagemaker-userprofile-userprofilename): String
  [UserSettings](#cfn-sagemaker-userprofile-usersettings): 
    UserSettings
```

## Properties<a name="aws-resource-sagemaker-userprofile-properties"></a>

`DomainId`  <a name="cfn-sagemaker-userprofile-domainid"></a>
The domain ID\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SingleSignOnUserIdentifier`  <a name="cfn-sagemaker-userprofile-singlesignonuseridentifier"></a>
A specifier for the type of value specified in SingleSignOnUserValue\. Currently, the only supported value is "UserName"\. If the Domain's AuthMode is IAM Identity Center, this field is required\. If the Domain's AuthMode is not IAM Identity Center, this field cannot be specified\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SingleSignOnUserValue`  <a name="cfn-sagemaker-userprofile-singlesignonuservalue"></a>
The username of the associated AWS Single Sign\-On User for this UserProfile\. If the Domain's AuthMode is IAM Identity Center, this field is required, and must match a valid username of a user in your directory\. If the Domain's AuthMode is not IAM Identity Center, this field cannot be specified\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-userprofile-tags"></a>
An array of key\-value pairs to apply to this resource\.  
Tags that you specify for the User Profile are also added to all apps that the User Profile launches\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserProfileName`  <a name="cfn-sagemaker-userprofile-userprofilename"></a>
The user profile name\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserSettings`  <a name="cfn-sagemaker-userprofile-usersettings"></a>
A collection of settings that apply to users of Amazon SageMaker Studio\.  
*Required*: No  
*Type*: [UserSettings](aws-properties-sagemaker-userprofile-usersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-userprofile-return-values"></a>

### Ref<a name="aws-resource-sagemaker-userprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Domain ID and the user profile name, such as `d-xxxxxxxxxxxx` and `my-user-profile`, respectively\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-userprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-sagemaker-userprofile-return-values-fn--getatt-fn--getatt"></a>

`UserProfileArn`  <a name="UserProfileArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the user profile, such as `arn:aws:sagemaker:us-west-2:account-id:user-profile/my-user-profile`\.