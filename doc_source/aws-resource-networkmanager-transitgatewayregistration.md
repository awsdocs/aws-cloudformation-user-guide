# AWS::NetworkManager::TransitGatewayRegistration<a name="aws-resource-networkmanager-transitgatewayregistration"></a>

Registers a transit gateway in your global network\. The transit gateway can be in any AWS Region, but it must be owned by the same AWS account that owns the global network\. You cannot register a transit gateway in more than one global network\.

## Syntax<a name="aws-resource-networkmanager-transitgatewayregistration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-transitgatewayregistration-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::TransitGatewayRegistration",
  "Properties" : {
      "[GlobalNetworkId](#cfn-networkmanager-transitgatewayregistration-globalnetworkid)" : String,
      "[TransitGatewayArn](#cfn-networkmanager-transitgatewayregistration-transitgatewayarn)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-transitgatewayregistration-syntax.yaml"></a>

```
Type: AWS::NetworkManager::TransitGatewayRegistration
Properties: 
  [GlobalNetworkId](#cfn-networkmanager-transitgatewayregistration-globalnetworkid): String
  [TransitGatewayArn](#cfn-networkmanager-transitgatewayregistration-transitgatewayarn): String
```

## Properties<a name="aws-resource-networkmanager-transitgatewayregistration-properties"></a>

`GlobalNetworkId`  <a name="cfn-networkmanager-transitgatewayregistration-globalnetworkid"></a>
The ID of the global network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayArn`  <a name="cfn-networkmanager-transitgatewayregistration-transitgatewayarn"></a>
The Amazon Resource Name \(ARN\) of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-transitgatewayregistration-return-values"></a>

### Ref<a name="aws-resource-networkmanager-transitgatewayregistration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the global network and the ARN of the transit gateway\. For example: `global-network-01231231231231231|arn:aws:ec2:us-west-2:123456789012:transit-gateway/tgw-123abc05e04123abc`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-networkmanager-transitgatewayregistration--examples"></a>



### Transit Gateway Registration<a name="aws-resource-networkmanager-transitgatewayregistration--examples--Transit_Gateway_Registration"></a>

The following example registers a transit gateway in a global network\.

#### JSON<a name="aws-resource-networkmanager-transitgatewayregistration--examples--Transit_Gateway_Registration--json"></a>

```
{
    "Type": "AWS::NetworkManager::TransitGatewayRegistration",
    "Properties": {
        "GlobalNetworkId": {
            "Ref": "GlobalNetwork"
        },
        "TransitGatewayArn": {
            "Fn::Sub": "arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:transit-gateway/${TransitGateway}"
        }
    }
}
```

#### YAML<a name="aws-resource-networkmanager-transitgatewayregistration--examples--Transit_Gateway_Registration--yaml"></a>

```
Type: AWS::NetworkManager::TransitGatewayRegistration
Properties:
  GlobalNetworkId: !Ref GlobalNetwork
  TransitGatewayArn: !Sub 'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:transit-gateway/${TransitGateway}'
```