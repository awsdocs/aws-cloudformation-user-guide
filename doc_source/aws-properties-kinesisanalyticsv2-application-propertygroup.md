# Amazon Kinesis Data Analytics Application PropertyGroup<a name="aws-properties-kinesisanalyticsv2-application-propertygroup"></a>

<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-description"></a>The `PropertyGroup` property type specifies property key\-value pairs passed into a Java\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-inheritance"></a> `PropertyGroup` is a property of the [EnvironmentProperties](aws-properties-kinesisanalyticsv2-application-environmentproperties.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-syntax.json"></a>

```
{
  "[PropertyMap](#cfn-kinesisanalyticsv2-application-propertygroup-propertymap)" : Json,
  "[PropertyGroupId](#cfn-kinesisanalyticsv2-application-propertygroup-propertygroupid)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-syntax.yaml"></a>

```
[PropertyMap](#cfn-kinesisanalyticsv2-application-propertygroup-propertymap): Json
[PropertyGroupId](#cfn-kinesisanalyticsv2-application-propertygroup-propertygroupid): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-properties"></a>

`PropertyMap`  <a name="cfn-kinesisanalyticsv2-application-propertygroup-propertymap"></a>
Describes the value of an application execution property key\-value pair\.  
 *Required*: No  
 *Type*: Json  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PropertyGroupId`  <a name="cfn-kinesisanalyticsv2-application-propertygroup-propertygroupid"></a>
Describes the key of an application execution property key\-value pair\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 