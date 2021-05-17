# AWS::Cognito::UserPoolUICustomizationAttachment<a name="aws-resource-cognito-userpooluicustomizationattachment"></a>

The `AWS::Cognito::UserPoolUICustomizationAttachment` resource sets the UI customization information for a user pool's built\-in app UI\.

You can specify app UI customization settings for a single client \(with a specific `clientId`\) or for all clients \(by setting the `clientId` to `ALL`\)\. If you specify `ALL`, the default configuration is used for every client that has had no UI customization set previously\. If you specify UI customization settings for a particular client, it no longer falls back to the `ALL` configuration\.

**Note**  
Before you create this resource, your user pool must have a domain associated with it\. You can create an `AWS::Cognito::UserPoolDomain` resource first in this user pool\.

Setting a logo image isn't supported from AWS CloudFormation\. Use the Amazon Cognito [SetUICustomization](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_SetUICustomization.html#API_SetUICustomization_RequestSyntax) API operation to set the image\.

## Syntax<a name="aws-resource-cognito-userpooluicustomizationattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpooluicustomizationattachment-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolUICustomizationAttachment",
  "Properties" : {
      "[ClientId](#cfn-cognito-userpooluicustomizationattachment-clientid)" : String,
      "[CSS](#cfn-cognito-userpooluicustomizationattachment-css)" : String,
      "[UserPoolId](#cfn-cognito-userpooluicustomizationattachment-userpoolid)" : String
    }
}
```

### YAML<a name="aws-resource-cognito-userpooluicustomizationattachment-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolUICustomizationAttachment
Properties: 
  [ClientId](#cfn-cognito-userpooluicustomizationattachment-clientid): String
  [CSS](#cfn-cognito-userpooluicustomizationattachment-css): String
  [UserPoolId](#cfn-cognito-userpooluicustomizationattachment-userpoolid): String
```

## Properties<a name="aws-resource-cognito-userpooluicustomizationattachment-properties"></a>

`ClientId`  <a name="cfn-cognito-userpooluicustomizationattachment-clientid"></a>
The client ID for the client app\. You can specify the UI customization settings for a single client \(with a specific clientId\) or for all clients \(by setting the clientId to `ALL`\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CSS`  <a name="cfn-cognito-userpooluicustomizationattachment-css"></a>
The CSS values in the UI customization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-cognito-userpooluicustomizationattachment-userpoolid"></a>
The user pool ID for the user pool\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cognito-userpooluicustomizationattachment-return-values"></a>

### Ref<a name="aws-resource-cognito-userpooluicustomizationattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the physicalResourceId, which is “UserPoolUICustomizationAttachment\-UserPoolId\-ClientId"\. For example:

 `{ "Ref": "UserPoolUICustomizationAttachment-us-east-1_FAKEPOOLID-2asc123fakeclientidajjulj6bh" }` 

For the Amazon Cognito user pool domain `UserPoolUICustomizationAttachment-us-east-1_FAKEPOOLID-2asc123fakeclientidajjulj6bh`, Ref returns the name of the UI customization attachment\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cognito-userpooluicustomizationattachment--examples"></a>



### Creating a new UI customization attachment for a user pool<a name="aws-resource-cognito-userpooluicustomizationattachment--examples--Creating_a_new_UI_customization_attachment_for_a_user_pool"></a>

The following example sets UI customization settings in the referenced user pool and client\.

#### JSON<a name="aws-resource-cognito-userpooluicustomizationattachment--examples--Creating_a_new_UI_customization_attachment_for_a_user_pool--json"></a>

```
{
   "UserPoolUICustomization":{
      "Type":"AWS::Cognito::UserPoolUICustomizationAttachment",
      "Properties":{
         "UserPoolId":{
            "Ref":"UserPool"
         },
         "ClientId":{
            "Ref":"Client"
         },
         "CSS":".banner-customizable {\nbackground:
        linear-gradient(#9940B8, #C27BDB)\n}"
      }
   }
}
```

#### YAML<a name="aws-resource-cognito-userpooluicustomizationattachment--examples--Creating_a_new_UI_customization_attachment_for_a_user_pool--yaml"></a>

```
UserPoolUICustomization: 
  Type: AWS::Cognito::UserPoolUICustomizationAttachment 
  Properties: 
    UserPoolId: !Ref UserPool
    ClientId: !Ref Client 
    CSS: ".banner-customizable { 
      background: linear-gradient(#9940B8, #C27BDB) 
    }"
```