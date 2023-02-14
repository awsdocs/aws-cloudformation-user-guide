# AWS::EC2::TransitGatewayMulticastDomainAssociation<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation"></a>

Associates the specified subnets and transit gateway attachments with the specified transit gateway multicast domain\.

The transit gateway attachment must be in the available state before you can add a resource\.

## Syntax<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayMulticastDomainAssociation",
  "Properties" : {
      "[SubnetId](#cfn-ec2-transitgatewaymulticastdomainassociation-subnetid)" : String,
      "[TransitGatewayAttachmentId](#cfn-ec2-transitgatewaymulticastdomainassociation-transitgatewayattachmentid)" : String,
      "[TransitGatewayMulticastDomainId](#cfn-ec2-transitgatewaymulticastdomainassociation-transitgatewaymulticastdomainid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayMulticastDomainAssociation
Properties: 
  [SubnetId](#cfn-ec2-transitgatewaymulticastdomainassociation-subnetid): String
  [TransitGatewayAttachmentId](#cfn-ec2-transitgatewaymulticastdomainassociation-transitgatewayattachmentid): String
  [TransitGatewayMulticastDomainId](#cfn-ec2-transitgatewaymulticastdomainassociation-transitgatewaymulticastdomainid): String
```

## Properties<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-properties"></a>

`SubnetId`  <a name="cfn-ec2-transitgatewaymulticastdomainassociation-subnetid"></a>
The IDs of the subnets to associate with the transit gateway multicast domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewaymulticastdomainassociation-transitgatewayattachmentid"></a>
The ID of the transit gateway attachment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayMulticastDomainId`  <a name="cfn-ec2-transitgatewaymulticastdomainassociation-transitgatewaymulticastdomainid"></a>
The ID of the transit gateway multicast domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the transit gateway multicast domain ID\. For example: `tgw-mcast-domain-000fb24d04EXAMPLE`\.

### Fn::GetAtt<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-transitgatewaymulticastdomainassociation-return-values-fn--getatt-fn--getatt"></a>

`ResourceId`  <a name="ResourceId-fn::getatt"></a>
The ID of the resource\.

`ResourceType`  <a name="ResourceType-fn::getatt"></a>
The type of resource, for example a VPC attachment\.

`State`  <a name="State-fn::getatt"></a>
The state of the resource\.

## See also<a name="aws-resource-ec2-transitgatewaymulticastdomainassociation--seealso"></a>
+ [AssociateTransitGatewayMulticastDomain](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AssociateTransitGatewayMulticastDomain.html) in the *Amazon EC2 API Reference*

