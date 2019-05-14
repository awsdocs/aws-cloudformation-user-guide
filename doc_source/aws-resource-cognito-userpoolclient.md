# AWS::Cognito::UserPoolClient<a name="aws-resource-cognito-userpoolclient"></a>

The `AWS::Cognito::UserPoolClient` resource creates an Amazon Cognito user pool client\.

## Syntax<a name="aws-resource-cognito-userpoolclient-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolclient-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolClient",
  "Properties" : {
      "[ClientName](#cfn-cognito-userpoolclient-clientname)" : String,
      "[ExplicitAuthFlows](#cfn-cognito-userpoolclient-explicitauthflows)" : [ String, ... ],
      "[GenerateSecret](#cfn-cognito-userpoolclient-generatesecret)" : Boolean,
      "[ReadAttributes](#cfn-cognito-userpoolclient-readattributes)" : [ String, ... ],
      "[RefreshTokenValidity](#cfn-cognito-userpoolclient-refreshtokenvalidity)" : Double,
      "[UserPoolId](#cfn-cognito-userpoolclient-userpoolid)" : String,
      "[WriteAttributes](#cfn-cognito-userpoolclient-writeattributes)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-cognito-userpoolclient-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolClient
Properties : 
﻿  [ClientName](#cfn-cognito-userpoolclient-clientname) : String
﻿  [ExplicitAuthFlows](#cfn-cognito-userpoolclient-explicitauthflows) : 
    - String
﻿  [GenerateSecret](#cfn-cognito-userpoolclient-generatesecret) : Boolean
﻿  [ReadAttributes](#cfn-cognito-userpoolclient-readattributes) : 
    - String
﻿  [RefreshTokenValidity](#cfn-cognito-userpoolclient-refreshtokenvalidity) : Double
﻿  [UserPoolId](#cfn-cognito-userpoolclient-userpoolid) : String
﻿  [WriteAttributes](#cfn-cognito-userpoolclient-writeattributes) : 
    - String
```

## Properties<a name="aws-resource-cognito-userpoolclient-properties"></a>

`ClientName`  <a name="cfn-cognito-userpoolclient-clientname"></a>
The client name for the user pool client you would like to create\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w\s+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExplicitAuthFlows`  <a name="cfn-cognito-userpoolclient-explicitauthflows"></a>
The explicit authentication flows, which can be one of the following: `ADMIN_NO_SRP_AUTH`, `CUSTOM_AUTH_FLOW_ONLY`, or `USER_PASSWORD_AUTH`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GenerateSecret`  <a name="cfn-cognito-userpoolclient-generatesecret"></a>
Boolean to specify whether you want to generate a secret for the user pool client being created\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReadAttributes`  <a name="cfn-cognito-userpoolclient-readattributes"></a>
The read attributes\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshTokenValidity`  <a name="cfn-cognito-userpoolclient-refreshtokenvalidity"></a>
The time limit, in days, after which the refresh token is no longer valid and cannot be used\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `3650`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-cognito-userpoolclient-userpoolid"></a>
The user pool ID for the user pool where you want to create a user pool client\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WriteAttributes`  <a name="cfn-cognito-userpoolclient-writeattributes"></a>
The user pool attributes that the app client can write to\.  
If your app client allows users to sign in through an identity provider, this array must include all attributes that are mapped to identity provider attributes\. Amazon Cognito updates mapped attributes when users sign in to your application through an identity provider\. If your app client lacks write access to a mapped attribute, Amazon Cognito throws an error when it attempts to update the attribute\. For more information, see [Specifying Identity Provider Attribute Mappings for Your User Pool](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools-specifying-attribute-mapping.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-cognito-userpoolclient-return-values"></a>

### Ref<a name="aws-resource-cognito-userpoolclient-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Cognito user pool client ID, such as `1h57kf5cpq17m0eml12EXAMPLE`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.