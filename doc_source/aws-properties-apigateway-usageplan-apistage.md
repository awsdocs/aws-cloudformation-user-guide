# Amazon API Gateway UsagePlan ApiStage<a name="aws-properties-apigateway-usageplan-apistage"></a>

`ApiStage` is a property of the [AWS::ApiGateway::UsagePlan](aws-resource-apigateway-usageplan.md) resource that specifies which Amazon API Gateway \(API Gateway\) stages and APIs to associate with a usage plan\.

## Syntax<a name="aws-properties-apigateway-usageplan-apistage-syntax"></a>

### JSON<a name="aws-properties-apigateway-usageplan-apistage-syntax.json"></a>

```
{
  "[ApiId](#cfn-apigateway-usageplan-apistage-apiid)" : String,
  "[Stage](#cfn-apigateway-usageplan-apistage-stage)" : String
}
```

### YAML<a name="aws-properties-apigateway-usageplan-apistage-syntax.yaml"></a>

```
[ApiId](#cfn-apigateway-usageplan-apistage-apiid): String
[Stage](#cfn-apigateway-usageplan-apistage-stage): String
```

## Properties<a name="aws-properties-apigateway-usageplan-apistage-properties"></a>

`ApiId`  <a name="cfn-apigateway-usageplan-apistage-apiid"></a>
The ID of an API that is in the specified `Stage` property that you want to associate with the usage plan\.  
*Required*: No  
*Type*: String

`Stage`  <a name="cfn-apigateway-usageplan-apistage-stage"></a>
The name of an API Gateway stage to associate with the usage plan\.  
*Required*: No  
*Type*: String