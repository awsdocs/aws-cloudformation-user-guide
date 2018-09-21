# Amazon Cognito IdentityPool PushSync<a name="aws-properties-cognito-identitypool-pushsync"></a>

`PushSync` is a property of the [AWS::Cognito::IdentityPool](aws-resource-cognito-identitypool.md) resource that defines the configuration options to be applied to an Amazon Cognito identity pool\.

## Syntax<a name="aws-properties-cognito-identitypool-pushsync-syntax"></a>

### JSON<a name="aws-properties-cognito-identitypool-pushsync-syntax.json"></a>

```
{
  "[ApplicationArns](#cfn-cognito-identitypool-pushsync-applicationarns)" : [ String, ... ],
  "[RoleArn](#cfn-cognito-identitypool-pushsync-rolearn)" : String
}
```

### YAML<a name="aws-properties-cognito-identitypool-pushsync-syntax.yaml"></a>

```
[ApplicationArns](#cfn-cognito-identitypool-pushsync-applicationarns): 
  - String
[RoleArn](#cfn-cognito-identitypool-pushsync-rolearn): String
```

## Properties<a name="aws-properties-cognito-identitypool-pushsync-properties"></a>

`ApplicationArns`  <a name="cfn-cognito-identitypool-pushsync-applicationarns"></a>
List of Amazon SNS platform application ARNs that could be used by clients\.  
*Type*: List of String values  
*Required*: No

`RoleArn`  <a name="cfn-cognito-identitypool-pushsync-rolearn"></a>
An IAM role configured to allow Amazon Cognito to call SNS on behalf of the developer\.  
*Type*: String  
*Required*: No