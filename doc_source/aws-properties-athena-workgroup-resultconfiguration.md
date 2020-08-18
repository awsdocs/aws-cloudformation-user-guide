# AWS::Athena::WorkGroup ResultConfiguration<a name="aws-properties-athena-workgroup-resultconfiguration"></a>

The location in Amazon S3 where query results are stored and the encryption option, if any, used for query results\. These are known as "client\-side settings"\. If workgroup settings override client\-side settings, then the query uses the workgroup settings\.

## Syntax<a name="aws-properties-athena-workgroup-resultconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-resultconfiguration-syntax.json"></a>

```
{
  "[EncryptionConfiguration](#cfn-athena-workgroup-resultconfiguration-encryptionconfiguration)" : EncryptionConfiguration,
  "[OutputLocation](#cfn-athena-workgroup-resultconfiguration-outputlocation)" : String
}
```

### YAML<a name="aws-properties-athena-workgroup-resultconfiguration-syntax.yaml"></a>

```
  [EncryptionConfiguration](#cfn-athena-workgroup-resultconfiguration-encryptionconfiguration): 
    EncryptionConfiguration
  [OutputLocation](#cfn-athena-workgroup-resultconfiguration-outputlocation): String
```

## Properties<a name="aws-properties-athena-workgroup-resultconfiguration-properties"></a>

`EncryptionConfiguration`  <a name="cfn-athena-workgroup-resultconfiguration-encryptionconfiguration"></a>
If query results are encrypted in Amazon S3, indicates the encryption option used \(for example, `SSE-KMS` or `CSE-KMS`\) and key information\. This is a client\-side setting\. If workgroup settings override client\-side settings, then the query uses the encryption configuration that is specified for the workgroup, and also uses the location for storing query results specified in the workgroup\. See [EnforceWorkGroupConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-athena-workgroup-workgroupconfigurationupdates.html#cfn-athena-workgroup-workgroupconfigurationupdates-enforceworkgroupconfiguration) and [Workgroup Settings Override Client\-Side Settings](https://docs.aws.amazon.com/athena/latest/ug/workgroups-settings-override.html)\.  
*Required*: No  
*Type*: [EncryptionConfiguration](aws-properties-athena-workgroup-encryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputLocation`  <a name="cfn-athena-workgroup-resultconfiguration-outputlocation"></a>
The location in Amazon S3 where your query results are stored, such as `s3://path/to/query/bucket/`\. To run a query, you must specify the query results location using either a client\-side setting for individual queries or a location specified by the workgroup\. If workgroup settings override client\-side settings, then the query uses the location specified for the workgroup\. If no query location is set, Athena issues an error\. For more information, see [Working with Query Results, Output Files, and Query History](https://docs.aws.amazon.com/athena/latest/ug/querying.html) and [EnforceWorkGroupConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-athena-workgroup-workgroupconfigurationupdates.html#cfn-athena-workgroup-workgroupconfigurationupdates-enforceworkgroupconfiguration)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)