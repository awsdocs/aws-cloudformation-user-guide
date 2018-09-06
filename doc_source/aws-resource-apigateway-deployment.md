# AWS::ApiGateway::Deployment<a name="aws-resource-apigateway-deployment"></a>

The `AWS::ApiGateway::Deployment` resource deploys an Amazon API Gateway \(API Gateway\) `[RestApi](aws-resource-apigateway-restapi.md)` resource to a stage so that clients can call the API over the Internet\. The stage acts as an environment\.

**Topics**
+ [Syntax](#aws-resource-apigateway-deployment-syntax)
+ [Properties](#w3ab2c21c10c35b9)
+ [Return Value](#w3ab2c21c10c35c11)
+ [Examples](#aws-resource-apigateway-deployment-examples)

## Syntax<a name="aws-resource-apigateway-deployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-deployment-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Deployment",
  "Properties" : {
    "[Description](#cfn-apigateway-deployment-description)" : String,
    "[RestApiId](#cfn-apigateway-deployment-restapiid)" : String,
    "[StageDescription](#cfn-apigateway-deployment-stagedescription)" : [StageDescription](aws-properties-apigateway-deployment-stagedescription.md),
    "[StageName](#cfn-apigateway-deployment-stagename)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-deployment-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::Deployment"
Properties:
  [Description](#cfn-apigateway-deployment-description): String
  [RestApiId](#cfn-apigateway-deployment-restapiid): String
  [StageDescription](#cfn-apigateway-deployment-stagedescription): [StageDescription](aws-properties-apigateway-deployment-stagedescription.md)
  [StageName](#cfn-apigateway-deployment-stagename): String
```

## Properties<a name="w3ab2c21c10c35b9"></a>

`Description`  <a name="cfn-apigateway-deployment-description"></a>
A description of the purpose of the API Gateway deployment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-deployment-restapiid"></a>
The ID of the [RestApi](aws-resource-apigateway-restapi.md) resource to deploy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StageDescription`  <a name="cfn-apigateway-deployment-stagedescription"></a>
Configures the stage that API Gateway creates with this deployment\.  
*Required*: No  
*Type*: [Amazon API Gateway Deployment StageDescription](aws-properties-apigateway-deployment-stagedescription.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StageName`  <a name="cfn-apigateway-deployment-stagename"></a>
A name for the stage that API Gateway creates with this deployment\. Use only alphanumeric characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10c35c11"></a>

### Ref<a name="w3ab2c21c10c35c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the deployment ID, such as `123abc`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-apigateway-deployment-examples"></a>

The following sections provide examples for declaring API Gateway deployments\.

### Deployment with an Empty Embedded Stage<a name="w3ab2c21c10c35c13b4"></a>

The following example deploys the `MyApi` API to a stage named `DummyStage`\.

#### JSON<a name="aws-resource-apigateway-deployment-example1.json"></a>

```
"Deployment": {
  "Type": "AWS::ApiGateway::Deployment",
  "Properties": {
    "RestApiId": { "Ref": "MyApi" },
    "Description": "My deployment",
    "StageName": "DummyStage"
  }
}
```

#### YAML<a name="aws-resource-apigateway-deployment-example1.yaml"></a>

```
Deployment: 
  Type: "AWS::ApiGateway::Deployment"
  Properties: 
    RestApiId: 
      Ref: "MyApi"
    Description: "My deployment"
    StageName: "DummyStage"
```

### `AWS::ApiGateway::Method` Dependency<a name="w3ab2c21c10c35c13b6"></a>

If you create a `AWS::ApiGateway::RestApi` resource and its methods \(using `AWS::ApiGateway::Method`\) in the same template as your deployment, the deployment must depend on the `RestApi`'s methods\. To create a dependency, add a `DependsOn` attribute to the deployment\. If you don't, AWS CloudFormation creates the deployment right after it creates the `RestApi` resource that doesn't contain any methods, and AWS CloudFormation encounters the following error: `The REST API doesn't contain any methods`\.

#### JSON<a name="aws-resource-apigateway-deployment-example2.json"></a>

```
"Deployment": {
  "DependsOn": "MyMethod",
  "Type": "AWS::ApiGateway::Deployment",
  "Properties": {
    "RestApiId": { "Ref": "MyApi" },
    "Description": "My deployment",
    "StageName": "DummyStage"
  }
}
```

#### YAML<a name="aws-resource-apigateway-deployment-example2.yaml"></a>

```
Deployment: 
  DependsOn: "MyMethod"
  Type: "AWS::ApiGateway::Deployment"
  Properties: 
    RestApiId: 
      Ref: "MyApi"
    Description: "My deployment"
    StageName: "DummyStage"
```