# AWS::EC2::NetworkInsightsPath PathFilter<a name="aws-properties-ec2-networkinsightspath-pathfilter"></a>

Describes a set of filters for a path analysis\. Use path filters to scope the analysis when there can be multiple resulting paths\.

## Syntax<a name="aws-properties-ec2-networkinsightspath-pathfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightspath-pathfilter-syntax.json"></a>

```
{
  "[DestinationAddress](#cfn-ec2-networkinsightspath-pathfilter-destinationaddress)" : String,
  "[DestinationPortRange](#cfn-ec2-networkinsightspath-pathfilter-destinationportrange)" : FilterPortRange,
  "[SourceAddress](#cfn-ec2-networkinsightspath-pathfilter-sourceaddress)" : String,
  "[SourcePortRange](#cfn-ec2-networkinsightspath-pathfilter-sourceportrange)" : FilterPortRange
}
```

### YAML<a name="aws-properties-ec2-networkinsightspath-pathfilter-syntax.yaml"></a>

```
  [DestinationAddress](#cfn-ec2-networkinsightspath-pathfilter-destinationaddress): String
  [DestinationPortRange](#cfn-ec2-networkinsightspath-pathfilter-destinationportrange): 
    FilterPortRange
  [SourceAddress](#cfn-ec2-networkinsightspath-pathfilter-sourceaddress): String
  [SourcePortRange](#cfn-ec2-networkinsightspath-pathfilter-sourceportrange): 
    FilterPortRange
```

## Properties<a name="aws-properties-ec2-networkinsightspath-pathfilter-properties"></a>

`DestinationAddress`  <a name="cfn-ec2-networkinsightspath-pathfilter-destinationaddress"></a>
The destination IPv4 address\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `15`  
*Pattern*: `^([0-9]{1,3}.){3}[0-9]{1,3}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationPortRange`  <a name="cfn-ec2-networkinsightspath-pathfilter-destinationportrange"></a>
The destination port range\.  
*Required*: No  
*Type*: [FilterPortRange](aws-properties-ec2-networkinsightspath-filterportrange.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceAddress`  <a name="cfn-ec2-networkinsightspath-pathfilter-sourceaddress"></a>
The source IPv4 address\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `15`  
*Pattern*: `^([0-9]{1,3}.){3}[0-9]{1,3}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourcePortRange`  <a name="cfn-ec2-networkinsightspath-pathfilter-sourceportrange"></a>
The source port range\.  
*Required*: No  
*Type*: [FilterPortRange](aws-properties-ec2-networkinsightspath-filterportrange.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)