# AWS::GuardDuty::Detector CFNScanEc2InstanceWithFindingsConfiguration<a name="aws-properties-guardduty-detector-cfnscanec2instancewithfindingsconfiguration"></a>

Describes whether Malware Protection for EC2 instances with findings will be enabled as a data source\.

## Syntax<a name="aws-properties-guardduty-detector-cfnscanec2instancewithfindingsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-detector-cfnscanec2instancewithfindingsconfiguration-syntax.json"></a>

```
{
  "[EbsVolumes](#cfn-guardduty-detector-cfnscanec2instancewithfindingsconfiguration-ebsvolumes)" : Boolean
}
```

### YAML<a name="aws-properties-guardduty-detector-cfnscanec2instancewithfindingsconfiguration-syntax.yaml"></a>

```
  [EbsVolumes](#cfn-guardduty-detector-cfnscanec2instancewithfindingsconfiguration-ebsvolumes): Boolean
```

## Properties<a name="aws-properties-guardduty-detector-cfnscanec2instancewithfindingsconfiguration-properties"></a>

`EbsVolumes`  <a name="cfn-guardduty-detector-cfnscanec2instancewithfindingsconfiguration-ebsvolumes"></a>
Describes the configuration for scanning EBS volumes as data source\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)