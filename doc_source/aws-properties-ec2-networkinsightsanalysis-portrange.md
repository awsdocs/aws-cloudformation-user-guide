# AWS::EC2::NetworkInsightsAnalysis PortRange<a name="aws-properties-ec2-networkinsightsanalysis-portrange"></a>

Describes a range of ports\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-portrange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-portrange-syntax.json"></a>

```
{
  "[From](#cfn-ec2-networkinsightsanalysis-portrange-from)" : Integer,
  "[To](#cfn-ec2-networkinsightsanalysis-portrange-to)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-portrange-syntax.yaml"></a>

```
  [From](#cfn-ec2-networkinsightsanalysis-portrange-from): Integer
  [To](#cfn-ec2-networkinsightsanalysis-portrange-to): Integer
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-portrange-properties"></a>

`From`  <a name="cfn-ec2-networkinsightsanalysis-portrange-from"></a>
The first port in the range\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`To`  <a name="cfn-ec2-networkinsightsanalysis-portrange-to"></a>
The last port in the range\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)