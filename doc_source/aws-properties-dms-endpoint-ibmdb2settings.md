# AWS::DMS::Endpoint IbmDb2Settings<a name="aws-properties-dms-endpoint-ibmdb2settings"></a>

Provides information that defines an IBMDB2 endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For more information about other available settings, see [ Extra connection attributes when using Db2 LUW as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.DB2.html#CHAP_Source.DB2.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-ibmdb2settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-ibmdb2settings-syntax.json"></a>

```
{
  "[CurrentLsn](#cfn-dms-endpoint-ibmdb2settings-currentlsn)" : String,
  "[MaxKBytesPerRead](#cfn-dms-endpoint-ibmdb2settings-maxkbytesperread)" : Integer,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-ibmdb2settings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-ibmdb2settings-secretsmanagersecretid)" : String,
  "[SetDataCaptureChanges](#cfn-dms-endpoint-ibmdb2settings-setdatacapturechanges)" : Boolean
}
```

### YAML<a name="aws-properties-dms-endpoint-ibmdb2settings-syntax.yaml"></a>

```
  [CurrentLsn](#cfn-dms-endpoint-ibmdb2settings-currentlsn): String
  [MaxKBytesPerRead](#cfn-dms-endpoint-ibmdb2settings-maxkbytesperread): Integer
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-ibmdb2settings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-ibmdb2settings-secretsmanagersecretid): String
  [SetDataCaptureChanges](#cfn-dms-endpoint-ibmdb2settings-setdatacapturechanges): Boolean
```

## Properties<a name="aws-properties-dms-endpoint-ibmdb2settings-properties"></a>

`CurrentLsn`  <a name="cfn-dms-endpoint-ibmdb2settings-currentlsn"></a>
For ongoing replication \(CDC\), use CurrentLSN to specify a log sequence number \(LSN\) where you want the replication to start\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxKBytesPerRead`  <a name="cfn-dms-endpoint-ibmdb2settings-maxkbytesperread"></a>
Maximum number of bytes per read, as a NUMBER value\. The default is 64 KB\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-ibmdb2settings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret`\. The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value ofthe AWS Secrets Manager secret that allows access to the Db2 LUW endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-ibmdb2settings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the IBMDB2 endpoint connection details\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SetDataCaptureChanges`  <a name="cfn-dms-endpoint-ibmdb2settings-setdatacapturechanges"></a>
Enables ongoing replication \(CDC\) as a BOOLEAN value\. The default is true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)