# AWS::KinesisAnalyticsV2::Application EnvironmentProperties<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties"></a>

Describes execution properties for a Java\-based Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-syntax.json"></a>

```
{
  "[PropertyGroups](#cfn-kinesisanalyticsv2-application-environmentproperties-propertygroups)" : [ [PropertyGroup](aws-properties-kinesisanalyticsv2-application-propertygroup.md), ... ]
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-syntax.yaml"></a>

```
  [PropertyGroups](#cfn-kinesisanalyticsv2-application-environmentproperties-propertygroups): 
    - [PropertyGroup](aws-properties-kinesisanalyticsv2-application-propertygroup.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-properties"></a>

`PropertyGroups`  <a name="cfn-kinesisanalyticsv2-application-environmentproperties-propertygroups"></a>
Describes the execution property groups\.  
*Required*: No  
*Type*: List of [PropertyGroup](aws-properties-kinesisanalyticsv2-application-propertygroup.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties--seealso"></a>
+  [EnvironmentProperties](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_EnvironmentProperties.html) in the *Amazon Kinesis Data Analytics API Reference* 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
