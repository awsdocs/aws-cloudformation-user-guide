# AWS::ApiGatewayV2::Deployment<a name="aws-resource-apigatewayv2-deployment"></a>

The `AWS::ApiGatewayV2::Deployment` resource creates a deployment for an API\.

## Syntax<a name="aws-resource-apigatewayv2-deployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-deployment-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Deployment",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-deployment-apiid)" : String,
      "[Description](#cfn-apigatewayv2-deployment-description)" : String,
      "[StageName](#cfn-apigatewayv2-deployment-stagename)" : String
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-deployment-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::Deployment
Properties: 
  [ApiId](#cfn-apigatewayv2-deployment-apiid): String
  [Description](#cfn-apigatewayv2-deployment-description): String
  [StageName](#cfn-apigatewayv2-deployment-stagename): String
```

## Properties<a name="aws-resource-apigatewayv2-deployment-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-deployment-apiid"></a>
The API identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-apigatewayv2-deployment-description"></a>
The description for the deployment resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageName`  <a name="cfn-apigatewayv2-deployment-stagename"></a>
The name of an existing stage to associate with the deployment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-deployment-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-deployment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the deployment ID, such as `123abc`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-deployment--examples"></a>



### Deployment creation example<a name="aws-resource-apigatewayv2-deployment--examples--Deployment_creation_example"></a>

The following example creates a `deployment` resource for the `MyApi` API, which has the `MyRoute` route defined\.

#### JSON<a name="aws-resource-apigatewayv2-deployment--examples--Deployment_creation_example--json"></a>

```
{
    "Deployment": {
        "Type": "AWS::ApiGatewayV2::Deployment",
        "DependsOn": [
            "MyRoute"
        ],
        "Properties": {
            "Description": "My deployment",
            "ApiId": {
                "Ref": "MyApi"
            },
            "StageName": "Beta"
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-deployment--examples--Deployment_creation_example--yaml"></a>

```
Deployment:
  Type: 'AWS::ApiGatewayV2::Deployment'
  DependsOn:
    - MyRoute
  Properties:
    Description: My deployment
    ApiId: !Ref MyApi
    StageName: Beta
```

## See also<a name="aws-resource-apigatewayv2-deployment--seealso"></a>
+ [CreateDeployment](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-deployments.html#CreateDeployment) in the *Amazon API Gateway Version 2 API Reference*

