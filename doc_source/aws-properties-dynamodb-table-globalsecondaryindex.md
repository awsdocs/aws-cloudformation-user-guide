# AWS::DynamoDB::Table GlobalSecondaryIndex<a name="aws-properties-dynamodb-table-globalsecondaryindex"></a>

Represents the properties of a global secondary index\.

## Syntax<a name="aws-properties-dynamodb-table-globalsecondaryindex-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-globalsecondaryindex-syntax.json"></a>

```
{
  "[ContributorInsightsSpecification](#cfn-dynamodb-table-globalsecondaryindex-contributorinsightsspecification)" : ContributorInsightsSpecification,
  "[IndexName](#cfn-dynamodb-table-globalsecondaryindex-indexname)" : String,
  "[KeySchema](#cfn-dynamodb-table-globalsecondaryindex-keyschema)" : [ KeySchema, ... ],
  "[Projection](#cfn-dynamodb-table-globalsecondaryindex-projection)" : Projection,
  "[ProvisionedThroughput](#cfn-dynamodb-table-globalsecondaryindex-provisionedthroughput)" : ProvisionedThroughput
}
```

### YAML<a name="aws-properties-dynamodb-table-globalsecondaryindex-syntax.yaml"></a>

```
  [ContributorInsightsSpecification](#cfn-dynamodb-table-globalsecondaryindex-contributorinsightsspecification): 
    ContributorInsightsSpecification
  [IndexName](#cfn-dynamodb-table-globalsecondaryindex-indexname): String
  [KeySchema](#cfn-dynamodb-table-globalsecondaryindex-keyschema): 
    - KeySchema
  [Projection](#cfn-dynamodb-table-globalsecondaryindex-projection): 
    Projection
  [ProvisionedThroughput](#cfn-dynamodb-table-globalsecondaryindex-provisionedthroughput): 
    ProvisionedThroughput
```

## Properties<a name="aws-properties-dynamodb-table-globalsecondaryindex-properties"></a>

`ContributorInsightsSpecification`  <a name="cfn-dynamodb-table-globalsecondaryindex-contributorinsightsspecification"></a>
The settings used to enable or disable CloudWatch Contributor Insights for the specified global secondary index\.  
*Required*: No  
*Type*: [ContributorInsightsSpecification](aws-properties-dynamodb-table-contributorinsightsspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexName`  <a name="cfn-dynamodb-table-globalsecondaryindex-indexname"></a>
The name of the global secondary index\. The name must be unique among all other indexes on this table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: Updates are not supported\.

`KeySchema`  <a name="cfn-dynamodb-table-globalsecondaryindex-keyschema"></a>
The complete key schema for a global secondary index, which consists of one or more pairs of attribute names and key types:  
+  `HASH` \- partition key
+  `RANGE` \- sort key
The partition key of an item is also known as its *hash attribute*\. The term "hash attribute" derives from DynamoDB's usage of an internal hash function to evenly distribute data items across partitions, based on their partition key values\.  
The sort key of an item is also known as its *range attribute*\. The term "range attribute" derives from the way DynamoDB stores items with the same partition key physically close together, in sorted order by the sort key value\.
*Required*: Yes  
*Type*: [List](aws-properties-dynamodb-table-keyschema.md) of [KeySchema](aws-properties-dynamodb-table-keyschema.md)  
*Maximum*: `2`  
*Update requires*: Updates are not supported\.

`Projection`  <a name="cfn-dynamodb-table-globalsecondaryindex-projection"></a>
Represents attributes that are copied \(projected\) from the table into the global secondary index\. These are in addition to the primary key attributes and index key attributes, which are automatically projected\.   
*Required*: Yes  
*Type*: [Projection](aws-properties-dynamodb-table-projection.md)  
*Update requires*: Updates are not supported\.

`ProvisionedThroughput`  <a name="cfn-dynamodb-table-globalsecondaryindex-provisionedthroughput"></a>
Represents the provisioned throughput settings for the specified global secondary index\.  
For current minimum and maximum provisioned throughput values, see [Service, Account, and Table Quotas](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Limits.html) in the *Amazon DynamoDB Developer Guide*\.  
*Required*: No  
*Type*: [ProvisionedThroughput](aws-properties-dynamodb-table-provisionedthroughput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)