# AWS::EC2::IPAM<a name="aws-resource-ec2-ipam"></a>

IPAM is a VPC feature that you can use to automate your IP address management workflows including assigning, tracking, troubleshooting, and auditing IP addresses across AWS Regions and accounts throughout your AWS Organization\. For more information, see [What is IPAM?](https://docs.aws.amazon.com/vpc/latest/ipam/what-is-it-ipam.html) in the *Amazon VPC IPAM User Guide*\.

## Syntax<a name="aws-resource-ec2-ipam-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ipam-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::IPAM",
  "Properties" : {
      "[DefaultResourceDiscoveryAssociationId](#cfn-ec2-ipam-defaultresourcediscoveryassociationid)" : String,
      "[DefaultResourceDiscoveryId](#cfn-ec2-ipam-defaultresourcediscoveryid)" : String,
      "[Description](#cfn-ec2-ipam-description)" : String,
      "[OperatingRegions](#cfn-ec2-ipam-operatingregions)" : [ IpamOperatingRegion, ... ],
      "[ResourceDiscoveryAssociationCount](#cfn-ec2-ipam-resourcediscoveryassociationcount)" : Integer,
      "[Tags](#cfn-ec2-ipam-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-ipam-syntax.yaml"></a>

```
Type: AWS::EC2::IPAM
Properties: 
  [DefaultResourceDiscoveryAssociationId](#cfn-ec2-ipam-defaultresourcediscoveryassociationid): String
  [DefaultResourceDiscoveryId](#cfn-ec2-ipam-defaultresourcediscoveryid): String
  [Description](#cfn-ec2-ipam-description): String
  [OperatingRegions](#cfn-ec2-ipam-operatingregions): 
    - IpamOperatingRegion
  [ResourceDiscoveryAssociationCount](#cfn-ec2-ipam-resourcediscoveryassociationcount): Integer
  [Tags](#cfn-ec2-ipam-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-ipam-properties"></a>

`DefaultResourceDiscoveryAssociationId`  <a name="cfn-ec2-ipam-defaultresourcediscoveryassociationid"></a>
The IPAM's default resource discovery association ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultResourceDiscoveryId`  <a name="cfn-ec2-ipam-defaultresourcediscoveryid"></a>
The IPAM's default resource discovery ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ec2-ipam-description"></a>
The description for the IPAM\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperatingRegions`  <a name="cfn-ec2-ipam-operatingregions"></a>
The operating Regions for an IPAM\. Operating Regions are AWS Regions where the IPAM is allowed to manage IP address CIDRs\. IPAM only discovers and monitors resources in the AWS Regions you select as operating Regions\.  
For more information about operating Regions, see [Create an IPAM](https://docs.aws.amazon.com/vpc/latest/ipam/create-ipam.html) in the *Amazon VPC IPAM User Guide*\.  
*Required*: No  
*Type*: List of [IpamOperatingRegion](aws-properties-ec2-ipam-ipamoperatingregion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceDiscoveryAssociationCount`  <a name="cfn-ec2-ipam-resourcediscoveryassociationcount"></a>
The IPAM's resource discovery association count\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-ipam-tags"></a>
The key/value combination of a tag assigned to the resource\. Use the tag key in the filter name and the tag value as the filter value\. For example, to find all resources that have a tag with the key `Owner` and the value `TeamA`, specify `tag:Owner` for the filter name and `TeamA` for the filter value\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-ipam-return-values"></a>

### Ref<a name="aws-resource-ec2-ipam-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IPAM ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-ipam-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ipam-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the IPAM\.

`IpamId`  <a name="IpamId-fn::getatt"></a>
The ID of the IPAM\.

`PrivateDefaultScopeId`  <a name="PrivateDefaultScopeId-fn::getatt"></a>
The ID of the IPAM's default private scope\.

`PublicDefaultScopeId`  <a name="PublicDefaultScopeId-fn::getatt"></a>
The ID of the IPAM's default public scope\.

`ScopeCount`  <a name="ScopeCount-fn::getatt"></a>
The number of scopes in the IPAM\. The scope quota is 5\.