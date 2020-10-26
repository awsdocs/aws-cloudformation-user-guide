# AWS::ElastiCache::GlobalReplicationGroup<a name="aws-resource-elasticache-globalreplicationgroup"></a>

Consists of a primary cluster that accepts writes and an associated secondary cluster that resides in a different AWS region\. The secondary cluster accepts only reads\. The primary cluster automatically replicates updates to the secondary cluster\.
+ The **GlobalReplicationGroupIdSuffix** represents the name of the Global Datastore, which is what you use to associate a secondary cluster\.

## Syntax<a name="aws-resource-elasticache-globalreplicationgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-globalreplicationgroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::GlobalReplicationGroup",
  "Properties" : {
      "[AutomaticFailoverEnabled](#cfn-elasticache-globalreplicationgroup-automaticfailoverenabled)" : Boolean,
      "[CacheNodeType](#cfn-elasticache-globalreplicationgroup-cachenodetype)" : String,
      "[EngineVersion](#cfn-elasticache-globalreplicationgroup-engineversion)" : String,
      "[GlobalNodeGroupCount](#cfn-elasticache-globalreplicationgroup-globalnodegroupcount)" : Integer,
      "[GlobalReplicationGroupDescription](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupdescription)" : String,
      "[GlobalReplicationGroupIdSuffix](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupidsuffix)" : String,
      "[Members](#cfn-elasticache-globalreplicationgroup-members)" : [ GlobalReplicationGroupMember, ... ],
      "[RegionalConfigurations](#cfn-elasticache-globalreplicationgroup-regionalconfigurations)" : [ RegionalConfiguration, ... ],
      "[Status](#cfn-elasticache-globalreplicationgroup-status)" : String
    }
}
```

### YAML<a name="aws-resource-elasticache-globalreplicationgroup-syntax.yaml"></a>

```
Type: AWS::ElastiCache::GlobalReplicationGroup
Properties: 
  [AutomaticFailoverEnabled](#cfn-elasticache-globalreplicationgroup-automaticfailoverenabled): Boolean
  [CacheNodeType](#cfn-elasticache-globalreplicationgroup-cachenodetype): String
  [EngineVersion](#cfn-elasticache-globalreplicationgroup-engineversion): String
  [GlobalNodeGroupCount](#cfn-elasticache-globalreplicationgroup-globalnodegroupcount): Integer
  [GlobalReplicationGroupDescription](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupdescription): String
  [GlobalReplicationGroupIdSuffix](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupidsuffix): String
  [Members](#cfn-elasticache-globalreplicationgroup-members): 
    - GlobalReplicationGroupMember
  [RegionalConfigurations](#cfn-elasticache-globalreplicationgroup-regionalconfigurations): 
    - RegionalConfiguration
  [Status](#cfn-elasticache-globalreplicationgroup-status): String
```

## Properties<a name="aws-resource-elasticache-globalreplicationgroup-properties"></a>

`AutomaticFailoverEnabled`  <a name="cfn-elasticache-globalreplicationgroup-automaticfailoverenabled"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheNodeType`  <a name="cfn-elasticache-globalreplicationgroup-cachenodetype"></a>
The cache node type of the Global Datastore  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineVersion`  <a name="cfn-elasticache-globalreplicationgroup-engineversion"></a>
The Elasticache Redis engine version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalNodeGroupCount`  <a name="cfn-elasticache-globalreplicationgroup-globalnodegroupcount"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalReplicationGroupDescription`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupdescription"></a>
The optional description of the Global Datastore  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalReplicationGroupIdSuffix`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupidsuffix"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Members`  <a name="cfn-elasticache-globalreplicationgroup-members"></a>
The replication groups that comprise the Global Datastore\.  
*Required*: Yes  
*Type*: List of [GlobalReplicationGroupMember](aws-properties-elasticache-globalreplicationgroup-globalreplicationgroupmember.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegionalConfigurations`  <a name="cfn-elasticache-globalreplicationgroup-regionalconfigurations"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [RegionalConfiguration](aws-properties-elasticache-globalreplicationgroup-regionalconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-elasticache-globalreplicationgroup-status"></a>
The status of the Global Datastore  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-elasticache-globalreplicationgroup-return-values"></a>

### Ref<a name="aws-resource-elasticache-globalreplicationgroup-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-elasticache-globalreplicationgroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-elasticache-globalreplicationgroup-return-values-fn--getatt-fn--getatt"></a>

`GlobalReplicationGroupId`  <a name="GlobalReplicationGroupId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.