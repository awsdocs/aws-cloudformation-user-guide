# AWS::Cognito::UserPoolClient<a name="aws-resource-cognito-userpoolclient"></a>

The `AWS::Cognito::UserPoolClient` resource creates an Amazon Cognito user pool client\.


+ [Syntax](#aws-resource-cognito-userpoolclient-syntax)
+ [Properties](#w3ab2c21c10d254b9)
+ [Return Value](#w3ab2c21c10d254c11)

## Syntax<a name="aws-resource-cognito-userpoolclient-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolclient-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolClient",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-clientname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-explicitauthflows)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-generatesecret)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-readattributes)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-refreshtokenvalidity)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-userpoolid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-writeattributes)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-cognito-userpoolclient-syntax.yaml"></a>

```
Type: "AWS::Cognito::UserPoolClient"
Properties:
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-clientname): String,
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-explicitauthflows): 
      - String
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-generatesecret): Boolean
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-readattributes): 
      - String
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-refreshtokenvalidity): Integer
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-userpoolid): String
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpoolclient-writeattributes): 
      - String
```

## Properties<a name="w3ab2c21c10d254b9"></a>

`ClientName`  
The client name for the user pool client that you want to create\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption  
MinLength: 1  
MaxLength: 128

`ExplicitAuthFlows`  
The explicit authentication flows, which can be one of the following: `ADMIN_NO_SRP_AUTH` or `CUSTOM_AUTH_FLOW_ONLY`\.  
*Required: *No  
*Type*: List of Strings  
*Update requires*: No interruption

`GenerateSecret`  
Specifies whether you want to generate a secret for the user pool client being created\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`ReadAttributes`  
The read attributes\.  
*Required: *No  
*Type*: List of Strings  
*Update requires*: No interruption

`RefreshTokenValidity`  
The time limit, in days, after which the refresh token is no longer valid\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`UserPoolId`  
The user pool ID for the user pool where you want to create a client\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`WriteAttributes`  
The write attributes\.  
*Required: *No  
*Type*: List of Strings  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10d254c11"></a>

### Ref<a name="w3ab2c21c10d254c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the Amazon Cognito user pool client ID, such as `1h57kf5cpq17m0eml12EXAMPLE`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d254c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`ClientSecret`  
The client secret, as a `String`\.

`Name`  
The name of the user pool client, as a `String`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.