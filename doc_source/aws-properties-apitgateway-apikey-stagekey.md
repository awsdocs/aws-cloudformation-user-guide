# Amazon API Gateway ApiKey StageKey<a name="aws-properties-apitgateway-apikey-stagekey"></a>

`StageKey` is a property of the [AWS::ApiGateway::ApiKey](aws-resource-apigateway-apikey.md) resource that specifies the Amazon API Gateway \(API Gateway\) stage to associate with the API key\. This association allows only clients with the key to make requests to methods in that stage\.

## Syntax<a name="aws-properties-apitgateway-apikey-stagekey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apitgateway-apikey-stagekey-syntax.json"></a>

```
{
  "[RestApiId](#cfn-apigateway-apikey-stagekey-restapiid)" : String,
  "[StageName](#cfn-apigateway-apikey-stagekey-stagename)" : String
}
```

### YAML<a name="aws-properties-apitgateway-apikey-stagekey-syntax.yaml"></a>

```
[RestApiId](#cfn-apigateway-apikey-stagekey-restapiid): String
[StageName](#cfn-apigateway-apikey-stagekey-stagename): String
```

## Properties<a name="w3ab2c21c14c13b7"></a>

`RestApiId`  <a name="cfn-apigateway-apikey-stagekey-restapiid"></a>
The ID of a `RestApi` resource that includes the stage with which you want to associate the API key\.  
*Required*: No  
*Type*: String

`StageName`  <a name="cfn-apigateway-apikey-stagekey-stagename"></a>
The name of the stage with which to associate the API key\. The stage must be included in the `RestApi` resource that you specified in the `RestApiId` property\.  
*Required*: No  
*Type*: String