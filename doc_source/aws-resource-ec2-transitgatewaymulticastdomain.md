# AWS::EC2::TransitGatewayMulticastDomain<a name="aws-resource-ec2-transitgatewaymulticastdomain"></a>

Creates a multicast domain using the specified transit gateway\.

The transit gateway must be in the available state before you create a domain\.

## Syntax<a name="aws-resource-ec2-transitgatewaymulticastdomain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewaymulticastdomain-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayMulticastDomain",
  "Properties" : {
      "[Options](#cfn-ec2-transitgatewaymulticastdomain-options)" : Options,
      "[Tags](#cfn-ec2-transitgatewaymulticastdomain-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayId](#cfn-ec2-transitgatewaymulticastdomain-transitgatewayid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewaymulticastdomain-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayMulticastDomain
Properties: 
  [Options](#cfn-ec2-transitgatewaymulticastdomain-options): 
    Options
  [Tags](#cfn-ec2-transitgatewaymulticastdomain-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayId](#cfn-ec2-transitgatewaymulticastdomain-transitgatewayid): String
```

## Properties<a name="aws-resource-ec2-transitgatewaymulticastdomain-properties"></a>

`Options`  <a name="cfn-ec2-transitgatewaymulticastdomain-options"></a>
The options for the transit gateway multicast domain\.  
+ AutoAcceptSharedAssociations \(enable \| disable\)
+ Igmpv2Support \(enable \| disable\)
+ StaticSourcesSupport \(enable \| disable\)
*Required*: No  
*Type*: [Options](aws-properties-ec2-transitgatewaymulticastdomain-options.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-transitgatewaymulticastdomain-tags"></a>
The tags for the transit gateway multicast domain\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayId`  <a name="cfn-ec2-transitgatewaymulticastdomain-transitgatewayid"></a>
The ID of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewaymulticastdomain-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewaymulticastdomain-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the transit gateway multicast domain ID\. For example: `tgw-mcast-domain-000fb24d04EXAMPLE`\.

### Fn::GetAtt<a name="aws-resource-ec2-transitgatewaymulticastdomain-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-transitgatewaymulticastdomain-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time the multicast domain was created\.

`State`  <a name="State-fn::getatt"></a>
The state of the multicast domain\.

`TransitGatewayMulticastDomainArn`  <a name="TransitGatewayMulticastDomainArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the multicast domain\.

`TransitGatewayMulticastDomainId`  <a name="TransitGatewayMulticastDomainId-fn::getatt"></a>
The ID of the multicast domain\.

## See also<a name="aws-resource-ec2-transitgatewaymulticastdomain--seealso"></a>
+ [CreateTransitGatewayMulticastDomain](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayMulticastDomain.html) in the *Amazon EC2 API Reference*

