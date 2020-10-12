# AWS::Athena::WorkGroup ResultConfigurationUpdates<a name="aws-properties-athena-workgroup-resultconfigurationupdates"></a>

The information about the updates in the query results, such as output location and encryption configuration for the query results\.

## Syntax<a name="aws-properties-athena-workgroup-resultconfigurationupdates-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-resultconfigurationupdates-syntax.json"></a>

```
{
  "[EncryptionConfiguration](#cfn-athena-workgroup-resultconfigurationupdates-encryptionconfiguration)" : EncryptionConfiguration,
  "[OutputLocation](#cfn-athena-workgroup-resultconfigurationupdates-outputlocation)" : String,
  "[RemoveEncryptionConfiguration](#cfn-athena-workgroup-resultconfigurationupdates-removeencryptionconfiguration)" : Boolean,
  "[RemoveOutputLocation](#cfn-athena-workgroup-resultconfigurationupdates-removeoutputlocation)" : Boolean
}
```

### YAML<a name="aws-properties-athena-workgroup-resultconfigurationupdates-syntax.yaml"></a>

```
  [EncryptionConfiguration](#cfn-athena-workgroup-resultconfigurationupdates-encryptionconfiguration): 
    EncryptionConfiguration
  [OutputLocation](#cfn-athena-workgroup-resultconfigurationupdates-outputlocation): String
  [RemoveEncryptionConfiguration](#cfn-athena-workgroup-resultconfigurationupdates-removeencryptionconfiguration): Boolean
  [RemoveOutputLocation](#cfn-athena-workgroup-resultconfigurationupdates-removeoutputlocation): Boolean
```

## Properties<a name="aws-properties-athena-workgroup-resultconfigurationupdates-properties"></a>

`EncryptionConfiguration`  <a name="cfn-athena-workgroup-resultconfigurationupdates-encryptionconfiguration"></a>
The encryption configuration for the query results\.  
*Required*: No  
*Type*: [EncryptionConfiguration](aws-properties-athena-workgroup-encryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputLocation`  <a name="cfn-athena-workgroup-resultconfigurationupdates-outputlocation"></a>
The location in Amazon S3 where your query results are stored, such as `s3://path/to/query/bucket/`\. For more information, see [Query Results](https://docs.aws.amazon.com/athena/latest/ug/querying.html) If workgroup settings override client\-side settings, then the query uses the location for the query results and the encryption configuration that are specified for the workgroup\. The "workgroup settings override" is specified in EnforceWorkGroupConfiguration \(true/false\) in the WorkGroupConfiguration\. See [EnforceWorkGroupConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-athena-workgroup-workgroupconfigurationupdates.html#cfn-athena-workgroup-workgroupconfigurationupdates-enforceworkgroupconfiguration)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveEncryptionConfiguration`  <a name="cfn-athena-workgroup-resultconfigurationupdates-removeencryptionconfiguration"></a>
If set to "true", indicates that the previously\-specified encryption configuration \(also known as the client\-side setting\) for queries in this workgroup should be ignored and set to null\. If set to "false" or not set, and a value is present in the EncryptionConfiguration in ResultConfigurationUpdates \(the client\-side setting\), the EncryptionConfiguration in the workgroup's ResultConfiguration will be updated with the new value\. For more information, see [Workgroup Settings Override Client\-Side Settings](https://docs.aws.amazon.com/athena/latest/ug/workgroups-settings-override.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveOutputLocation`  <a name="cfn-athena-workgroup-resultconfigurationupdates-removeoutputlocation"></a>
If set to "true", indicates that the previously\-specified query results location \(also known as a client\-side setting\) for queries in this workgroup should be ignored and set to null\. If set to "false" or not set, and a value is present in the OutputLocation in ResultConfigurationUpdates \(the client\-side setting\), the OutputLocation in the workgroup's ResultConfiguration will be updated with the new value\. For more information, see [Workgroup Settings Override Client\-Side Settings](https://docs.aws.amazon.com/athena/latest/ug/workgroups-settings-override.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)