# AWS::EC2::CarrierGateway<a name="aws-resource-ec2-carriergateway"></a>

Creates a carrier gateway\. For more information about carrier gateways, see [Carrier gateways](https://docs.aws.amazon.com/wavelength/latest/developerguide/how-wavelengths-work.html#wavelength-carrier-gateway) in the *AWS Wavelength Developer Guide*\.

## Syntax<a name="aws-resource-ec2-carriergateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-carriergateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::CarrierGateway",
  "Properties" : {
      "[Tags](#cfn-ec2-carriergateway-tags)" : Tags,
      "[VpcId](#cfn-ec2-carriergateway-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-carriergateway-syntax.yaml"></a>

```
Type: AWS::EC2::CarrierGateway
Properties: 
  [Tags](#cfn-ec2-carriergateway-tags): 
    Tags
  [VpcId](#cfn-ec2-carriergateway-vpcid): String
```

## Properties<a name="aws-resource-ec2-carriergateway-properties"></a>

`Tags`  <a name="cfn-ec2-carriergateway-tags"></a>
The tags assigned to the carrier gateway\.  
*Required*: No  
*Type*: [Tags](aws-properties-ec2-carriergateway-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-carriergateway-vpcid"></a>
The ID of the VPC associated with the carrier gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-carriergateway-return-values"></a>

### Ref<a name="aws-resource-ec2-carriergateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the carrier gateway ID\. For example: `cagw-05a8da9a199afb1c7`\.

### Fn::GetAtt<a name="aws-resource-ec2-carriergateway-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-carriergateway-return-values-fn--getatt-fn--getatt"></a>

`CarrierGatewayId`  <a name="CarrierGatewayId-fn::getatt"></a>
The ID of the carrier gateway\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The AWS account ID of the owner of the carrier gateway\.

`State`  <a name="State-fn::getatt"></a>
The state of the carrier gateway\.

## See also<a name="aws-resource-ec2-carriergateway--seealso"></a>
+ [Carrier gateways](https://docs.aws.amazon.com/vpc/latest/userguide/Carrier_Gateway.html) in *Amazon Virtual Private Cloud User Guide*
+ [CreateCarrierGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateCarrierGateway.html) in the *Amazon EC2 API Reference*

