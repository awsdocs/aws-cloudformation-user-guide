# AWS::EC2::IPAMResourceDiscoveryAssociation<a name="aws-resource-ec2-ipamresourcediscoveryassociation"></a>

An IPAM resource discovery association\. An associated resource discovery is a resource discovery that has been associated with an IPAM\. IPAM aggregates the resource CIDRs discovered by the associated resource discovery\.

## Syntax<a name="aws-resource-ec2-ipamresourcediscoveryassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ipamresourcediscoveryassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::IPAMResourceDiscoveryAssociation",
  "Properties" : {
      "[IpamId](#cfn-ec2-ipamresourcediscoveryassociation-ipamid)" : String,
      "[IpamResourceDiscoveryId](#cfn-ec2-ipamresourcediscoveryassociation-ipamresourcediscoveryid)" : String,
      "[Tags](#cfn-ec2-ipamresourcediscoveryassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-ipamresourcediscoveryassociation-syntax.yaml"></a>

```
Type: AWS::EC2::IPAMResourceDiscoveryAssociation
Properties: 
  [IpamId](#cfn-ec2-ipamresourcediscoveryassociation-ipamid): String
  [IpamResourceDiscoveryId](#cfn-ec2-ipamresourcediscoveryassociation-ipamresourcediscoveryid): String
  [Tags](#cfn-ec2-ipamresourcediscoveryassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-ipamresourcediscoveryassociation-properties"></a>

`IpamId`  <a name="cfn-ec2-ipamresourcediscoveryassociation-ipamid"></a>
The IPAM ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpamResourceDiscoveryId`  <a name="cfn-ec2-ipamresourcediscoveryassociation-ipamresourcediscoveryid"></a>
The resource discovery ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-ipamresourcediscoveryassociation-tags"></a>
A tag is a label that you assign to an AWS resource\. Each tag consists of a key and an optional value\. You can use tags to search and filter your resources or track your AWS costs\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-ipamresourcediscoveryassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-ipamresourcediscoveryassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource discovery ID\. For example: `ipam-res-disco-111122223333`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-ipamresourcediscoveryassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ipamresourcediscoveryassociation-return-values-fn--getatt-fn--getatt"></a>

`IpamArn`  <a name="IpamArn-fn::getatt"></a>
Property description not available\.

`IpamRegion`  <a name="IpamRegion-fn::getatt"></a>
Property description not available\.

`IpamResourceDiscoveryAssociationArn`  <a name="IpamResourceDiscoveryAssociationArn-fn::getatt"></a>
The resource discovery association ARN\.

`IpamResourceDiscoveryAssociationId`  <a name="IpamResourceDiscoveryAssociationId-fn::getatt"></a>
The resource discovery association ID\.

`IsDefault`  <a name="IsDefault-fn::getatt"></a>
Defines if the resource discovery is the default\. When you create an IPAM, a default resource discovery is created for your IPAM and it's associated with your IPAM\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The owner ID\.

`ResourceDiscoveryStatus`  <a name="ResourceDiscoveryStatus-fn::getatt"></a>
Property description not available\.

`State`  <a name="State-fn::getatt"></a>
The lifecycle state of the association when you associate or disassociate a resource discovery\.  
+ `associate-in-progress` \- Resource discovery is being associated\.
+ `associate-complete` \- Resource discovery association is complete\.
+ `associate-failed` \- Resource discovery association has failed\.
+ `disassociate-in-progress` \- Resource discovery is being disassociated\.
+ `disassociate-complete` \- Resource discovery disassociation is complete\.
+ `disassociate-failed ` \- Resource discovery disassociation has failed\.
+ `isolate-in-progress` \- AWS account that created the resource discovery association has been removed and the resource discovery associatation is being isolated\.
+ `isolate-complete` \- Resource discovery isolation is complete\.\.
+ `restore-in-progress` \- Resource discovery is being restored\.