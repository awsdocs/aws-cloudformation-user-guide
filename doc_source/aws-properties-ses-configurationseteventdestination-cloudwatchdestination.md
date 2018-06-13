# Amazon Simple Email Service ConfigurationSetEventDestination CloudWatchDestination<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination"></a>

<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-description"></a>The `CloudWatchDestination` property type specifies information associated with an CloudWatch event destination to which email sending events are published in Amazon SES\.

<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-inheritance"></a> `CloudWatchDestination` is a property of the [Amazon SES ConfigurationSetEventDestination EventDestination](aws-properties-ses-configurationseteventdestination-eventdestination.md) property type\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-syntax.json"></a>

```
{
  "[DimensionConfigurations](#cfn-ses-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations)" : [ [*DimensionConfiguration*](aws-properties-ses-configurationseteventdestination-dimensionconfiguration.md), ... ]
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-syntax.yaml"></a>

```
[DimensionConfigurations](#cfn-ses-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations): 
  - [*DimensionConfiguration*](aws-properties-ses-configurationseteventdestination-dimensionconfiguration.md)
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-properties"></a>

`DimensionConfigurations`  <a name="cfn-ses-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations"></a>
A list of dimensions upon which to categorize your emails when you publish email sending events to CloudWatch\.  
 *Required*: No  
 *Type*: List of [Amazon SES ConfigurationSetEventDestination DimensionConfiguration](aws-properties-ses-configurationseteventdestination-dimensionconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-configurationseteventdestination-cloudwatchdestination-seealso"></a>
+ [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*
+ [CloudWatchDestination](http://docs.aws.amazon.com/ses/latest/APIReference/API_CloudWatchDestination.html) in the *Amazon Simple Email Service API Reference*