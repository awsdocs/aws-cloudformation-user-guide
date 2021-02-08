# AWS::Athena::WorkGroup WorkGroupConfigurationUpdates<a name="aws-properties-athena-workgroup-workgroupconfigurationupdates"></a>

The configuration information that will be updated for this workgroup, which includes the location in Amazon S3 where query results are stored, the encryption option, if any, used for query results, whether the Amazon CloudWatch Metrics are enabled for the workgroup, whether the workgroup settings override the client\-side settings, and the data usage limit for the amount of bytes scanned per query, if it is specified\.

## Syntax<a name="aws-properties-athena-workgroup-workgroupconfigurationupdates-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-workgroupconfigurationupdates-syntax.json"></a>

```
{
  "[BytesScannedCutoffPerQuery](#cfn-athena-workgroup-workgroupconfigurationupdates-bytesscannedcutoffperquery)" : Integer,
  "[EnforceWorkGroupConfiguration](#cfn-athena-workgroup-workgroupconfigurationupdates-enforceworkgroupconfiguration)" : Boolean,
  "[PublishCloudWatchMetricsEnabled](#cfn-athena-workgroup-workgroupconfigurationupdates-publishcloudwatchmetricsenabled)" : Boolean,
  "[RemoveBytesScannedCutoffPerQuery](#cfn-athena-workgroup-workgroupconfigurationupdates-removebytesscannedcutoffperquery)" : Boolean,
  "[RequesterPaysEnabled](#cfn-athena-workgroup-workgroupconfigurationupdates-requesterpaysenabled)" : Boolean,
  "[ResultConfigurationUpdates](#cfn-athena-workgroup-workgroupconfigurationupdates-resultconfigurationupdates)" : ResultConfigurationUpdates
}
```

### YAML<a name="aws-properties-athena-workgroup-workgroupconfigurationupdates-syntax.yaml"></a>

```
  [BytesScannedCutoffPerQuery](#cfn-athena-workgroup-workgroupconfigurationupdates-bytesscannedcutoffperquery): Integer
  [EnforceWorkGroupConfiguration](#cfn-athena-workgroup-workgroupconfigurationupdates-enforceworkgroupconfiguration): Boolean
  [PublishCloudWatchMetricsEnabled](#cfn-athena-workgroup-workgroupconfigurationupdates-publishcloudwatchmetricsenabled): Boolean
  [RemoveBytesScannedCutoffPerQuery](#cfn-athena-workgroup-workgroupconfigurationupdates-removebytesscannedcutoffperquery): Boolean
  [RequesterPaysEnabled](#cfn-athena-workgroup-workgroupconfigurationupdates-requesterpaysenabled): Boolean
  [ResultConfigurationUpdates](#cfn-athena-workgroup-workgroupconfigurationupdates-resultconfigurationupdates): 
    ResultConfigurationUpdates
```

## Properties<a name="aws-properties-athena-workgroup-workgroupconfigurationupdates-properties"></a>

`BytesScannedCutoffPerQuery`  <a name="cfn-athena-workgroup-workgroupconfigurationupdates-bytesscannedcutoffperquery"></a>
The upper limit \(cutoff\) for the amount of bytes a single query in a workgroup is allowed to scan\.  
This property currently supports integer types\. Support for long values is planned\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnforceWorkGroupConfiguration`  <a name="cfn-athena-workgroup-workgroupconfigurationupdates-enforceworkgroupconfiguration"></a>
If set to "true", the settings for the workgroup override client\-side settings\. If set to "false" client\-side settings are used\. For more information, see [Workgroup Settings Override Client\-Side Settings](https://docs.aws.amazon.com/athena/latest/ug/workgroups-settings-override.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublishCloudWatchMetricsEnabled`  <a name="cfn-athena-workgroup-workgroupconfigurationupdates-publishcloudwatchmetricsenabled"></a>
Indicates whether this workgroup enables publishing metrics to Amazon CloudWatch\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveBytesScannedCutoffPerQuery`  <a name="cfn-athena-workgroup-workgroupconfigurationupdates-removebytesscannedcutoffperquery"></a>
Indicates that the data usage control limit per query is removed\. See [BytesScannedCutoffPerQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-athena-workgroup-workgroupconfigurationupdates.html#cfn-athena-workgroup-workgroupconfigurationupdates-bytesscannedcutoffperquery)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequesterPaysEnabled`  <a name="cfn-athena-workgroup-workgroupconfigurationupdates-requesterpaysenabled"></a>
If set to `true`, allows members assigned to a workgroup to specify Amazon S3 Requester Pays buckets in queries\. If set to `false`, workgroup members cannot query data from Requester Pays buckets, and queries that retrieve data from Requester Pays buckets cause an error\. The default is `false`\. For more information about Requester Pays buckets, see [Requester Pays Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/RequesterPaysBuckets.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResultConfigurationUpdates`  <a name="cfn-athena-workgroup-workgroupconfigurationupdates-resultconfigurationupdates"></a>
The result configuration information about the queries in this workgroup that will be updated\. Includes the updated results location and an updated option for encrypting query results\.  
*Required*: No  
*Type*: [ResultConfigurationUpdates](aws-properties-athena-workgroup-resultconfigurationupdates.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)