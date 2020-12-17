# AWS::EC2::TransitGateway<a name="aws-resource-ec2-transitgateway"></a>

Specifies a transit gateway\.

You can use a transit gateway to interconnect your virtual private clouds \(VPC\) and on\-premises networks\. After the transit gateway enters the `available` state, you can attach your VPCs and VPN connections to the transit gateway\.

To attach your VPCs, use [AWS::EC2::TransitGatewayAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayattachment.html)\.

To attach a VPN connection, use [AWS::EC2::CustomerGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-customer-gateway.html) to create a customer gateway and specify the ID of the customer gateway and the ID of the transit gateway in a call to [AWS::EC2::VPNConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpn-connection.html)\.

When you create a transit gateway, we create a default transit gateway route table and use it as the default association route table and the default propagation route table\. You can use [AWS::EC2::TransitGatewayRouteTable](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetable.html) to create additional transit gateway route tables\. If you disable automatic route propagation, we do not create a default transit gateway route table\. You can use [AWS::EC2::TransitGatewayRouteTablePropagation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetablepropagation.html) to propagate routes from a resource attachment to a transit gateway route table\. If you disable automatic associations, you can use [AWS::EC2::TransitGatewayRouteTableAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetableassociation.html) to associate a resource attachment with a transit gateway route table\.

## Syntax<a name="aws-resource-ec2-transitgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGateway",
  "Properties" : {
      "[AmazonSideAsn](#cfn-ec2-transitgateway-amazonsideasn)" : Integer,
      "[AutoAcceptSharedAttachments](#cfn-ec2-transitgateway-autoacceptsharedattachments)" : String,
      "[DefaultRouteTableAssociation](#cfn-ec2-transitgateway-defaultroutetableassociation)" : String,
      "[DefaultRouteTablePropagation](#cfn-ec2-transitgateway-defaultroutetablepropagation)" : String,
      "[Description](#cfn-ec2-transitgateway-description)" : String,
      "[DnsSupport](#cfn-ec2-transitgateway-dnssupport)" : String,
      "[MulticastSupport](#cfn-ec2-transitgateway-multicastsupport)" : String,
      "[Tags](#cfn-ec2-transitgateway-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpnEcmpSupport](#cfn-ec2-transitgateway-vpnecmpsupport)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgateway-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGateway
Properties: 
  [AmazonSideAsn](#cfn-ec2-transitgateway-amazonsideasn): Integer
  [AutoAcceptSharedAttachments](#cfn-ec2-transitgateway-autoacceptsharedattachments): String
  [DefaultRouteTableAssociation](#cfn-ec2-transitgateway-defaultroutetableassociation): String
  [DefaultRouteTablePropagation](#cfn-ec2-transitgateway-defaultroutetablepropagation): String
  [Description](#cfn-ec2-transitgateway-description): String
  [DnsSupport](#cfn-ec2-transitgateway-dnssupport): String
  [MulticastSupport](#cfn-ec2-transitgateway-multicastsupport): String
  [Tags](#cfn-ec2-transitgateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpnEcmpSupport](#cfn-ec2-transitgateway-vpnecmpsupport): String
```

## Properties<a name="aws-resource-ec2-transitgateway-properties"></a>

`AmazonSideAsn`  <a name="cfn-ec2-transitgateway-amazonsideasn"></a>
A private Autonomous System Number \(ASN\) for the Amazon side of a BGP session\. The range is 64512 to 65534 for 16\-bit ASNs\. The default is 64512\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AutoAcceptSharedAttachments`  <a name="cfn-ec2-transitgateway-autoacceptsharedattachments"></a>
Enable or disable automatic acceptance of attachment requests\. Disabled by default\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultRouteTableAssociation`  <a name="cfn-ec2-transitgateway-defaultroutetableassociation"></a>
Enable or disable automatic association with the default association route table\. Enabled by default\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultRouteTablePropagation`  <a name="cfn-ec2-transitgateway-defaultroutetablepropagation"></a>
Enable or disable automatic propagation of routes to the default propagation route table\. Enabled by default\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-transitgateway-description"></a>
The description of the transit gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DnsSupport`  <a name="cfn-ec2-transitgateway-dnssupport"></a>
Enable or disable DNS support\. Enabled by default\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MulticastSupport`  <a name="cfn-ec2-transitgateway-multicastsupport"></a>
Indicates whether multicast is enabled on the transit gateway  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-transitgateway-tags"></a>
The tags for the transit gateway\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpnEcmpSupport`  <a name="cfn-ec2-transitgateway-vpnecmpsupport"></a>
Enable or disable Equal Cost Multipath Protocol support\. Enabled by default\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disable | enable`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgateway-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the transit gateway\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-transitgateway--examples"></a>



### Transit Gateway<a name="aws-resource-ec2-transitgateway--examples--Transit_Gateway"></a>

The following example declares a transit gateway\.

#### JSON<a name="aws-resource-ec2-transitgateway--examples--Transit_Gateway--json"></a>

```
"myTransitGateway": {
   "Type": "AWS::EC2::TransitGateway",
   "Properties": {
      "AmazonSideAsn": 65000,
      "Description": "TGW Route Integration Test",
      "AutoAcceptSharedAttachments": "disable",
      "DefaultRouteTableAssociation": "enable",
      "DnsSupport": "enable",
      "VpnEcmpSupport": "enable",
      "Tags": [
         {
            "Key": "Application",
            "Value": {
               "Ref": "AWS::StackId"
            }
         }
      ]
   }
}
```

#### YAML<a name="aws-resource-ec2-transitgateway--examples--Transit_Gateway--yaml"></a>

```
  myTransitGateway:
    Type: "AWS::EC2::TransitGateway"
    Properties:
      AmazonSideAsn: 65000
      Description: "TGW Route Integration Test"
      AutoAcceptSharedAttachments: "disable"
      DefaultRouteTableAssociation: "enable"
      DnsSupport: "enable"
      VpnEcmpSupport: "enable"
      Tags:
      - Key: Application
        Value: !Ref 'AWS::StackId'
```

## See also<a name="aws-resource-ec2-transitgateway--seealso"></a>
+  [CreateTransitGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGateway.html) in the *Amazon EC2 API Reference*
+  [AWS::RAM::ResourceShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ram-resourceshare.html)

