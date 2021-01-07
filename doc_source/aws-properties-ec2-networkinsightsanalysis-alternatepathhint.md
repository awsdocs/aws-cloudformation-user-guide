# AWS::EC2::NetworkInsightsAnalysis AlternatePathHint<a name="aws-properties-ec2-networkinsightsanalysis-alternatepathhint"></a>

Describes an potential intermediate component of a feasible path\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-alternatepathhint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-alternatepathhint-syntax.json"></a>

```
{
  "[ComponentArn](#cfn-ec2-networkinsightsanalysis-alternatepathhint-componentarn)" : String,
  "[ComponentId](#cfn-ec2-networkinsightsanalysis-alternatepathhint-componentid)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-alternatepathhint-syntax.yaml"></a>

```
  [ComponentArn](#cfn-ec2-networkinsightsanalysis-alternatepathhint-componentarn): String
  [ComponentId](#cfn-ec2-networkinsightsanalysis-alternatepathhint-componentid): String
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-alternatepathhint-properties"></a>

`ComponentArn`  <a name="cfn-ec2-networkinsightsanalysis-alternatepathhint-componentarn"></a>
The Amazon Resource Name \(ARN\) of the component\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentId`  <a name="cfn-ec2-networkinsightsanalysis-alternatepathhint-componentid"></a>
The ID of the component\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)