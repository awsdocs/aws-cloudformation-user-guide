# AWS::KinesisAnalyticsV2::Application PropertyGroup<a name="aws-properties-kinesisanalyticsv2-application-propertygroup"></a>

Property key\-value pairs passed into a Flink\-based Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-syntax.json"></a>

```
{
  "[PropertyGroupId](#cfn-kinesisanalyticsv2-application-propertygroup-propertygroupid)" : String,
  "[PropertyMap](#cfn-kinesisanalyticsv2-application-propertygroup-propertymap)" : Json
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-syntax.yaml"></a>

```
  [PropertyGroupId](#cfn-kinesisanalyticsv2-application-propertygroup-propertygroupid): String
  [PropertyMap](#cfn-kinesisanalyticsv2-application-propertygroup-propertymap): Json
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-propertygroup-properties"></a>

`PropertyGroupId`  <a name="cfn-kinesisanalyticsv2-application-propertygroup-propertygroupid"></a>
Describes the key of an application execution property key\-value pair\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyMap`  <a name="cfn-kinesisanalyticsv2-application-propertygroup-propertymap"></a>
Describes the value of an application execution property key\-value pair\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-propertygroup--seealso"></a>
+  [PropertyGroup](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_PropertyGroup.html) in the *Amazon Kinesis Data Analytics API Reference* 

