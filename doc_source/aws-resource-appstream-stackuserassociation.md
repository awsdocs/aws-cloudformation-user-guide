# AWS::AppStream::StackUserAssociation<a name="aws-resource-appstream-stackuserassociation"></a>

The `AWS::AppStream::StackUserAssociation` resource associates the specified users with the specified stacks for Amazon AppStream 2\.0\. Users in an AppStream 2\.0 user pool cannot be assigned to stacks with fleets that are joined to an Active Directory domain\.

## Syntax<a name="aws-resource-appstream-stackuserassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-stackuserassociation-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::StackUserAssociation",
  "Properties" : {
      "[AuthenticationType](#cfn-appstream-stackuserassociation-authenticationtype)" : String,
      "[SendEmailNotification](#cfn-appstream-stackuserassociation-sendemailnotification)" : Boolean,
      "[StackName](#cfn-appstream-stackuserassociation-stackname)" : String,
      "[UserName](#cfn-appstream-stackuserassociation-username)" : String
    }
}
```

### YAML<a name="aws-resource-appstream-stackuserassociation-syntax.yaml"></a>

```
Type: AWS::AppStream::StackUserAssociation
Properties: 
  [AuthenticationType](#cfn-appstream-stackuserassociation-authenticationtype): String
  [SendEmailNotification](#cfn-appstream-stackuserassociation-sendemailnotification): Boolean
  [StackName](#cfn-appstream-stackuserassociation-stackname): String
  [UserName](#cfn-appstream-stackuserassociation-username): String
```

## Properties<a name="aws-resource-appstream-stackuserassociation-properties"></a>

`AuthenticationType`  <a name="cfn-appstream-stackuserassociation-authenticationtype"></a>
The authentication type for the user who is associated with the stack\. You must specify USERPOOL\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `API | SAML | USERPOOL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SendEmailNotification`  <a name="cfn-appstream-stackuserassociation-sendemailnotification"></a>
Specifies whether a welcome email is sent to a user after the user is created in the user pool\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StackName`  <a name="cfn-appstream-stackuserassociation-stackname"></a>
The name of the stack that is associated with the user\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserName`  <a name="cfn-appstream-stackuserassociation-username"></a>
The email address of the user who is associated with the stack\.  
Users' email addresses are case\-sensitive\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-resource-appstream-stackuserassociation--seealso"></a>
+  [BatchAssociateUserStack](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_BatchAssociateUserStack.html) in the *Amazon AppStream 2\.0 API Reference* 

