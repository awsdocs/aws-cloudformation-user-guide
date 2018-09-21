# Amazon Cognito IdentityPool CognitoStreams<a name="aws-properties-cognito-identitypool-cognitostreams"></a>

`CognitoStreams` is a property of the [AWS::Cognito::IdentityPool](aws-resource-cognito-identitypool.md) resource that defines configuration options for Amazon Cognito streams\.

## Syntax<a name="aws-properties-cognito-identitypool-cognitostreams-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypool-cognitostreams-syntax.json"></a>

```
{
  "[RoleArn](#cfn-cognito-identitypool-cognitostreams-rolearn)" : String,
  "[StreamingStatus](#cfn-cognito-identitypool-cognitostreams-streamingstatus)" : String,
  "[StreamName](#cfn-cognito-identitypool-cognitostreams-streamname)" : String
}
```

### YAML<a name="aws-properties-cognito-identitypool-cognitostreams-syntax.yaml"></a>

```
[RoleArn](#cfn-cognito-identitypool-cognitostreams-rolearn): String
[StreamingStatus](#cfn-cognito-identitypool-cognitostreams-streamingstatus): String
[StreamName](#cfn-cognito-identitypool-cognitostreams-streamname): String
```

## Properties<a name="aws-properties-cognito-identitypool-cognitostreams-properties"></a>

`RoleArn`  <a name="cfn-cognito-identitypool-cognitostreams-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role Amazon Cognito can assume to publish to the stream\. This role must grant access to Amazon Cognito \(cognito\-sync\) to invoke `PutRecord` on your Amazon Cognito stream\.  
*Type*: String  
*Required*: No

`StreamingStatus`  <a name="cfn-cognito-identitypool-cognitostreams-streamingstatus"></a>
Status of the Cognito streams\. Valid values are: `ENABLED` or `DISABLED`\.  
*Type*: String  
*Required*: No

`StreamName`  <a name="cfn-cognito-identitypool-cognitostreams-streamname"></a>
The name of the Amazon Cognito stream to receive updates\. This stream must be in the developer's account and in the same region as the identity pool\.  
*Type*: String  
*Required*: No