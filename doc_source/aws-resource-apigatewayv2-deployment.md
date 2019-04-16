# AWS::ApiGatewayV2::Deployment<a name="aws-resource-apigatewayv2-deployment"></a>

The `AWS::ApiGatewayV2::Deployment` resource represents a deployment for an API\. For more information, see [CreateDeployment](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-deployments.html#CreateDeployment) in the *Amazon API Gateway V2 API Reference*\. 

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
Type: "AWS::ApiGatewayV2::Deployment"
Properties:
  [ApiId](#cfn-apigatewayv2-deployment-apiid): String
  [Description](#cfn-apigatewayv2-deployment-description): String
  [StageName](#cfn-apigatewayv2-deployment-stagename): String
```

## Properties<a name="aws-resource-apigatewayv2-deployment-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-deployment-apiid"></a>
The ID of the [Api](aws-resource-apigatewayv2-api.md) resource to deploy\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Description`  <a name="cfn-apigatewayv2-deployment-description"></a>
Describes the stage that API Gateway creates with this deployment\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StageName`  <a name="cfn-apigatewayv2-deployment-stagename"></a>
A name for the stage that API Gateway creates with this deployment\. Use only alphanumeric characters\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-apigatewayv2-deployment-returnvalues"></a>

### Ref<a name="aws-resource-apigatewayv2-deployment-ref"></a>

When you pass the logical ID of an `AWS::ApiGatewayV2::Deployment` resource to the intrinsic `Ref` function, the function returns the deployment ID, such as `123abc`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-apigatewayv2-deployment-examples"></a>

### Deployment creation example<a name="aws-resource-apigatewayv2-deployment-example1"></a>

The following example creates a `deployment` resource for the `MyApi` API, which has the `MyRoute` route defined\.

#### JSON<a name="aws-resource-apigatewayv2-deployment-example1.json"></a>

```
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
```

#### YAML<a name="aws-resource-apigatewayv2-deployment-example1.yaml"></a>

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

## See Also<a name="aws-resource-apigatewayv2-deployment-seealso"></a>
+  [CreateDeployment](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-deployments.html#CreateDeployment) in the *Amazon API Gateway V2 API Reference*\. 