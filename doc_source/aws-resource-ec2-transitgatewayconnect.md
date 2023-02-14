# AWS::EC2::TransitGatewayConnect<a name="aws-resource-ec2-transitgatewayconnect"></a>

Creates a Connect attachment from a specified transit gateway attachment\. A Connect attachment is a GRE\-based tunnel attachment that you can use to establish a connection between a transit gateway and an appliance\.

A Connect attachment uses an existing VPC or AWS Direct Connect attachment as the underlying transport mechanism\.

## Syntax<a name="aws-resource-ec2-transitgatewayconnect-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayconnect-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayConnect",
  "Properties" : {
      "[Options](#cfn-ec2-transitgatewayconnect-options)" : TransitGatewayConnectOptions,
      "[Tags](#cfn-ec2-transitgatewayconnect-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransportTransitGatewayAttachmentId](#cfn-ec2-transitgatewayconnect-transporttransitgatewayattachmentid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayconnect-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayConnect
Properties: 
  [Options](#cfn-ec2-transitgatewayconnect-options): 
    TransitGatewayConnectOptions
  [Tags](#cfn-ec2-transitgatewayconnect-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransportTransitGatewayAttachmentId](#cfn-ec2-transitgatewayconnect-transporttransitgatewayattachmentid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayconnect-properties"></a>

`Options`  <a name="cfn-ec2-transitgatewayconnect-options"></a>
The Connect attachment options\.  
+ protocol \(gre\)
*Required*: Yes  
*Type*: [TransitGatewayConnectOptions](aws-properties-ec2-transitgatewayconnect-transitgatewayconnectoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-transitgatewayconnect-tags"></a>
The tags for the attachment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransportTransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewayconnect-transporttransitgatewayattachmentid"></a>
The ID of the attachment from which the Connect attachment was created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewayconnect-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayconnect-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the transit gateway attachment\. 

### Fn::GetAtt<a name="aws-resource-ec2-transitgatewayconnect-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-transitgatewayconnect-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The creation time\.

`State`  <a name="State-fn::getatt"></a>
The state of the attachment\.

`TransitGatewayAttachmentId`  <a name="TransitGatewayAttachmentId-fn::getatt"></a>
The ID of the transit gateway attachment\.

`TransitGatewayId`  <a name="TransitGatewayId-fn::getatt"></a>
The ID of the transit gateway\.