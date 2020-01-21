# AWS::Elasticsearch::Domain CognitoOptions<a name="aws-properties-elasticsearch-domain-cognitooptions"></a>

Configures Amazon ES to use Amazon Cognito authentication for Kibana\.

## Syntax<a name="aws-properties-elasticsearch-domain-cognitooptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-cognitooptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-elasticsearch-domain-cognitooptions-enabled)" : Boolean,
  "[IdentityPoolId](#cfn-elasticsearch-domain-cognitooptions-identitypoolid)" : String,
  "[RoleArn](#cfn-elasticsearch-domain-cognitooptions-rolearn)" : String,
  "[UserPoolId](#cfn-elasticsearch-domain-cognitooptions-userpoolid)" : String
}
```

### YAML<a name="aws-properties-elasticsearch-domain-cognitooptions-syntax.yaml"></a>

```
  [Enabled](#cfn-elasticsearch-domain-cognitooptions-enabled): Boolean
  [IdentityPoolId](#cfn-elasticsearch-domain-cognitooptions-identitypoolid): String
  [RoleArn](#cfn-elasticsearch-domain-cognitooptions-rolearn): String
  [UserPoolId](#cfn-elasticsearch-domain-cognitooptions-userpoolid): String
```

## Properties<a name="aws-properties-elasticsearch-domain-cognitooptions-properties"></a>

`Enabled`  <a name="cfn-elasticsearch-domain-cognitooptions-enabled"></a>
Whether to enable or disable Amazon Cognito authentication for Kibana\. See [Amazon Cognito Authentication for Kibana](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-cognito-auth.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityPoolId`  <a name="cfn-elasticsearch-domain-cognitooptions-identitypoolid"></a>
The Amazon Cognito identity pool ID that you want Amazon ES to use for Kibana authentication\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-elasticsearch-domain-cognitooptions-rolearn"></a>
The `AmazonESCognitoAccess` role that allows Amazon ES to configure your user pool and identity pool\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-elasticsearch-domain-cognitooptions-userpoolid"></a>
The Amazon Cognito user pool ID that you want Amazon ES to use for Kibana authentication\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)