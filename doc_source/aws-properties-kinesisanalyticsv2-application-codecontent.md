# AWS::KinesisAnalyticsV2::Application CodeContent<a name="aws-properties-kinesisanalyticsv2-application-codecontent"></a>

Specifies either the application code, or the location of the application code, for a Flink\-based Kinesis Data Analytics application\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-codecontent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-codecontent-syntax.json"></a>

```
{
  "[S3ContentLocation](#cfn-kinesisanalyticsv2-application-codecontent-s3contentlocation)" : S3ContentLocation,
  "[TextContent](#cfn-kinesisanalyticsv2-application-codecontent-textcontent)" : String,
  "[ZipFileContent](#cfn-kinesisanalyticsv2-application-codecontent-zipfilecontent)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-codecontent-syntax.yaml"></a>

```
  [S3ContentLocation](#cfn-kinesisanalyticsv2-application-codecontent-s3contentlocation): 
    S3ContentLocation
  [TextContent](#cfn-kinesisanalyticsv2-application-codecontent-textcontent): String
  [ZipFileContent](#cfn-kinesisanalyticsv2-application-codecontent-zipfilecontent): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-codecontent-properties"></a>

`S3ContentLocation`  <a name="cfn-kinesisanalyticsv2-application-codecontent-s3contentlocation"></a>
Information about the Amazon S3 bucket containing the application code\.  
*Required*: No  
*Type*: [S3ContentLocation](aws-properties-kinesisanalyticsv2-application-s3contentlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextContent`  <a name="cfn-kinesisanalyticsv2-application-codecontent-textcontent"></a>
The text\-format code for a Flink\-based Kinesis Data Analytics application\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `102400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ZipFileContent`  <a name="cfn-kinesisanalyticsv2-application-codecontent-zipfilecontent"></a>
The zip\-format code for a Flink\-based Kinesis Data Analytics application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-codecontent--seealso"></a>
+  [CodeContent](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_CodeContent.html) in the *Amazon Kinesis Data Analytics API Reference* 

