# AWS::ECR::ReplicationConfiguration ReplicationRule<a name="aws-properties-ecr-replicationconfiguration-replicationrule"></a>

An array of objects representing the replication destinations for a replication configuration\. A replication configuration may contain only one replication rule but the rule may contain one or more replication destinations\.

## Syntax<a name="aws-properties-ecr-replicationconfiguration-replicationrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecr-replicationconfiguration-replicationrule-syntax.json"></a>

```
{
  "[Destinations](#cfn-ecr-replicationconfiguration-replicationrule-destinations)" : [ ReplicationDestination, ... ]
}
```

### YAML<a name="aws-properties-ecr-replicationconfiguration-replicationrule-syntax.yaml"></a>

```
  [Destinations](#cfn-ecr-replicationconfiguration-replicationrule-destinations): 
    - ReplicationDestination
```

## Properties<a name="aws-properties-ecr-replicationconfiguration-replicationrule-properties"></a>

`Destinations`  <a name="cfn-ecr-replicationconfiguration-replicationrule-destinations"></a>
An array of objects representing the details of a replication destination\.  
*Required*: Yes  
*Type*: List of [ReplicationDestination](aws-properties-ecr-replicationconfiguration-replicationdestination.md)  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)