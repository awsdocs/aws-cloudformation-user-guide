# AWS::RefactorSpaces::Application<a name="aws-resource-refactorspaces-application"></a>

Creates an AWS Migration Hub Refactor Spaces application\. The account that owns the environment also owns the applications created inside the environment, regardless of the account that creates the application\. Refactor Spaces provisions an Amazon API Gateway, API Gateway VPC link, and Network Load Balancer for the application proxy inside your account\.

## Syntax<a name="aws-resource-refactorspaces-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-refactorspaces-application-syntax.json"></a>

```
{
  "Type" : "AWS::RefactorSpaces::Application",
  "Properties" : {
      "[ApiGatewayProxy](#cfn-refactorspaces-application-apigatewayproxy)" : ApiGatewayProxyInput,
      "[EnvironmentIdentifier](#cfn-refactorspaces-application-environmentidentifier)" : String,
      "[Name](#cfn-refactorspaces-application-name)" : String,
      "[ProxyType](#cfn-refactorspaces-application-proxytype)" : String,
      "[Tags](#cfn-refactorspaces-application-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-refactorspaces-application-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-refactorspaces-application-syntax.yaml"></a>

```
Type: AWS::RefactorSpaces::Application
Properties: 
  [ApiGatewayProxy](#cfn-refactorspaces-application-apigatewayproxy): 
    ApiGatewayProxyInput
  [EnvironmentIdentifier](#cfn-refactorspaces-application-environmentidentifier): String
  [Name](#cfn-refactorspaces-application-name): String
  [ProxyType](#cfn-refactorspaces-application-proxytype): String
  [Tags](#cfn-refactorspaces-application-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-refactorspaces-application-vpcid): String
```

## Properties<a name="aws-resource-refactorspaces-application-properties"></a>

`ApiGatewayProxy`  <a name="cfn-refactorspaces-application-apigatewayproxy"></a>
The endpoint URL of the Amazon API Gateway proxy\.   
*Required*: No  
*Type*: [ApiGatewayProxyInput](aws-properties-refactorspaces-application-apigatewayproxyinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnvironmentIdentifier`  <a name="cfn-refactorspaces-application-environmentidentifier"></a>
The unique identifier of the environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-refactorspaces-application-name"></a>
The name of the application\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProxyType`  <a name="cfn-refactorspaces-application-proxytype"></a>
The proxy type of the proxy created within the application\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-refactorspaces-application-tags"></a>
The tags assigned to the application\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-refactorspaces-application-vpcid"></a>
The ID of the virtual private cloud \(VPC\)\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-refactorspaces-application-return-values"></a>

### Ref<a name="aws-resource-refactorspaces-application-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a composite ID following this format: `<EnvironmentId>|<ApplicationId>`, for example, `env-1234654123|app-1234654123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-refactorspaces-application-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-refactorspaces-application-return-values-fn--getatt-fn--getatt"></a>

`ApiGatewayId`  <a name="ApiGatewayId-fn::getatt"></a>
The resource ID of the API Gateway for the proxy\. 

`ApplicationIdentifier`  <a name="ApplicationIdentifier-fn::getatt"></a>
The unique identifier of the application\.

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the application\.

`NlbArn`  <a name="NlbArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Network Load Balancer\.

`NlbName`  <a name="NlbName-fn::getatt"></a>
The name of the Network Load Balancer configured by the API Gateway proxy\.

`ProxyUrl`  <a name="ProxyUrl-fn::getatt"></a>
The endpoint URL of the Amazon API Gateway proxy\.

`StageName`  <a name="StageName-fn::getatt"></a>
The name of the API Gateway stage\. The name defaults to `prod`\.

`VpcLinkId`  <a name="VpcLinkId-fn::getatt"></a>
The `VpcLink` ID of the API Gateway proxy\. 