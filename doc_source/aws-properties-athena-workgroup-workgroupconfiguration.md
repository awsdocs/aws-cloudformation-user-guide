# AWS::Athena::WorkGroup WorkGroupConfiguration<a name="aws-properties-athena-workgroup-workgroupconfiguration"></a>

The configuration of the workgroup, which includes the location in Amazon S3 where query results are stored, the encryption option, if any, used for query results, whether Amazon CloudWatch Metrics are enabled for the workgroup, and the limit for the amount of bytes scanned \(cutoff\) per query, if it is specified\. The [EnforceWorkGroupConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-athena-workgroup-workgroupconfiguration.html#cfn-athena-workgroup-workgroupconfiguration-enforceworkgroupconfiguration) option determines whether workgroup settings override client\-side query settings\.

## Syntax<a name="aws-properties-athena-workgroup-workgroupconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-workgroupconfiguration-syntax.json"></a>

```
{
  "[BytesScannedCutoffPerQuery](#cfn-athena-workgroup-workgroupconfiguration-bytesscannedcutoffperquery)" : Integer,
  "[EnforceWorkGroupConfiguration](#cfn-athena-workgroup-workgroupconfiguration-enforceworkgroupconfiguration)" : Boolean,
  "[PublishCloudWatchMetricsEnabled](#cfn-athena-workgroup-workgroupconfiguration-publishcloudwatchmetricsenabled)" : Boolean,
  "[RequesterPaysEnabled](#cfn-athena-workgroup-workgroupconfiguration-requesterpaysenabled)" : Boolean,
  "[ResultConfiguration](#cfn-athena-workgroup-workgroupconfiguration-resultconfiguration)" : ResultConfiguration
}
```

### YAML<a name="aws-properties-athena-workgroup-workgroupconfiguration-syntax.yaml"></a>

```
  [BytesScannedCutoffPerQuery](#cfn-athena-workgroup-workgroupconfiguration-bytesscannedcutoffperquery): Integer
  [EnforceWorkGroupConfiguration](#cfn-athena-workgroup-workgroupconfiguration-enforceworkgroupconfiguration): Boolean
  [PublishCloudWatchMetricsEnabled](#cfn-athena-workgroup-workgroupconfiguration-publishcloudwatchmetricsenabled): Boolean
  [RequesterPaysEnabled](#cfn-athena-workgroup-workgroupconfiguration-requesterpaysenabled): Boolean
  [ResultConfiguration](#cfn-athena-workgroup-workgroupconfiguration-resultconfiguration): 
    ResultConfiguration
```

## Properties<a name="aws-properties-athena-workgroup-workgroupconfiguration-properties"></a>

`BytesScannedCutoffPerQuery`  <a name="cfn-athena-workgroup-workgroupconfiguration-bytesscannedcutoffperquery"></a>
The upper limit \(cutoff\) for the amount of bytes a single query in a workgroup is allowed to scan\.  
This property currently supports integer types\. Support for long values is planned\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnforceWorkGroupConfiguration`  <a name="cfn-athena-workgroup-workgroupconfiguration-enforceworkgroupconfiguration"></a>
If set to "true", the settings for the workgroup override client\-side settings\. If set to "false", client\-side settings are used\. For more information, see [Workgroup Settings Override Client\-Side Settings](https://docs.aws.amazon.com/athena/latest/ug/workgroups-settings-override.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublishCloudWatchMetricsEnabled`  <a name="cfn-athena-workgroup-workgroupconfiguration-publishcloudwatchmetricsenabled"></a>
Indicates that the Amazon CloudWatch metrics are enabled for the workgroup\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequesterPaysEnabled`  <a name="cfn-athena-workgroup-workgroupconfiguration-requesterpaysenabled"></a>
If set to `true`, allows members assigned to a workgroup to reference Amazon S3 Requester Pays buckets in queries\. If set to `false`, workgroup members cannot query data from Requester Pays buckets, and queries that retrieve data from Requester Pays buckets cause an error\. The default is `false`\. For more information about Requester Pays buckets, see [Requester Pays Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/RequesterPaysBuckets.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResultConfiguration`  <a name="cfn-athena-workgroup-workgroupconfiguration-resultconfiguration"></a>
Specifies the location in Amazon S3 where query results are stored and the encryption option, if any, used for query results\. For more information, see [Working with Query Results, Output Files, and Query History](https://docs.aws.amazon.com/athena/latest/ug/querying.html)\.  
*Required*: No  
*Type*: [ResultConfiguration](aws-properties-athena-workgroup-resultconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)