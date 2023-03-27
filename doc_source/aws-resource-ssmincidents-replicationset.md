# AWS::SSMIncidents::ReplicationSet<a name="aws-resource-ssmincidents-replicationset"></a>

The `AWS::SSMIncidents::ReplicationSet` resource specifies a set of Regions that Incident Manager data is replicated to and the KMS key used to encrypt the data\.

## Syntax<a name="aws-resource-ssmincidents-replicationset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssmincidents-replicationset-syntax.json"></a>

```
{
  "Type" : "AWS::SSMIncidents::ReplicationSet",
  "Properties" : {
      "[DeletionProtected](#cfn-ssmincidents-replicationset-deletionprotected)" : Boolean,
      "[Regions](#cfn-ssmincidents-replicationset-regions)" : [ ReplicationRegion, ... ],
      "[Tags](#cfn-ssmincidents-replicationset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ssmincidents-replicationset-syntax.yaml"></a>

```
Type: AWS::SSMIncidents::ReplicationSet
Properties: 
  [DeletionProtected](#cfn-ssmincidents-replicationset-deletionprotected): Boolean
  [Regions](#cfn-ssmincidents-replicationset-regions): 
    - ReplicationRegion
  [Tags](#cfn-ssmincidents-replicationset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ssmincidents-replicationset-properties"></a>

`DeletionProtected`  <a name="cfn-ssmincidents-replicationset-deletionprotected"></a>
Determines if the replication set deletion protection is enabled or not\. If deletion protection is enabled, you can't delete the last Region in the replication set\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regions`  <a name="cfn-ssmincidents-replicationset-regions"></a>
Specifies the Regions of the replication set\.  
*Required*: Yes  
*Type*: List of [ReplicationRegion](aws-properties-ssmincidents-replicationset-replicationregion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssmincidents-replicationset-tags"></a>
A list of tags to add to the replication set\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)