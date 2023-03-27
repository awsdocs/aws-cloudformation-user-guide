# AWS::DMS::Endpoint RedshiftSettings<a name="aws-properties-dms-endpoint-redshiftsettings"></a>

Provides information that defines an Amazon Redshift endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For more information about other available settings, see [ Extra connection attributes when using Amazon Redshift as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Redshift.html#CHAP_Target.Redshift.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-redshiftsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-redshiftsettings-syntax.json"></a>

```
{
  "[AcceptAnyDate](#cfn-dms-endpoint-redshiftsettings-acceptanydate)" : Boolean,
  "[AfterConnectScript](#cfn-dms-endpoint-redshiftsettings-afterconnectscript)" : String,
  "[BucketFolder](#cfn-dms-endpoint-redshiftsettings-bucketfolder)" : String,
  "[BucketName](#cfn-dms-endpoint-redshiftsettings-bucketname)" : String,
  "[CaseSensitiveNames](#cfn-dms-endpoint-redshiftsettings-casesensitivenames)" : Boolean,
  "[CompUpdate](#cfn-dms-endpoint-redshiftsettings-compupdate)" : Boolean,
  "[ConnectionTimeout](#cfn-dms-endpoint-redshiftsettings-connectiontimeout)" : Integer,
  "[DateFormat](#cfn-dms-endpoint-redshiftsettings-dateformat)" : String,
  "[EmptyAsNull](#cfn-dms-endpoint-redshiftsettings-emptyasnull)" : Boolean,
  "[EncryptionMode](#cfn-dms-endpoint-redshiftsettings-encryptionmode)" : String,
  "[ExplicitIds](#cfn-dms-endpoint-redshiftsettings-explicitids)" : Boolean,
  "[FileTransferUploadStreams](#cfn-dms-endpoint-redshiftsettings-filetransferuploadstreams)" : Integer,
  "[LoadTimeout](#cfn-dms-endpoint-redshiftsettings-loadtimeout)" : Integer,
  "[MaxFileSize](#cfn-dms-endpoint-redshiftsettings-maxfilesize)" : Integer,
  "[RemoveQuotes](#cfn-dms-endpoint-redshiftsettings-removequotes)" : Boolean,
  "[ReplaceChars](#cfn-dms-endpoint-redshiftsettings-replacechars)" : String,
  "[ReplaceInvalidChars](#cfn-dms-endpoint-redshiftsettings-replaceinvalidchars)" : String,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-redshiftsettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-redshiftsettings-secretsmanagersecretid)" : String,
  "[ServerSideEncryptionKmsKeyId](#cfn-dms-endpoint-redshiftsettings-serversideencryptionkmskeyid)" : String,
  "[ServiceAccessRoleArn](#cfn-dms-endpoint-redshiftsettings-serviceaccessrolearn)" : String,
  "[TimeFormat](#cfn-dms-endpoint-redshiftsettings-timeformat)" : String,
  "[TrimBlanks](#cfn-dms-endpoint-redshiftsettings-trimblanks)" : Boolean,
  "[TruncateColumns](#cfn-dms-endpoint-redshiftsettings-truncatecolumns)" : Boolean,
  "[WriteBufferSize](#cfn-dms-endpoint-redshiftsettings-writebuffersize)" : Integer
}
```

### YAML<a name="aws-properties-dms-endpoint-redshiftsettings-syntax.yaml"></a>

```
  [AcceptAnyDate](#cfn-dms-endpoint-redshiftsettings-acceptanydate): Boolean
  [AfterConnectScript](#cfn-dms-endpoint-redshiftsettings-afterconnectscript): String
  [BucketFolder](#cfn-dms-endpoint-redshiftsettings-bucketfolder): String
  [BucketName](#cfn-dms-endpoint-redshiftsettings-bucketname): String
  [CaseSensitiveNames](#cfn-dms-endpoint-redshiftsettings-casesensitivenames): Boolean
  [CompUpdate](#cfn-dms-endpoint-redshiftsettings-compupdate): Boolean
  [ConnectionTimeout](#cfn-dms-endpoint-redshiftsettings-connectiontimeout): Integer
  [DateFormat](#cfn-dms-endpoint-redshiftsettings-dateformat): String
  [EmptyAsNull](#cfn-dms-endpoint-redshiftsettings-emptyasnull): Boolean
  [EncryptionMode](#cfn-dms-endpoint-redshiftsettings-encryptionmode): String
  [ExplicitIds](#cfn-dms-endpoint-redshiftsettings-explicitids): Boolean
  [FileTransferUploadStreams](#cfn-dms-endpoint-redshiftsettings-filetransferuploadstreams): Integer
  [LoadTimeout](#cfn-dms-endpoint-redshiftsettings-loadtimeout): Integer
  [MaxFileSize](#cfn-dms-endpoint-redshiftsettings-maxfilesize): Integer
  [RemoveQuotes](#cfn-dms-endpoint-redshiftsettings-removequotes): Boolean
  [ReplaceChars](#cfn-dms-endpoint-redshiftsettings-replacechars): String
  [ReplaceInvalidChars](#cfn-dms-endpoint-redshiftsettings-replaceinvalidchars): String
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-redshiftsettings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-redshiftsettings-secretsmanagersecretid): String
  [ServerSideEncryptionKmsKeyId](#cfn-dms-endpoint-redshiftsettings-serversideencryptionkmskeyid): String
  [ServiceAccessRoleArn](#cfn-dms-endpoint-redshiftsettings-serviceaccessrolearn): String
  [TimeFormat](#cfn-dms-endpoint-redshiftsettings-timeformat): String
  [TrimBlanks](#cfn-dms-endpoint-redshiftsettings-trimblanks): Boolean
  [TruncateColumns](#cfn-dms-endpoint-redshiftsettings-truncatecolumns): Boolean
  [WriteBufferSize](#cfn-dms-endpoint-redshiftsettings-writebuffersize): Integer
```

## Properties<a name="aws-properties-dms-endpoint-redshiftsettings-properties"></a>

`AcceptAnyDate`  <a name="cfn-dms-endpoint-redshiftsettings-acceptanydate"></a>
A value that indicates to allow any date format, including invalid formats such as 00/00/00 00:00:00, to be loaded without generating an error\. You can choose `true` or `false` \(the default\)\.  
This parameter applies only to TIMESTAMP and DATE columns\. Always use ACCEPTANYDATE with the DATEFORMAT parameter\. If the date format for the data doesn't match the DATEFORMAT specification, Amazon Redshift inserts a NULL value into that field\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AfterConnectScript`  <a name="cfn-dms-endpoint-redshiftsettings-afterconnectscript"></a>
Code to run after connecting\. This parameter should contain the code itself, not the name of a file containing the code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketFolder`  <a name="cfn-dms-endpoint-redshiftsettings-bucketfolder"></a>
An S3 folder where the comma\-separated\-value \(\.csv\) files are stored before being uploaded to the target Redshift cluster\.   
For full load mode, AWS DMS converts source records into \.csv files and loads them to the *BucketFolder/TableID* path\. AWS DMS uses the Redshift `COPY` command to upload the \.csv files to the target table\. The files are deleted once the `COPY` operation has finished\. For more information, see [COPY](https://docs.aws.amazon.com/redshift/latest/dg/r_COPY.html) in the *Amazon Redshift Database Developer Guide*\.  
For change\-data\-capture \(CDC\) mode, AWS DMS creates a *NetChanges* table, and loads the \.csv files to this *BucketFolder/NetChangesTableID* path\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketName`  <a name="cfn-dms-endpoint-redshiftsettings-bucketname"></a>
The name of the intermediate S3 bucket used to store \.csv files before uploading data to Redshift\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaseSensitiveNames`  <a name="cfn-dms-endpoint-redshiftsettings-casesensitivenames"></a>
If Amazon Redshift is configured to support case sensitive schema names, set `CaseSensitiveNames` to `true`\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CompUpdate`  <a name="cfn-dms-endpoint-redshiftsettings-compupdate"></a>
If you set `CompUpdate` to `true` Amazon Redshift applies automatic compression if the table is empty\. This applies even if the table columns already have encodings other than `RAW`\. If you set `CompUpdate` to `false`, automatic compression is disabled and existing column encodings aren't changed\. The default is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionTimeout`  <a name="cfn-dms-endpoint-redshiftsettings-connectiontimeout"></a>
A value that sets the amount of time to wait \(in milliseconds\) before timing out, beginning from when you initially establish a connection\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateFormat`  <a name="cfn-dms-endpoint-redshiftsettings-dateformat"></a>
The date format that you are using\. Valid values are `auto` \(case\-sensitive\), your date format string enclosed in quotes, or NULL\. If this parameter is left unset \(NULL\), it defaults to a format of 'YYYY\-MM\-DD'\. Using `auto` recognizes most strings, even some that aren't supported when you use a date format string\.   
If your date and time values use formats different from each other, set this to `auto`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmptyAsNull`  <a name="cfn-dms-endpoint-redshiftsettings-emptyasnull"></a>
A value that specifies whether AWS DMS should migrate empty CHAR and VARCHAR fields as NULL\. A value of `true` sets empty CHAR and VARCHAR fields to null\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionMode`  <a name="cfn-dms-endpoint-redshiftsettings-encryptionmode"></a>
The type of server\-side encryption that you want to use for your data\. This encryption type is part of the endpoint settings or the extra connections attributes for Amazon S3\. You can choose either `SSE_S3` \(the default\) or `SSE_KMS`\.   
For the `ModifyEndpoint` operation, you can change the existing value of the `EncryptionMode` parameter from `SSE_KMS` to `SSE_S3`\. But you can’t change the existing value from `SSE_S3` to `SSE_KMS`\.
To use `SSE_S3`, create an AWS Identity and Access Management \(IAM\) role with a policy that allows `"arn:aws:s3:::*"` to use the following actions: `"s3:PutObject", "s3:ListBucket"`   
*Required*: No  
*Type*: String  
*Allowed values*: `sse-kms | sse-s3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExplicitIds`  <a name="cfn-dms-endpoint-redshiftsettings-explicitids"></a>
This setting is only valid for a full\-load migration task\. Set `ExplicitIds` to `true` to have tables with `IDENTITY` columns override their auto\-generated values with explicit values loaded from the source data files used to populate the tables\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileTransferUploadStreams`  <a name="cfn-dms-endpoint-redshiftsettings-filetransferuploadstreams"></a>
The number of threads used to upload a single file\. This parameter accepts a value from 1 through 64\. It defaults to 10\.  
The number of parallel streams used to upload a single \.csv file to an S3 bucket using S3 Multipart Upload\. For more information, see [Multipart upload overview](https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html)\.   
 `FileTransferUploadStreams` accepts a value from 1 through 64\. It defaults to 10\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadTimeout`  <a name="cfn-dms-endpoint-redshiftsettings-loadtimeout"></a>
The amount of time to wait \(in milliseconds\) before timing out of operations performed by AWS DMS on a Redshift cluster, such as Redshift COPY, INSERT, DELETE, and UPDATE\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxFileSize`  <a name="cfn-dms-endpoint-redshiftsettings-maxfilesize"></a>
The maximum size \(in KB\) of any \.csv file used to load data on an S3 bucket and transfer data to Amazon Redshift\. It defaults to 1048576KB \(1 GB\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveQuotes`  <a name="cfn-dms-endpoint-redshiftsettings-removequotes"></a>
A value that specifies to remove surrounding quotation marks from strings in the incoming data\. All characters within the quotation marks, including delimiters, are retained\. Choose `true` to remove quotation marks\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceChars`  <a name="cfn-dms-endpoint-redshiftsettings-replacechars"></a>
A value that specifies to replaces the invalid characters specified in `ReplaceInvalidChars`, substituting the specified characters instead\. The default is `"?"`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceInvalidChars`  <a name="cfn-dms-endpoint-redshiftsettings-replaceinvalidchars"></a>
A list of characters that you want to replace\. Use with `ReplaceChars`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-redshiftsettings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret`\. The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value of the AWS Secrets Manager secret that allows access to the Amazon Redshift endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-redshiftsettings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the Amazon Redshift endpoint connection details\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerSideEncryptionKmsKeyId`  <a name="cfn-dms-endpoint-redshiftsettings-serversideencryptionkmskeyid"></a>
The AWS KMS key ID\. If you are using `SSE_KMS` for the `EncryptionMode`, provide this key ID\. The key that you use needs an attached policy that enables IAM user permissions and allows use of the key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-redshiftsettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that has access to the Amazon Redshift service\. The role must allow the `iam:PassRole` action\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeFormat`  <a name="cfn-dms-endpoint-redshiftsettings-timeformat"></a>
The time format that you want to use\. Valid values are `auto` \(case\-sensitive\), `'timeformat_string'`, `'epochsecs'`, or `'epochmillisecs'`\. It defaults to 10\. Using `auto` recognizes most strings, even some that aren't supported when you use a time format string\.   
If your date and time values use formats different from each other, set this parameter to `auto`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrimBlanks`  <a name="cfn-dms-endpoint-redshiftsettings-trimblanks"></a>
A value that specifies to remove the trailing white space characters from a VARCHAR string\. This parameter applies only to columns with a VARCHAR data type\. Choose `true` to remove unneeded white space\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TruncateColumns`  <a name="cfn-dms-endpoint-redshiftsettings-truncatecolumns"></a>
A value that specifies to truncate data in columns to the appropriate number of characters, so that the data fits in the column\. This parameter applies only to columns with a VARCHAR or CHAR data type, and rows with a size of 4 MB or less\. Choose `true` to truncate data\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriteBufferSize`  <a name="cfn-dms-endpoint-redshiftsettings-writebuffersize"></a>
The size \(in KB\) of the in\-memory file write buffer used when generating \.csv files on the local disk at the DMS replication instance\. The default value is 1000 \(buffer size is 1000KB\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)