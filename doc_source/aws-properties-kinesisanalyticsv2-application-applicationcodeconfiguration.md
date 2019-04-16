# Amazon Kinesis Data Analytics Application ApplicationCodeConfiguration<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-description"></a>The `ApplicationCodeConfiguration` property type specifies a code configuration for a Java\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-inheritance"></a> `ApplicationCodeConfiguration` is a property of the [ApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-syntax.json"></a>

```
{
  "[CodeContentType](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontenttype)" : String,
  "[CodeContent](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontent)" : [*CodeContent*](aws-properties-kinesisanalyticsv2-application-codecontent.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-syntax.yaml"></a>

```
[CodeContentType](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontenttype): String
[CodeContent](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontent): [*CodeContent*](aws-properties-kinesisanalyticsv2-application-codecontent.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-properties"></a>

`CodeContentType`  <a name="cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontenttype"></a>
The location and type of the application code\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CodeContent`  <a name="cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontent"></a>
Specifies whether the code content is in text or zip format\.  
 *Required*: Yes  
 *Type*: [CodeContent](aws-properties-kinesisanalyticsv2-application-codecontent.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 