# AWS::OpenSearchService::Domain CognitoOptions<a name="aws-properties-opensearchservice-domain-cognitooptions"></a>

Configures OpenSearch Service to use Amazon Cognito authentication for OpenSearch Dashboards\.

## Syntax<a name="aws-properties-opensearchservice-domain-cognitooptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-cognitooptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-opensearchservice-domain-cognitooptions-enabled)" : Boolean,
  "[IdentityPoolId](#cfn-opensearchservice-domain-cognitooptions-identitypoolid)" : String,
  "[RoleArn](#cfn-opensearchservice-domain-cognitooptions-rolearn)" : String,
  "[UserPoolId](#cfn-opensearchservice-domain-cognitooptions-userpoolid)" : String
}
```

### YAML<a name="aws-properties-opensearchservice-domain-cognitooptions-syntax.yaml"></a>

```
  [Enabled](#cfn-opensearchservice-domain-cognitooptions-enabled): Boolean
  [IdentityPoolId](#cfn-opensearchservice-domain-cognitooptions-identitypoolid): String
  [RoleArn](#cfn-opensearchservice-domain-cognitooptions-rolearn): String
  [UserPoolId](#cfn-opensearchservice-domain-cognitooptions-userpoolid): String
```

## Properties<a name="aws-properties-opensearchservice-domain-cognitooptions-properties"></a>

`Enabled`  <a name="cfn-opensearchservice-domain-cognitooptions-enabled"></a>
Whether to enable or disable Amazon Cognito authentication for OpenSearch Dashboards\. See [Amazon Cognito authentication for OpenSearch Dashboards](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cognito-auth.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityPoolId`  <a name="cfn-opensearchservice-domain-cognitooptions-identitypoolid"></a>
The Amazon Cognito identity pool ID that you want OpenSearch Service to use for OpenSearch Dashboards authentication\.  
Required if you enabled Cognito Authentication for OpenSearch Dashboards\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+:[0-9a-f-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-opensearchservice-domain-cognitooptions-rolearn"></a>
The `AmazonOpenSearchServiceCognitoAccess` role that allows OpenSearch Service to configure your user pool and identity pool\.  
Required if you enabled Cognito Authentication for OpenSearch Dashboards\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:(aws|aws\-cn|aws\-us\-gov|aws\-iso|aws\-iso\-b):iam::[0-9]+:role\/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-opensearchservice-domain-cognitooptions-userpoolid"></a>
The Amazon Cognito user pool ID that you want OpenSearch Service to use for OpenSearch Dashboards authentication\.  
Required if you enabled Cognito Authentication for OpenSearch Dashboards\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)