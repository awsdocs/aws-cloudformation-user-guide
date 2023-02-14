# AWS::EC2::NetworkInsightsAnalysis AnalysisPacketHeader<a name="aws-properties-ec2-networkinsightsanalysis-analysispacketheader"></a>

Describes a header\. Reflects any changes made by a component as traffic passes through\. The fields of an inbound header are null except for the first component of a path\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-analysispacketheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-analysispacketheader-syntax.json"></a>

```
{
  "[DestinationAddresses](#cfn-ec2-networkinsightsanalysis-analysispacketheader-destinationaddresses)" : [ String, ... ],
  "[DestinationPortRanges](#cfn-ec2-networkinsightsanalysis-analysispacketheader-destinationportranges)" : [ PortRange, ... ],
  "[Protocol](#cfn-ec2-networkinsightsanalysis-analysispacketheader-protocol)" : String,
  "[SourceAddresses](#cfn-ec2-networkinsightsanalysis-analysispacketheader-sourceaddresses)" : [ String, ... ],
  "[SourcePortRanges](#cfn-ec2-networkinsightsanalysis-analysispacketheader-sourceportranges)" : [ PortRange, ... ]
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-analysispacketheader-syntax.yaml"></a>

```
  [DestinationAddresses](#cfn-ec2-networkinsightsanalysis-analysispacketheader-destinationaddresses): 
    - String
  [DestinationPortRanges](#cfn-ec2-networkinsightsanalysis-analysispacketheader-destinationportranges): 
    - PortRange
  [Protocol](#cfn-ec2-networkinsightsanalysis-analysispacketheader-protocol): String
  [SourceAddresses](#cfn-ec2-networkinsightsanalysis-analysispacketheader-sourceaddresses): 
    - String
  [SourcePortRanges](#cfn-ec2-networkinsightsanalysis-analysispacketheader-sourceportranges): 
    - PortRange
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-analysispacketheader-properties"></a>

`DestinationAddresses`  <a name="cfn-ec2-networkinsightsanalysis-analysispacketheader-destinationaddresses"></a>
The destination addresses\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationPortRanges`  <a name="cfn-ec2-networkinsightsanalysis-analysispacketheader-destinationportranges"></a>
The destination port ranges\.  
*Required*: No  
*Type*: List of [PortRange](aws-properties-ec2-networkinsightsanalysis-portrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-ec2-networkinsightsanalysis-analysispacketheader-protocol"></a>
The protocol\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceAddresses`  <a name="cfn-ec2-networkinsightsanalysis-analysispacketheader-sourceaddresses"></a>
The source addresses\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourcePortRanges`  <a name="cfn-ec2-networkinsightsanalysis-analysispacketheader-sourceportranges"></a>
The source port ranges\.  
*Required*: No  
*Type*: List of [PortRange](aws-properties-ec2-networkinsightsanalysis-portrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)