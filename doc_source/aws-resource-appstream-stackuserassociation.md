# AWS::AppStream::StackUserAssociation<a name="aws-resource-appstream-stackuserassociation"></a>

The `AWS::AppStream::StackUserAssociation` resource associates the specified stacks with the specified users for Amazon AppStream 2\.0\. For more information, see [UserStackAssociation](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_UserStackAssociation.html) in the *Amazon AppStream 2\.0 API Reference*\. 

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
Type: "AWS::AppStream::StackUserAssociation"
Properties:
  [AuthenticationType](#cfn-appstream-stackuserassociation-authenticationtype): String
  [SendEmailNotification](#cfn-appstream-stackuserassociation-sendemailnotification): Boolean
  [StackName](#cfn-appstream-stackuserassociation-stackname): String
  [UserName](#cfn-appstream-stackuserassociation-username): String
```

## Properties<a name="aws-resource-appstream-stackuserassociation-properties"></a>

`AuthenticationType`  <a name="cfn-appstream-stackuserassociation-authenticationtype"></a>
The authentication type for the user\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SendEmailNotification`  <a name="cfn-appstream-stackuserassociation-sendemailnotification"></a>
Specifies whether a welcome email is sent to a user after the user is created in the user pool\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StackName`  <a name="cfn-appstream-stackuserassociation-stackname"></a>
The name of the stack\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`UserName`  <a name="cfn-appstream-stackuserassociation-username"></a>
The email address of the user\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-resource-appstream-stackuserassociation-seealso"></a>
+  [UserStackAssociation](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_UserStackAssociation.html) in the *Amazon AppStream 2\.0 API Reference* 