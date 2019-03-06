# Amazon Kinesis Data Analytics Application CodeContent<a name="aws-properties-kinesisanalyticsv2-application-codecontent"></a>

<a name="aws-properties-kinesisanalyticsv2-application-codecontent-description"></a>The `CodeContent` property type specifies either the application code, or the location of the application code, for a Java\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-codecontent-inheritance"></a> `CodeContent` is a property of the [ApplicationCodeConfiguration](aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-codecontent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-codecontent-syntax.json"></a>

```
{
  "[ZipFileContent](#cfn-kinesisanalyticsv2-application-codecontent-zipfilecontent)" : String,
  "[S3ContentLocation](#cfn-kinesisanalyticsv2-application-codecontent-s3contentlocation)" : [*S3ContentLocation*](aws-properties-kinesisanalyticsv2-application-s3contentlocation.md),
  "[TextContent](#cfn-kinesisanalyticsv2-application-codecontent-textcontent)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-codecontent-syntax.yaml"></a>

```
[ZipFileContent](#cfn-kinesisanalyticsv2-application-codecontent-zipfilecontent): String
[S3ContentLocation](#cfn-kinesisanalyticsv2-application-codecontent-s3contentlocation): [*S3ContentLocation*](aws-properties-kinesisanalyticsv2-application-s3contentlocation.md)
[TextContent](#cfn-kinesisanalyticsv2-application-codecontent-textcontent): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-codecontent-properties"></a>

`ZipFileContent`  <a name="cfn-kinesisanalyticsv2-application-codecontent-zipfilecontent"></a>
The zip\-format code for a Java\-based Kinesis Data Analytics application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3ContentLocation`  <a name="cfn-kinesisanalyticsv2-application-codecontent-s3contentlocation"></a>
Information about the Amazon S3 bucket containing the application code\.  
 *Required*: No  
 *Type*: [S3ContentLocation](aws-properties-kinesisanalyticsv2-application-s3contentlocation.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TextContent`  <a name="cfn-kinesisanalyticsv2-application-codecontent-textcontent"></a>
The text\-format code for a Java\-based Kinesis Data Analytics application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 