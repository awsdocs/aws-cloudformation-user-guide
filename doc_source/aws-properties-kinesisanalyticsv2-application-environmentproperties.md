# Amazon Kinesis Data Analytics Application EnvironmentProperties<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties"></a>

<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-description"></a>The `EnvironmentProperties` property type specifies execution properties for a Java\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-inheritance"></a> `EnvironmentProperties` is a property of the [ApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-syntax.json"></a>

```
{
  "[PropertyGroups](#cfn-kinesisanalyticsv2-application-environmentproperties-propertygroups)" : [ [*PropertyGroup*](aws-properties-kinesisanalyticsv2-application-propertygroup.md), ... ]
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-syntax.yaml"></a>

```
[PropertyGroups](#cfn-kinesisanalyticsv2-application-environmentproperties-propertygroups): 
  - [*PropertyGroup*](aws-properties-kinesisanalyticsv2-application-propertygroup.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-environmentproperties-properties"></a>

`PropertyGroups`  <a name="cfn-kinesisanalyticsv2-application-environmentproperties-propertygroups"></a>
Describes the execution property groups\.  
 *Required*: No  
 *Type*: List of [PropertyGroup](aws-properties-kinesisanalyticsv2-application-propertygroup.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 