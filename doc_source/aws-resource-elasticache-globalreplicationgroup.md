# AWS::ElastiCache::GlobalReplicationGroup<a name="aws-resource-elasticache-globalreplicationgroup"></a>

Consists of a primary cluster that accepts writes and an associated secondary cluster that resides in a different Amazon region\. The secondary cluster accepts only reads\. The primary cluster automatically replicates updates to the secondary cluster\.
+ The **GlobalReplicationGroupIdSuffix** represents the name of the Global datastore, which is what you use to associate a secondary cluster\.

## Syntax<a name="aws-resource-elasticache-globalreplicationgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-globalreplicationgroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::GlobalReplicationGroup",
  "Properties" : {
      "[AutomaticFailoverEnabled](#cfn-elasticache-globalreplicationgroup-automaticfailoverenabled)" : Boolean,
      "[CacheNodeType](#cfn-elasticache-globalreplicationgroup-cachenodetype)" : String,
      "[CacheParameterGroupName](#cfn-elasticache-globalreplicationgroup-cacheparametergroupname)" : String,
      "[EngineVersion](#cfn-elasticache-globalreplicationgroup-engineversion)" : String,
      "[GlobalNodeGroupCount](#cfn-elasticache-globalreplicationgroup-globalnodegroupcount)" : Integer,
      "[GlobalReplicationGroupDescription](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupdescription)" : String,
      "[GlobalReplicationGroupIdSuffix](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupidsuffix)" : String,
      "[Members](#cfn-elasticache-globalreplicationgroup-members)" : [ GlobalReplicationGroupMember, ... ],
      "[RegionalConfigurations](#cfn-elasticache-globalreplicationgroup-regionalconfigurations)" : [ RegionalConfiguration, ... ]
    }
}
```

### YAML<a name="aws-resource-elasticache-globalreplicationgroup-syntax.yaml"></a>

```
Type: AWS::ElastiCache::GlobalReplicationGroup
Properties: 
  [AutomaticFailoverEnabled](#cfn-elasticache-globalreplicationgroup-automaticfailoverenabled): Boolean
  [CacheNodeType](#cfn-elasticache-globalreplicationgroup-cachenodetype): String
  [CacheParameterGroupName](#cfn-elasticache-globalreplicationgroup-cacheparametergroupname): String
  [EngineVersion](#cfn-elasticache-globalreplicationgroup-engineversion): String
  [GlobalNodeGroupCount](#cfn-elasticache-globalreplicationgroup-globalnodegroupcount): Integer
  [GlobalReplicationGroupDescription](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupdescription): String
  [GlobalReplicationGroupIdSuffix](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupidsuffix): String
  [Members](#cfn-elasticache-globalreplicationgroup-members): 
    - GlobalReplicationGroupMember
  [RegionalConfigurations](#cfn-elasticache-globalreplicationgroup-regionalconfigurations): 
    - RegionalConfiguration
```

## Properties<a name="aws-resource-elasticache-globalreplicationgroup-properties"></a>

`AutomaticFailoverEnabled`  <a name="cfn-elasticache-globalreplicationgroup-automaticfailoverenabled"></a>
Specifies whether a read\-only replica is automatically promoted to read/write primary if the existing primary fails\.  
 `AutomaticFailoverEnabled` must be enabled for Redis \(cluster mode enabled\) replication groups\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheNodeType`  <a name="cfn-elasticache-globalreplicationgroup-cachenodetype"></a>
The cache node type of the Global datastore  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheParameterGroupName`  <a name="cfn-elasticache-globalreplicationgroup-cacheparametergroupname"></a>
The name of the cache parameter group to use with the Global datastore\. It must be compatible with the major engine version used by the Global datastore\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineVersion`  <a name="cfn-elasticache-globalreplicationgroup-engineversion"></a>
The Elasticache Redis engine version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalNodeGroupCount`  <a name="cfn-elasticache-globalreplicationgroup-globalnodegroupcount"></a>
The number of node groups that comprise the Global Datastore\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalReplicationGroupDescription`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupdescription"></a>
The optional description of the Global datastore  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalReplicationGroupIdSuffix`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupidsuffix"></a>
The suffix name of a Global Datastore\. The suffix guarantees uniqueness of the Global Datastore name across multiple regions\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Members`  <a name="cfn-elasticache-globalreplicationgroup-members"></a>
The replication groups that comprise the Global datastore\.  
*Required*: Yes  
*Type*: List of [GlobalReplicationGroupMember](aws-properties-elasticache-globalreplicationgroup-globalreplicationgroupmember.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegionalConfigurations`  <a name="cfn-elasticache-globalreplicationgroup-regionalconfigurations"></a>
The Regions that comprise the Global Datastore\.  
*Required*: No  
*Type*: List of [RegionalConfiguration](aws-properties-elasticache-globalreplicationgroup-regionalconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-elasticache-globalreplicationgroup-return-values"></a>

### Ref<a name="aws-resource-elasticache-globalreplicationgroup-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-elasticache-globalreplicationgroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-elasticache-globalreplicationgroup-return-values-fn--getatt-fn--getatt"></a>

`GlobalReplicationGroupId`  <a name="GlobalReplicationGroupId-fn::getatt"></a>
The ID used to associate a secondary cluster to the Global Replication Group\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the Global Datastore\. Can be `Creating`, `Modifying`, `Available`, `Deleting` or `Primary-Only`\. Primary\-only status indicates the global datastore contains only a primary cluster\. Either all secondary clusters are deleted or not successfully created\.