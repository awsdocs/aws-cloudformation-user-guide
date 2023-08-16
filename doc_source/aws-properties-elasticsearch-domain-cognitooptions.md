# AWS::Elasticsearch::Domain CognitoOptions<a name="aws-properties-elasticsearch-domain-cognitooptions"></a>

Configures OpenSearch Service to use Amazon Cognito authentication for OpenSearch Dashboards\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

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
Whether to enable or disable Amazon Cognito authentication for OpenSearch Dashboards\. See [Amazon Cognito authentication for OpenSearch Dashboards](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cognito-auth.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityPoolId`  <a name="cfn-elasticsearch-domain-cognitooptions-identitypoolid"></a>
The Amazon Cognito identity pool ID that you want OpenSearch Service to use for OpenSearch Dashboards authentication\. Required if you enable Cognito authentication\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-elasticsearch-domain-cognitooptions-rolearn"></a>
The `AmazonESCognitoAccess` role that allows OpenSearch Service to configure your user pool and identity pool\. Required if you enable Cognito authentication\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-elasticsearch-domain-cognitooptions-userpoolid"></a>
The Amazon Cognito user pool ID that you want OpenSearch Service to use for OpenSearch Dashboards authentication\. Required if you enable Cognito authentication\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)