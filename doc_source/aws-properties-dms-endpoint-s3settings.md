# AWS::DMS::Endpoint S3Settings<a name="aws-properties-dms-endpoint-s3settings"></a>

Settings for exporting data to Amazon S3\. 

## Syntax<a name="aws-properties-dms-endpoint-s3settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-s3settings-syntax.json"></a>

```
{
  "[BucketFolder](#cfn-dms-endpoint-s3settings-bucketfolder)" : String,
  "[BucketName](#cfn-dms-endpoint-s3settings-bucketname)" : String,
  "[CompressionType](#cfn-dms-endpoint-s3settings-compressiontype)" : String,
  "[CsvDelimiter](#cfn-dms-endpoint-s3settings-csvdelimiter)" : String,
  "[CsvRowDelimiter](#cfn-dms-endpoint-s3settings-csvrowdelimiter)" : String,
  "[ExternalTableDefinition](#cfn-dms-endpoint-s3settings-externaltabledefinition)" : String,
  "[ServiceAccessRoleArn](#cfn-dms-endpoint-s3settings-serviceaccessrolearn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-s3settings-syntax.yaml"></a>

```
  [BucketFolder](#cfn-dms-endpoint-s3settings-bucketfolder): String
  [BucketName](#cfn-dms-endpoint-s3settings-bucketname): String
  [CompressionType](#cfn-dms-endpoint-s3settings-compressiontype): String
  [CsvDelimiter](#cfn-dms-endpoint-s3settings-csvdelimiter): String
  [CsvRowDelimiter](#cfn-dms-endpoint-s3settings-csvrowdelimiter): String
  [ExternalTableDefinition](#cfn-dms-endpoint-s3settings-externaltabledefinition): String
  [ServiceAccessRoleArn](#cfn-dms-endpoint-s3settings-serviceaccessrolearn): String
```

## Properties<a name="aws-properties-dms-endpoint-s3settings-properties"></a>

`BucketFolder`  <a name="cfn-dms-endpoint-s3settings-bucketfolder"></a>
 An optional parameter to set a folder name in the S3 bucket\. If provided, tables are created in the path `<bucketFolder>/<schema_name>/<table_name>/`\. If this parameter is not specified, then the path used is `<schema_name>/<table_name>/`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketName`  <a name="cfn-dms-endpoint-s3settings-bucketname"></a>
 The name of the S3 bucket\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CompressionType`  <a name="cfn-dms-endpoint-s3settings-compressiontype"></a>
 An optional parameter to use GZIP to compress the target files\. Set to GZIP to compress the target files\. Set to NONE \(the default\) or do not use to leave the files uncompressed\. Applies to both CSV and PARQUET data formats\.   
*Required*: No  
*Type*: String  
*Allowed Values*: `gzip | none`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CsvDelimiter`  <a name="cfn-dms-endpoint-s3settings-csvdelimiter"></a>
 The delimiter used to separate columns in the source files\. The default is a comma\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CsvRowDelimiter`  <a name="cfn-dms-endpoint-s3settings-csvrowdelimiter"></a>
 The delimiter used to separate rows in the source files\. The default is a carriage return \(`\n`\)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExternalTableDefinition`  <a name="cfn-dms-endpoint-s3settings-externaltabledefinition"></a>
 The external table definition\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-s3settings-serviceaccessrolearn"></a>
 The Amazon Resource Name \(ARN\) used by the service access IAM role\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)