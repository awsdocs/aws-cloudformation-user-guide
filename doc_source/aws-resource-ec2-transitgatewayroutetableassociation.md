# AWS::EC2::TransitGatewayRouteTableAssociation<a name="aws-resource-ec2-transitgatewayroutetableassociation"></a>

Associates the specified attachment with the specified transit gateway route table\. You can associate only one route table with an attachment\.

**Note**  
The `TransitGatewayRouteTableId` value changes when you use `AWS::EC2::TransitGatewayRouteTableAssociation`\. To update the route table on the resource, detach the route table and update the Cloud Formation stack\. After you have the new `TransitGatewayRouteTableId`, perform another Cloud Formation stack update with the new ID\. For more information, see [Update Behaviors of Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html)\.

## Syntax<a name="aws-resource-ec2-transitgatewayroutetableassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewayroutetableassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayRouteTableAssociation",
  "Properties" : {
      "[TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayattachmentid)" : String,
      "[TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayroutetableid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewayroutetableassociation-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayRouteTableAssociation
Properties: 
  [TransitGatewayAttachmentId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayattachmentid): String
  [TransitGatewayRouteTableId](#cfn-ec2-transitgatewayroutetableassociation-transitgatewayroutetableid): String
```

## Properties<a name="aws-resource-ec2-transitgatewayroutetableassociation-properties"></a>

`TransitGatewayAttachmentId`  <a name="cfn-ec2-transitgatewayroutetableassociation-transitgatewayattachmentid"></a>
The ID of the attachment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayRouteTableId`  <a name="cfn-ec2-transitgatewayroutetableassociation-transitgatewayroutetableid"></a>
The ID of the route table for the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewayroutetableassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewayroutetableassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the transit gateway route table association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-ec2-transitgatewayroutetableassociation--seealso"></a>
+  [AssociateTransitGatewayRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AssociateTransitGatewayRouteTable.html) in the *Amazon EC2 API Reference*

