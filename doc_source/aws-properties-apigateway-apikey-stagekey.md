# AWS::ApiGateway::ApiKey StageKey<a name="aws-properties-apigateway-apikey-stagekey"></a>

`StageKey` is a property of the [AWS::ApiGateway::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-apikey.html) resource that specifies the stage to associate with the API key\. This association allows only clients with the key to make requests to methods in that stage\.

## Syntax<a name="aws-properties-apigateway-apikey-stagekey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-apikey-stagekey-syntax.json"></a>

```
{
  "[RestApiId](#cfn-apigateway-apikey-stagekey-restapiid)" : String,
  "[StageName](#cfn-apigateway-apikey-stagekey-stagename)" : String
}
```

### YAML<a name="aws-properties-apigateway-apikey-stagekey-syntax.yaml"></a>

```
  [RestApiId](#cfn-apigateway-apikey-stagekey-restapiid): String
  [StageName](#cfn-apigateway-apikey-stagekey-stagename): String
```

## Properties<a name="aws-properties-apigateway-apikey-stagekey-properties"></a>

`RestApiId`  <a name="cfn-apigateway-apikey-stagekey-restapiid"></a>
The string identifier of the associated RestApi\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageName`  <a name="cfn-apigateway-apikey-stagekey-stagename"></a>
The stage name associated with the stage key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-apikey-stagekey--seealso"></a>
+ [stageKeys](https://docs.aws.amazon.com/apigateway/latest/api/API_CreateApiKey.html#stageKeys) in the *Amazon API Gateway REST API Reference*

