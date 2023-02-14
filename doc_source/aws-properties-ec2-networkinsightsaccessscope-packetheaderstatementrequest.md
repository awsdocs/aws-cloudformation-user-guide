# AWS::EC2::NetworkInsightsAccessScope PacketHeaderStatementRequest<a name="aws-properties-ec2-networkinsightsaccessscope-packetheaderstatementrequest"></a>

Describes a packet header statement\.

## Syntax<a name="aws-properties-ec2-networkinsightsaccessscope-packetheaderstatementrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsaccessscope-packetheaderstatementrequest-syntax.json"></a>

```
{
  "[DestinationAddresses](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationaddresses)" : [ String, ... ],
  "[DestinationPorts](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationports)" : [ String, ... ],
  "[DestinationPrefixLists](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationprefixlists)" : [ String, ... ],
  "[Protocols](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-protocols)" : [ String, ... ],
  "[SourceAddresses](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceaddresses)" : [ String, ... ],
  "[SourcePorts](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceports)" : [ String, ... ],
  "[SourcePrefixLists](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceprefixlists)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ec2-networkinsightsaccessscope-packetheaderstatementrequest-syntax.yaml"></a>

```
  [DestinationAddresses](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationaddresses): 
    - String
  [DestinationPorts](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationports): 
    - String
  [DestinationPrefixLists](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationprefixlists): 
    - String
  [Protocols](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-protocols): 
    - String
  [SourceAddresses](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceaddresses): 
    - String
  [SourcePorts](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceports): 
    - String
  [SourcePrefixLists](#cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceprefixlists): 
    - String
```

## Properties<a name="aws-properties-ec2-networkinsightsaccessscope-packetheaderstatementrequest-properties"></a>

`DestinationAddresses`  <a name="cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationaddresses"></a>
The destination addresses\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationPorts`  <a name="cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationports"></a>
The destination ports\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationPrefixLists`  <a name="cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-destinationprefixlists"></a>
The destination prefix lists\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocols`  <a name="cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-protocols"></a>
The protocols\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceAddresses`  <a name="cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceaddresses"></a>
The source addresses\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourcePorts`  <a name="cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceports"></a>
The source ports\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourcePrefixLists`  <a name="cfn-ec2-networkinsightsaccessscope-packetheaderstatementrequest-sourceprefixlists"></a>
The source prefix lists\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)