# AWS::SES::ConfigurationSetEventDestination CloudWatchDestination<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination"></a>

Contains information associated with an Amazon CloudWatch event destination to which email sending events are published\.

Event destinations, such as Amazon CloudWatch, are associated with configuration sets, which enable you to publish email sending events\. For information about using configuration sets, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/monitor-sending-activity.html)\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-syntax.json"></a>

```
{
  "[DimensionConfigurations](#cfn-ses-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations)" : [ DimensionConfiguration, ... ]
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-syntax.yaml"></a>

```
  [DimensionConfigurations](#cfn-ses-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations): 
    - DimensionConfiguration
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-properties"></a>

`DimensionConfigurations`  <a name="cfn-ses-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations"></a>
A list of dimensions upon which to categorize your emails when you publish email sending events to Amazon CloudWatch\.  
*Required*: No  
*Type*: List of [DimensionConfiguration](aws-properties-ses-configurationseteventdestination-dimensionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)