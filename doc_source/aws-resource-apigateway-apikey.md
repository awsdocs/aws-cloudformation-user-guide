# AWS::ApiGateway::ApiKey<a name="aws-resource-apigateway-apikey"></a>

The `AWS::ApiGateway::ApiKey` resource creates a unique key that you can distribute to clients who are executing Amazon API Gateway \(API Gateway\) `Method` resources that require an API key\. To specify which API key clients must use, map the API key with the `RestApi` and `Stage` resources that include the methods that require a key\.

**Topics**
+ [Syntax](#aws-resource-apigateway-apikey-syntax)
+ [Properties](#w3ab2c21c10c17b9)
+ [Return Value](#aws-resource-apigateway-apikey-returnvalues)
+ [Examples](#aws-resource-apigateway-apikey-examples)
+ [See Also](#aws-resource-apigateway-apikey-seealso)

## Syntax<a name="aws-resource-apigateway-apikey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-apikey-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::ApiKey",
  "Properties" : {
    "[CustomerId](#cfn-apigateway-apikey-customerid)" : String,
    "[Description](#cfn-apigateway-apikey-description)" : String,
    "[Enabled](#cfn-apigateway-apikey-enabled)" : Boolean,
    "[GenerateDistinctId](#cfn-apigateway-apikey-generatedistinctid)" : Boolean,
    "[Name](#cfn-apigateway-apikey-name)" : String,
    "[StageKeys](#cfn-apigateway-apikey-stagekeys)" : [ [StageKey](aws-properties-apitgateway-apikey-stagekey.md), ... ]
  }
}
```

### YAML<a name="aws-resource-apigateway-apikey-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::ApiKey"
Properties: 
  [CustomerId](#cfn-apigateway-apikey-customerid): String
  [Description](#cfn-apigateway-apikey-description): String
  [Enabled](#cfn-apigateway-apikey-enabled): Boolean
  [GenerateDistinctId](#cfn-apigateway-apikey-generatedistinctid): Boolean
  [Name](#cfn-apigateway-apikey-name): String
  [StageKeys](#cfn-apigateway-apikey-stagekeys):
    - [StageKey](aws-properties-apitgateway-apikey-stagekey.md)
    - ...
```

## Properties<a name="w3ab2c21c10c17b9"></a>

`CustomerId`  <a name="cfn-apigateway-apikey-customerid"></a>
An AWS Marketplace customer identifier to use when integrating with the AWS SaaS Marketplace\.  
*Required: *No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-apigateway-apikey-description"></a>
A description of the purpose of the API key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Enabled`  <a name="cfn-apigateway-apikey-enabled"></a>
Indicates whether the API key can be used by clients\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`GenerateDistinctId`  <a name="cfn-apigateway-apikey-generatedistinctid"></a>
Specifies whether the key identifier is distinct from the created API key value\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-apigateway-apikey-name"></a>
A name for the API key\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the API key name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StageKeys`  <a name="cfn-apigateway-apikey-stagekeys"></a>
A list of stages to associate with this API key\.  
*Required*: No  
*Type*: List of [Amazon API Gateway ApiKey StageKey](aws-properties-apitgateway-apikey-stagekey.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-apigateway-apikey-returnvalues"></a>

### Ref<a name="aws-resource-apigateway-apikey-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the API key ID, such as `m2m1k7sybf`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-apigateway-apikey-examples"></a>

### <a name="aws-resource-apigateway-apikey-example2"></a>

The following example creates an API key and associates it with the `Test` stage of the `TestAPIDeployment` deployment\. To ensure that AWS CloudFormation creates the stage and deployment \(which are declared elsewhere in the same template\) before the API key, the example adds an explicit dependency on the deployment and stage\. Without this dependency, AWS CloudFormation might create the API key first, which would cause the association to fail because the deployment and stage wouldn't exist\.

#### JSON<a name="aws-resource-apigateway-apikey-example.json"></a>

```
"ApiKey": {
  "Type": "AWS::ApiGateway::ApiKey",
  "DependsOn": ["TestAPIDeployment", "Test"],
  "Properties": {
    "Name": "TestApiKey",
    "Description": "CloudFormation API Key V1",
    "Enabled": "true",
    "StageKeys": [{
      "RestApiId": { "Ref": "RestApi" },
      "StageName": "Test"
    }]
  }
}
```

#### YAML<a name="aws-resource-apigateway-apikey-example.yaml"></a>

```
ApiKey: 
  Type: "AWS::ApiGateway::ApiKey"
  DependsOn: 
    - "TestAPIDeployment"
    - "Test"
  Properties: 
    Name: "TestApiKey"
    Description: "CloudFormation API Key V1"
    Enabled: "true"
    StageKeys: 
      - RestApiId: 
          Ref: "RestApi"
        StageName: "Test"
```

### <a name="aws-resource-apigateway-apikey-example2"></a>

The following example creates an API key, and enables you to specify a customer ID and whether to create a distinct ID\.

#### JSON<a name="aws-resource-apigateway-apikey-example2.json"></a>

```
{
  "Parameters": {
    "apiKeyName": {
      "Type": "String"
    },
    "customerId": {
      "Type": "String"
    },
    "generateDistinctId": {
      "Type": "String"
    }
  },
  "Resources": {
    "ApiKey": {
      "Type": "AWS::ApiGateway::ApiKey",
      "Properties": {
        "CustomerId": {
          "Ref": "customerId"
        },
        "GenerateDistinctId": {
          "Ref": "generateDistinctId"
        },
        "Name": {
          "Ref": "apiKeyName"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-apikey-example2.yaml"></a>

```
Parameters:
  apiKeyName:
    Type: String
  customerId:
    Type: String
  generateDistinctId:
    Type: String
Resources:
  ApiKey:
    Type: AWS::ApiGateway::ApiKey
    Properties:
      CustomerId: !Ref customerId
      GenerateDistinctId: !Ref generateDistinctId
      Name: !Ref apiKeyName
```

## See Also<a name="aws-resource-apigateway-apikey-seealso"></a>
+ [ apikey:create](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/apikey-create/) operation in the *Amazon API Gateway REST API Reference*