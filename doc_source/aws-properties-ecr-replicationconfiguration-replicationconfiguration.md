# AWS::ECR::ReplicationConfiguration ReplicationConfiguration<a name="aws-properties-ecr-replicationconfiguration-replicationconfiguration"></a>

The replication configuration for a registry\.

## Syntax<a name="aws-properties-ecr-replicationconfiguration-replicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecr-replicationconfiguration-replicationconfiguration-syntax.json"></a>

```
{
  "[Rules](#cfn-ecr-replicationconfiguration-replicationconfiguration-rules)" : [ ReplicationRule, ... ]
}
```

### YAML<a name="aws-properties-ecr-replicationconfiguration-replicationconfiguration-syntax.yaml"></a>

```
  [Rules](#cfn-ecr-replicationconfiguration-replicationconfiguration-rules): 
    - ReplicationRule
```

## Properties<a name="aws-properties-ecr-replicationconfiguration-replicationconfiguration-properties"></a>

`Rules`  <a name="cfn-ecr-replicationconfiguration-replicationconfiguration-rules"></a>
An array of objects representing the replication rules for a replication configuration\. A replication configuration may contain only one replication rule but the rule may contain one or more replication destinations\.  
*Required*: Yes  
*Type*: List of [ReplicationRule](aws-properties-ecr-replicationconfiguration-replicationrule.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)