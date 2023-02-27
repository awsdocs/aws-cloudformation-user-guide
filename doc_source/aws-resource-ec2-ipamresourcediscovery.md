# AWS::EC2::IPAMResourceDiscovery<a name="aws-resource-ec2-ipamresourcediscovery"></a>

A resource discovery is an IPAM component that enables IPAM to manage and monitor resources that belong to the owning account\.

## Syntax<a name="aws-resource-ec2-ipamresourcediscovery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ipamresourcediscovery-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::IPAMResourceDiscovery",
  "Properties" : {
      "[Description](#cfn-ec2-ipamresourcediscovery-description)" : String,
      "[OperatingRegions](#cfn-ec2-ipamresourcediscovery-operatingregions)" : [ IpamOperatingRegion, ... ],
      "[Tags](#cfn-ec2-ipamresourcediscovery-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-ipamresourcediscovery-syntax.yaml"></a>

```
Type: AWS::EC2::IPAMResourceDiscovery
Properties: 
  [Description](#cfn-ec2-ipamresourcediscovery-description): String
  [OperatingRegions](#cfn-ec2-ipamresourcediscovery-operatingregions): 
    - IpamOperatingRegion
  [Tags](#cfn-ec2-ipamresourcediscovery-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-ipamresourcediscovery-properties"></a>

`Description`  <a name="cfn-ec2-ipamresourcediscovery-description"></a>
The resource discovery description\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperatingRegions`  <a name="cfn-ec2-ipamresourcediscovery-operatingregions"></a>
The operating Regions for the resource discovery\. Operating Regions are AWS Regions where the IPAM is allowed to manage IP address CIDRs\. IPAM only discovers and monitors resources in the AWS Regions you select as operating Regions\.  
*Required*: No  
*Type*: List of [IpamOperatingRegion](aws-properties-ec2-ipamresourcediscovery-ipamoperatingregion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-ipamresourcediscovery-tags"></a>
A tag is a label that you assign to an AWS resource\. Each tag consists of a key and an optional value\. You can use tags to search and filter your resources or track your AWS costs\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-ipamresourcediscovery-return-values"></a>

### Ref<a name="aws-resource-ec2-ipamresourcediscovery-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource discovery ID\. For example: `ipam-res-disco-111122223333`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-ipamresourcediscovery-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ipamresourcediscovery-return-values-fn--getatt-fn--getatt"></a>

`IpamResourceDiscoveryArn`  <a name="IpamResourceDiscoveryArn-fn::getatt"></a>
The resource discovery ARN\.

`IpamResourceDiscoveryId`  <a name="IpamResourceDiscoveryId-fn::getatt"></a>
The resource discovery ID\.

`IpamResourceDiscoveryRegion`  <a name="IpamResourceDiscoveryRegion-fn::getatt"></a>
The resource discovery Region\.

`IsDefault`  <a name="IsDefault-fn::getatt"></a>
Defines if the resource discovery is the default\. The default resource discovery is the resource discovery automatically created when you create an IPAM\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The owner ID\.

`State`  <a name="State-fn::getatt"></a>
The resource discovery's state\.  
+ `create-in-progress` \- Resource discovery is being created\.
+ `create-complete` \- Resource discovery creation is complete\.
+ `create-failed` \- Resource discovery creation has failed\.
+ `modify-in-progress` \- Resource discovery is being modified\.
+ `modify-complete` \- Resource discovery modification is complete\.
+ `modify-failed` \- Resource discovery modification has failed\.
+ `delete-in-progress` \- Resource discovery is being deleted\.
+ `delete-complete` \- Resource discovery deletion is complete\.
+ `delete-failed` \- Resource discovery deletion has failed\.
+ `isolate-in-progress` \- AWS account that created the resource discovery has been removed and the resource discovery is being isolated\.
+ `isolate-complete` \- Resource discovery isolation is complete\.
+ `restore-in-progress` \- AWS account that created the resource discovery and was isolated has been restored\.