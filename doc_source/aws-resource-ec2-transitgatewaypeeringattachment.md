# AWS::EC2::TransitGatewayPeeringAttachment<a name="aws-resource-ec2-transitgatewaypeeringattachment"></a>

Requests a transit gateway peering attachment between the specified transit gateway \(requester\) and a peer transit gateway \(accepter\)\. The peer transit gateway can be in your account or a different AWS account\.

After you create the peering attachment, the owner of the accepter transit gateway must accept the attachment request\.

## Syntax<a name="aws-resource-ec2-transitgatewaypeeringattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewaypeeringattachment-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayPeeringAttachment",
  "Properties" : {
      "[PeerAccountId](#cfn-ec2-transitgatewaypeeringattachment-peeraccountid)" : String,
      "[PeerRegion](#cfn-ec2-transitgatewaypeeringattachment-peerregion)" : String,
      "[PeerTransitGatewayId](#cfn-ec2-transitgatewaypeeringattachment-peertransitgatewayid)" : String,
      "[Tags](#cfn-ec2-transitgatewaypeeringattachment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayId](#cfn-ec2-transitgatewaypeeringattachment-transitgatewayid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewaypeeringattachment-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayPeeringAttachment
Properties: 
  [PeerAccountId](#cfn-ec2-transitgatewaypeeringattachment-peeraccountid): String
  [PeerRegion](#cfn-ec2-transitgatewaypeeringattachment-peerregion): String
  [PeerTransitGatewayId](#cfn-ec2-transitgatewaypeeringattachment-peertransitgatewayid): String
  [Tags](#cfn-ec2-transitgatewaypeeringattachment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayId](#cfn-ec2-transitgatewaypeeringattachment-transitgatewayid): String
```

## Properties<a name="aws-resource-ec2-transitgatewaypeeringattachment-properties"></a>

`PeerAccountId`  <a name="cfn-ec2-transitgatewaypeeringattachment-peeraccountid"></a>
The ID of the AWS account that owns the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerRegion`  <a name="cfn-ec2-transitgatewaypeeringattachment-peerregion"></a>
The Region of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PeerTransitGatewayId`  <a name="cfn-ec2-transitgatewaypeeringattachment-peertransitgatewayid"></a>
The ID of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-transitgatewaypeeringattachment-tags"></a>
The tags for the transit gateway peering attachment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayId`  <a name="cfn-ec2-transitgatewaypeeringattachment-transitgatewayid"></a>
The ID of the transit gateway peering attachment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewaypeeringattachment-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewaypeeringattachment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the transit gateway peering attachment\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-transitgatewaypeeringattachment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-transitgatewaypeeringattachment-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time the transit gateway peering attachment was created\.

`State`  <a name="State-fn::getatt"></a>
The state of the transit gateway peering attachment\. Note that the `initiating` state has been deprecated\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the transit gateway peering attachment\.

`Status.Code`  <a name="Status.Code-fn::getatt"></a>
The status code\.

`Status.Message`  <a name="Status.Message-fn::getatt"></a>
The status message\.

`TransitGatewayAttachmentId`  <a name="TransitGatewayAttachmentId-fn::getatt"></a>
The ID of the transit gateway peering attachment\.

## See also<a name="aws-resource-ec2-transitgatewaypeeringattachment--seealso"></a>
+ [CreateTransitGatewayPeeringAttachment](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayPeeringAttachment.html) in the *Amazon EC2 API Reference*

