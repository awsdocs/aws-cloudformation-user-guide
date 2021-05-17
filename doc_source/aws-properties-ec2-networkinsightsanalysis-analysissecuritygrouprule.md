# AWS::EC2::NetworkInsightsAnalysis AnalysisSecurityGroupRule<a name="aws-properties-ec2-networkinsightsanalysis-analysissecuritygrouprule"></a>

Describes a security group rule\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-analysissecuritygrouprule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-analysissecuritygrouprule-syntax.json"></a>

```
{
  "[Cidr](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-cidr)" : String,
  "[Direction](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-direction)" : String,
  "[PortRange](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-portrange)" : PortRange,
  "[PrefixListId](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-prefixlistid)" : String,
  "[Protocol](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-protocol)" : String,
  "[SecurityGroupId](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-securitygroupid)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-analysissecuritygrouprule-syntax.yaml"></a>

```
  [Cidr](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-cidr): String
  [Direction](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-direction): String
  [PortRange](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-portrange): 
    PortRange
  [PrefixListId](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-prefixlistid): String
  [Protocol](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-protocol): String
  [SecurityGroupId](#cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-securitygroupid): String
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-analysissecuritygrouprule-properties"></a>

`Cidr`  <a name="cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-cidr"></a>
The IPv4 address range, in CIDR notation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Direction`  <a name="cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-direction"></a>
The direction\. The following are possible values:  
+ egress
+ ingress
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortRange`  <a name="cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-portrange"></a>
The port range\.  
*Required*: No  
*Type*: [PortRange](aws-properties-ec2-networkinsightsanalysis-portrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrefixListId`  <a name="cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-prefixlistid"></a>
The prefix list ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-protocol"></a>
The protocol name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupId`  <a name="cfn-ec2-networkinsightsanalysis-analysissecuritygrouprule-securitygroupid"></a>
The security group ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)