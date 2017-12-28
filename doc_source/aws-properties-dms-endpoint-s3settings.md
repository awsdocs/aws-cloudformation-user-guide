# AWS DMS Endpoint S3Settings<a name="aws-properties-dms-endpoint-s3settings"></a>

Use the `S3Settings` property to specify settings for an Amazon S3 endpoint for a  resource\.

## Syntax<a name="w3ab2c21c14d504b5"></a>

### JSON<a name="aws-properties-dms-endpoint-s3settings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-bucketfolder)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-bucketname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-compressiontype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-csvdelimiter)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-csvrowdelimiter)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-externaltabledefinition)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-serviceaccessrolearn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-s3settings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-bucketfolder): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-bucketname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-compressiontype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-csvdelimiter): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-csvrowdelimiter): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-externaltabledefinition): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings-serviceaccessrolearn): String
```

## Properties<a name="w3ab2c21c14d504b7"></a>

For more information about option settings, see [Using Amazon S3 as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html) in the *AWS Database Migration Service User Guide*

`BucketFolder`  
An optional parameter to set a folder name in the S3 bucket\. If provided, tables are created in the path <bucketFolder>/<schema\_name>/<table\_name>/\. If this parameter is not specified, then the path used is <schema\_name>/<table\_name>/\.   
*Required: *No  
*Type*: String

`BucketName`  
The name of the Amazon S3 bucket\.  
*Required: *No  
*Type*: String

`CompressionType`  
 An optional parameter to use GZIP to compress the target files\. Set to GZIP to compress the target files\. Set to NONE \(the default\) or do not use to leave the files uncompressed\.   
Valid Values: NONE | GZIP  
*Required: *No  
*Type*: String

`CsvDelimiter`  
 The delimiter used to separate columns in the source files\. The default is a comma\.  
*Required: *No  
*Type*: String

`CsvRowDelimiter`  
 The delimiter used to separate rows in the source files\. The default is a carriage return \(\\n\)\.  
*Required: *No  
*Type*: String

`ExternalTableDefinition`  
The definition of the external table\.  
*Required: *No  
*Type*: String

`ServiceAccessRoleArn`  
The Amazon Resource Name \(ARN\) used by the service access IAM role\.  
*Required: *No  
*Type*: String