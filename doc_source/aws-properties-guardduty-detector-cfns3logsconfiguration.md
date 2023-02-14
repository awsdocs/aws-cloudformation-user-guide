# AWS::GuardDuty::Detector CFNS3LogsConfiguration<a name="aws-properties-guardduty-detector-cfns3logsconfiguration"></a>

Describes whether S3 data event logs will be enabled as a data source when the detector is created\.

## Syntax<a name="aws-properties-guardduty-detector-cfns3logsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-detector-cfns3logsconfiguration-syntax.json"></a>

```
{
  "[Enable](#cfn-guardduty-detector-cfns3logsconfiguration-enable)" : Boolean
}
```

### YAML<a name="aws-properties-guardduty-detector-cfns3logsconfiguration-syntax.yaml"></a>

```
  [Enable](#cfn-guardduty-detector-cfns3logsconfiguration-enable): Boolean
```

## Properties<a name="aws-properties-guardduty-detector-cfns3logsconfiguration-properties"></a>

`Enable`  <a name="cfn-guardduty-detector-cfns3logsconfiguration-enable"></a>
 The status of S3 data event logs as a data source\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)