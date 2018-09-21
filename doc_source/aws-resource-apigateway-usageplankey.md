# AWS::ApiGateway::UsagePlanKey<a name="aws-resource-apigateway-usageplankey"></a>

The `AWS::ApiGateway::UsagePlanKey` resource associates an Amazon API Gateway API key with an API Gateway usage plan\. This association determines which users the usage plan is applied to\.

**Topics**
+ [Syntax](#aws-resource-apigateway-usageplankey-syntax)
+ [Properties](#aws-resource-apigateway-usageplankey-properties)
+ [Example](#aws-resource-apigateway-usageplankey-examples)

## Syntax<a name="aws-resource-apigateway-usageplankey-syntax"></a>

### JSON<a name="aws-resource-apigateway-usageplankey-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::UsagePlanKey",
  "Properties" : {
    "[KeyId](#cfn-apigateway-keyid)" : String,
    "[KeyType](#cfn-apigateway-keytype)" : String,
    "[UsagePlanId](#cfn-apigateway-usageplanid)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-usageplankey-syntax.yaml"></a>

```
Type: AWS::ApiGateway::UsagePlanKey
Properties:
  [KeyId](#cfn-apigateway-keyid): String
  [KeyType](#cfn-apigateway-keytype): String
  [UsagePlanId](#cfn-apigateway-usageplanid): String
```

## Properties<a name="aws-resource-apigateway-usageplankey-properties"></a>

`KeyId`  <a name="cfn-apigateway-keyid"></a>
The ID of the usage plan key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`KeyType`  <a name="cfn-apigateway-keytype"></a>
The type of usage plan key\. Currently, the valid key type is `API_KEY`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`UsagePlanId`  <a name="cfn-apigateway-usageplanid"></a>
The value of the usage plan key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Example<a name="aws-resource-apigateway-usageplankey-examples"></a>

### JSON<a name="aws-resource-apigateway-usageplankey-example.json"></a>

```
"usagePlanKey" : {
  "Type": "AWS::ApiGateway::UsagePlanKey",
  "Properties": {
    "KeyId" : {"Ref" : "myApiKey"},
    "KeyType" : "API_KEY",
    "UsagePlanId" : {"Ref" : "myUsagePlan"}
  }
}
```

### YAML<a name="aws-resource-apigateway-usageplankey-example.yaml"></a>

```
usagePlanKey:
  Type: AWS::ApiGateway::UsagePlanKey
  Properties : 
    KeyId: !Ref 'myApiKey'
    KeyType: API_KEY
    UsagePlanId: !Ref 'myUsagePlan'
```