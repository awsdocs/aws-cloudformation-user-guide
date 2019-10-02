# AWS::PinpointEmail::ConfigurationSetEventDestination CloudWatchDestination<a name="aws-properties-pinpointemail-configurationseteventdestination-cloudwatchdestination"></a>

An object that defines an Amazon CloudWatch destination for email events\. You can use Amazon CloudWatch to monitor and gain insights on your email sending metrics\.

## Syntax<a name="aws-properties-pinpointemail-configurationseteventdestination-cloudwatchdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationseteventdestination-cloudwatchdestination-syntax.json"></a>

```
{
  "[DimensionConfigurations](#cfn-pinpointemail-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations)" : [ [DimensionConfiguration](aws-properties-pinpointemail-configurationseteventdestination-dimensionconfiguration.md), ... ]
}
```

### YAML<a name="aws-properties-pinpointemail-configurationseteventdestination-cloudwatchdestination-syntax.yaml"></a>

```
  [DimensionConfigurations](#cfn-pinpointemail-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations): 
    - [DimensionConfiguration](aws-properties-pinpointemail-configurationseteventdestination-dimensionconfiguration.md)
```

## Properties<a name="aws-properties-pinpointemail-configurationseteventdestination-cloudwatchdestination-properties"></a>

`DimensionConfigurations`  <a name="cfn-pinpointemail-configurationseteventdestination-cloudwatchdestination-dimensionconfigurations"></a>
An array of objects that define the dimensions to use when you send email events to Amazon CloudWatch\.  
*Required*: No  
*Type*: List of [DimensionConfiguration](aws-properties-pinpointemail-configurationseteventdestination-dimensionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
