# AWS::ApiGatewayV2::VpcLink<a name="aws-resource-apigatewayv2-vpclink"></a>

The `AWS::ApiGatewayV2::VpcLink` resource creates a VPC link\. Supported only for HTTP APIs\. The VPC link status must transition from `PENDING` to `AVAILABLE` to successfully create a VPC link, which can take up to 10 minutes\. To learn more, see [Working with VPC Links for HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-vpc-links.html) in the *API Gateway Developer Guide*\. 

## Syntax<a name="aws-resource-apigatewayv2-vpclink-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-vpclink-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::VpcLink",
  "Properties" : {
      "[Name](#cfn-apigatewayv2-vpclink-name)" : String,
      "[SecurityGroupIds](#cfn-apigatewayv2-vpclink-securitygroupids)" : [ String, ... ],
      "[SubnetIds](#cfn-apigatewayv2-vpclink-subnetids)" : [ String, ... ],
      "[Tags](#cfn-apigatewayv2-vpclink-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-vpclink-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::VpcLink
Properties: 
  [Name](#cfn-apigatewayv2-vpclink-name): String
  [SecurityGroupIds](#cfn-apigatewayv2-vpclink-securitygroupids): 
    - String
  [SubnetIds](#cfn-apigatewayv2-vpclink-subnetids): 
    - String
  [Tags](#cfn-apigatewayv2-vpclink-tags): Json
```

## Properties<a name="aws-resource-apigatewayv2-vpclink-properties"></a>

`Name`  <a name="cfn-apigatewayv2-vpclink-name"></a>
The name of the VPC link\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-apigatewayv2-vpclink-securitygroupids"></a>
A list of security group IDs for the VPC link\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-apigatewayv2-vpclink-subnetids"></a>
A list of subnet IDs to include in the VPC link\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-apigatewayv2-vpclink-tags"></a>
The collection of tags\. Each tag element is associated with a given resource\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-vpclink-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-vpclink-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the VPC link's ID, such as `abcde1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.