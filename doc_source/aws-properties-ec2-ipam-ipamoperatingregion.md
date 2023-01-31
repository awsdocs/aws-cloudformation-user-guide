# AWS::EC2::IPAM IpamOperatingRegion<a name="aws-properties-ec2-ipam-ipamoperatingregion"></a>

The operating Regions for an IPAM\. Operating Regions are AWS Regions where the IPAM is allowed to manage IP address CIDRs\. IPAM only discovers and monitors resources in the AWS Regions you select as operating Regions\.

For more information about operating Regions, see [Create an IPAM](https://docs.aws.amazon.com/vpc/latest/ipam/create-ipam.html) in the *Amazon VPC IPAM User Guide*\.

## Syntax<a name="aws-properties-ec2-ipam-ipamoperatingregion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ipam-ipamoperatingregion-syntax.json"></a>

```
{
  "[RegionName](#cfn-ec2-ipam-ipamoperatingregion-regionname)" : String
}
```

### YAML<a name="aws-properties-ec2-ipam-ipamoperatingregion-syntax.yaml"></a>

```
  [RegionName](#cfn-ec2-ipam-ipamoperatingregion-regionname): String
```

## Properties<a name="aws-properties-ec2-ipam-ipamoperatingregion-properties"></a>

`RegionName`  <a name="cfn-ec2-ipam-ipamoperatingregion-regionname"></a>
The name of the operating Region\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)