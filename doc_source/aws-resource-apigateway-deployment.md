# AWS::ApiGateway::Deployment<a name="aws-resource-apigateway-deployment"></a>

The `AWS::ApiGateway::Deployment` resource deploys an API Gateway `RestApi` resource to a stage so that clients can call the API over the internet\. The stage acts as an environment\.

## Syntax<a name="aws-resource-apigateway-deployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-deployment-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Deployment",
  "Properties" : {
      "[DeploymentCanarySettings](#cfn-apigateway-deployment-deploymentcanarysettings)" : DeploymentCanarySettings,
      "[Description](#cfn-apigateway-deployment-description)" : String,
      "[RestApiId](#cfn-apigateway-deployment-restapiid)" : String,
      "[StageDescription](#cfn-apigateway-deployment-stagedescription)" : StageDescription,
      "[StageName](#cfn-apigateway-deployment-stagename)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-deployment-syntax.yaml"></a>

```
Type: AWS::ApiGateway::Deployment
Properties: 
  [DeploymentCanarySettings](#cfn-apigateway-deployment-deploymentcanarysettings): 
    DeploymentCanarySettings
  [Description](#cfn-apigateway-deployment-description): String
  [RestApiId](#cfn-apigateway-deployment-restapiid): String
  [StageDescription](#cfn-apigateway-deployment-stagedescription): 
    StageDescription
  [StageName](#cfn-apigateway-deployment-stagename): String
```

## Properties<a name="aws-resource-apigateway-deployment-properties"></a>

`DeploymentCanarySettings`  <a name="cfn-apigateway-deployment-deploymentcanarysettings"></a>
Specifies settings for the canary deployment\.  
*Required*: No  
*Type*: [DeploymentCanarySettings](aws-properties-apigateway-deployment-deploymentcanarysettings.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-apigateway-deployment-description"></a>
A description of the purpose of the API Gateway deployment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-deployment-restapiid"></a>
The ID of the `RestApi` resource to deploy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StageDescription`  <a name="cfn-apigateway-deployment-stagedescription"></a>
Configures the stage that API Gateway creates with this deployment\.  
*Required*: No  
*Type*: [StageDescription](aws-properties-apigateway-deployment-stagedescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageName`  <a name="cfn-apigateway-deployment-stagename"></a>
A name for the stage that API Gateway creates with this deployment\. Use only alphanumeric characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-deployment-return-values"></a>

### Ref<a name="aws-resource-apigateway-deployment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the deployment ID, such as `123abc`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-deployment--examples"></a>

The following sections provide examples for declaring API Gateway deployments\.

### Deployment with an empty embedded stage<a name="aws-resource-apigateway-deployment--examples--Deployment_with_an_empty_embedded_stage"></a>

The following example deploys the `MyApi` API to a stage named `DummyStage`\.

#### JSON<a name="aws-resource-apigateway-deployment--examples--Deployment_with_an_empty_embedded_stage--json"></a>

```
{
    "Deployment": {
        "Type": "AWS::ApiGateway::Deployment",
        "Properties": {
            "RestApiId": {
                "Ref": "MyApi"
            },
            "Description": "My deployment",
            "StageName": "DummyStage"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-deployment--examples--Deployment_with_an_empty_embedded_stage--yaml"></a>

```
Deployment:
  Type: 'AWS::ApiGateway::Deployment'
  Properties:
    RestApiId: !Ref MyApi
    Description: My deployment
    StageName: DummyStage
```

### AWS::ApiGateway::Method Dependency<a name="aws-resource-apigateway-deployment--examples--AWS::ApiGateway::Method_Dependency"></a>

If you create an [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html) resource and its methods \(using [AWS::ApiGateway::Method](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-method.html)\) in the same template as your deployment, the deployment must depend on the `RestApi`'s methods\. To create a dependency, add a `DependsOn` attribute to the deployment\. If you don't, AWS CloudFormation creates the deployment right after it creates the `RestApi` resource that doesn't contain any methods, and AWS CloudFormation encounters the following error: `The REST API doesn't contain any methods`\.

#### JSON<a name="aws-resource-apigateway-deployment--examples--AWS::ApiGateway::Method_Dependency--json"></a>

```
{
    "Deployment": {
        "DependsOn": "MyMethod",
        "Type": "AWS::ApiGateway::Deployment",
        "Properties": {
            "RestApiId": {
                "Ref": "MyApi"
            },
            "Description": "My deployment",
            "StageName": "DummyStage"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-deployment--examples--AWS::ApiGateway::Method_Dependency--yaml"></a>

```
Deployment:
  DependsOn: MyMethod
  Type: 'AWS::ApiGateway::Deployment'
  Properties:
    RestApiId: !Ref MyApi
    Description: My deployment
    StageName: DummyStage
```

## See also<a name="aws-resource-apigateway-deployment--seealso"></a>
+ [deployment:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/deployment-create/) in the *Amazon API Gateway REST API Reference*

