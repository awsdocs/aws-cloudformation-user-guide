# AWS::Cognito::IdentityPool CognitoStreams<a name="aws-properties-cognito-identitypool-cognitostreams"></a>

`CognitoStreams` is a property of the [AWS::Cognito::IdentityPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-identitypool.html) resource that defines configuration options for Amazon Cognito streams\.

## Syntax<a name="aws-properties-cognito-identitypool-cognitostreams-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamingStatus`  <a name="cfn-cognito-identitypool-cognitostreams-streamingstatus"></a>
Status of the Amazon Cognito streams\. Valid values are: `ENABLED` or `DISABLED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamName`  <a name="cfn-cognito-identitypool-cognitostreams-streamname"></a>
The name of the Amazon Cognito stream to receive updates\. This stream must be in the developer's account and in the same Region as the identity pool\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)