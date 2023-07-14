# AWS::Cassandra::Keyspace ReplicationSpecification<a name="aws-properties-cassandra-keyspace-replicationspecification"></a>

You can use `ReplicationSpecification` to configure the `ReplicationStrategy` of a keyspace in Amazon Keyspaces\. 

The `ReplicationSpecification` property is `CreateOnly` and cannot be changed after the keyspace has been created\. This property applies automatically to all tables in the keyspace\. 

For more information, see [Multi\-Region Replication](https://docs.aws.amazon.com/keyspaces/latest/devguide/multiRegion-replication.html) in the *Amazon Keyspaces Developer Guide*\.

## Syntax<a name="aws-properties-cassandra-keyspace-replicationspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cassandra-keyspace-replicationspecification-syntax.json"></a>

```
{
  "[RegionList](#cfn-cassandra-keyspace-replicationspecification-regionlist)" : [ String, ... ],
  "[ReplicationStrategy](#cfn-cassandra-keyspace-replicationspecification-replicationstrategy)" : String
}
```

### YAML<a name="aws-properties-cassandra-keyspace-replicationspecification-syntax.yaml"></a>

```
  [RegionList](#cfn-cassandra-keyspace-replicationspecification-regionlist): 
    - String
  [ReplicationStrategy](#cfn-cassandra-keyspace-replicationspecification-replicationstrategy): String
```

## Properties<a name="aws-properties-cassandra-keyspace-replicationspecification-properties"></a>

`RegionList`  <a name="cfn-cassandra-keyspace-replicationspecification-regionlist"></a>
Specifies the AWS Regions that the keyspace is replicated in\. You must specify at least two and up to six Regions, including the Region that the keyspace is being created in\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicationStrategy`  <a name="cfn-cassandra-keyspace-replicationspecification-replicationstrategy"></a>
The options are:  
+ `SINGLE_REGION` \(optional\) 
+ `MULTI_REGION` 
If no value is specified, the default is `SINGLE_REGION`\. If `MULTI_REGION` is specified, `RegionList` is required\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)