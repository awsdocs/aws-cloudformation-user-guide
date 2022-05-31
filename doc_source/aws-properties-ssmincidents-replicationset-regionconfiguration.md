# AWS::SSMIncidents::ReplicationSet RegionConfiguration<a name="aws-properties-ssmincidents-replicationset-regionconfiguration"></a>

The `RegionConfiguration` property specifies the Region and KMS key to add to the replication set\.

## Syntax<a name="aws-properties-ssmincidents-replicationset-regionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-replicationset-regionconfiguration-syntax.json"></a>

```
{
  "[SseKmsKeyId](#cfn-ssmincidents-replicationset-regionconfiguration-ssekmskeyid)" : String
}
```

### YAML<a name="aws-properties-ssmincidents-replicationset-regionconfiguration-syntax.yaml"></a>

```
  [SseKmsKeyId](#cfn-ssmincidents-replicationset-regionconfiguration-ssekmskeyid): String
```

## Properties<a name="aws-properties-ssmincidents-replicationset-regionconfiguration-properties"></a>

`SseKmsKeyId`  <a name="cfn-ssmincidents-replicationset-regionconfiguration-ssekmskeyid"></a>
The KMS key ID to use to encrypt your replication set\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)