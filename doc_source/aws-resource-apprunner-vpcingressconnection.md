# AWS::AppRunner::VpcIngressConnection<a name="aws-resource-apprunner-vpcingressconnection"></a>

The `AWS::AppRunner::VpcIngressConnection` resource is an AWS App Runner resource type that specifies an App Runner VPC Ingress Connection\.

App Runner requires this resource when you want to associate your App Runner service to an Amazon VPC endpoint\.

## Syntax<a name="aws-resource-apprunner-vpcingressconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apprunner-vpcingressconnection-syntax.json"></a>

```
{
  "Type" : "AWS::AppRunner::VpcIngressConnection",
  "Properties" : {
      "[IngressVpcConfiguration](#cfn-apprunner-vpcingressconnection-ingressvpcconfiguration)" : IngressVpcConfiguration,
      "[ServiceArn](#cfn-apprunner-vpcingressconnection-servicearn)" : String,
      "[Tags](#cfn-apprunner-vpcingressconnection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcIngressConnectionName](#cfn-apprunner-vpcingressconnection-vpcingressconnectionname)" : String
    }
}
```

### YAML<a name="aws-resource-apprunner-vpcingressconnection-syntax.yaml"></a>

```
Type: AWS::AppRunner::VpcIngressConnection
Properties: 
  [IngressVpcConfiguration](#cfn-apprunner-vpcingressconnection-ingressvpcconfiguration): 
    IngressVpcConfiguration
  [ServiceArn](#cfn-apprunner-vpcingressconnection-servicearn): String
  [Tags](#cfn-apprunner-vpcingressconnection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcIngressConnectionName](#cfn-apprunner-vpcingressconnection-vpcingressconnectionname): String
```

## Properties<a name="aws-resource-apprunner-vpcingressconnection-properties"></a>

`IngressVpcConfiguration`  <a name="cfn-apprunner-vpcingressconnection-ingressvpcconfiguration"></a>
Specifications for the customer’s Amazon VPC and the related AWS PrivateLink VPC endpoint that are used to create the VPC Ingress Connection resource\.  
*Required*: Yes  
*Type*: [IngressVpcConfiguration](aws-properties-apprunner-vpcingressconnection-ingressvpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceArn`  <a name="cfn-apprunner-vpcingressconnection-servicearn"></a>
The Amazon Resource Name \(ARN\) for this App Runner service that is used to create the VPC Ingress Connection resource\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1011`  
*Pattern*: `arn:aws(-[\w]+)*:[a-z0-9-\\.]{0,63}:[a-z0-9-\\.]{0,63}:[0-9]{12}:(\w|\/|-){1,1011}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-apprunner-vpcingressconnection-tags"></a>
An optional list of metadata items that you can associate with the VPC Ingress Connection resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcIngressConnectionName`  <a name="cfn-apprunner-vpcingressconnection-vpcingressconnectionname"></a>
The customer\-provided VPC Ingress Connection name\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `40`  
*Pattern*: `[A-Za-z0-9][A-Za-z0-9\-_]{3,39}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apprunner-vpcingressconnection-return-values"></a>

### Ref<a name="aws-resource-apprunner-vpcingressconnection-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apprunner-vpcingressconnection-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apprunner-vpcingressconnection-return-values-fn--getatt-fn--getatt"></a>

`DomainName`  <a name="DomainName-fn::getatt"></a>
The domain name associated with the VPC Ingress Connection resource\.

`Status`  <a name="Status-fn::getatt"></a>
The current status of the VPC Ingress Connection\. The VPC Ingress Connection displays one of the following statuses: `AVAILABLE`, `PENDING_CREATION`, `PENDING_DELETION`, `FAILED_CREATION`, `FAILED_DELETION`, `PENDNG_UPDATE`, `FAILED_UPDATE`, and `DELETED`\. 

`VpcIngressConnectionArn`  <a name="VpcIngressConnectionArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the VPC Ingress Connection\.

## Examples<a name="aws-resource-apprunner-vpcingressconnection--examples"></a>

### VPC Ingress Connection<a name="aws-resource-apprunner-vpcingressconnection--examples--VPC_Ingress_Connection"></a>

This example illustrates creating a VPC Ingress Connection\.

#### JSON<a name="aws-resource-apprunner-vpcingressconnection--examples--VPC_Ingress_Connection--json"></a>

```
{
  "Type": "AWS::AppRunner::VpcIngressConnection",
  "Properties": {
    "IngressVpcConfiguration": {
      "VpcEndpointId": "vpc-1a2b3c4d",
      "VpcId": "vpc-4a6b7c8d"
    },
    "ServiceArn": "arn:aws:apprunner:us-east-1:123456789012:service/my-service",
    "VpcIngressConnectionName": "my-vpc-ingress-connection"
  }
}
```

#### YAML<a name="aws-resource-apprunner-vpcingressconnection--examples--VPC_Ingress_Connection--yaml"></a>

```
Type: AWS::AppRunner::VpcIngressConnection
Properties:
  IngressVpcConfiguration:
    VpcEndpointId: vpce-1a2b3c4d
    VpcId: vpc-4a6b7c8d
  ServiceArn: arn:aws:apprunner:us-east-1:123456789012:service/my-service
  VpcIngressConnectionName: my-vpc-ingress-connection
```

## See also<a name="aws-resource-apprunner-vpcingressconnection--seealso"></a>
+ [Configure network settings for incoming traffic](https://docs.aws.amazon.com/apprunner/latest/dg/network-pl.html) in the *AWS App Runner Developer Guide*