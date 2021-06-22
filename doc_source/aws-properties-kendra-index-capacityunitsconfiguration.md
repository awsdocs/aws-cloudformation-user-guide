# AWS::Kendra::Index CapacityUnitsConfiguration<a name="aws-properties-kendra-index-capacityunitsconfiguration"></a>

Specifies capacity units configured for your enterprise edition index\. You can add and remove capacity units to tune an index to your requirements\.

## Syntax<a name="aws-properties-kendra-index-capacityunitsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-capacityunitsconfiguration-syntax.json"></a>

```
{
  "[QueryCapacityUnits](#cfn-kendra-index-capacityunitsconfiguration-querycapacityunits)" : Integer,
  "[StorageCapacityUnits](#cfn-kendra-index-capacityunitsconfiguration-storagecapacityunits)" : Integer
}
```

### YAML<a name="aws-properties-kendra-index-capacityunitsconfiguration-syntax.yaml"></a>

```
  [QueryCapacityUnits](#cfn-kendra-index-capacityunitsconfiguration-querycapacityunits): Integer
  [StorageCapacityUnits](#cfn-kendra-index-capacityunitsconfiguration-storagecapacityunits): Integer
```

## Properties<a name="aws-properties-kendra-index-capacityunitsconfiguration-properties"></a>

`QueryCapacityUnits`  <a name="cfn-kendra-index-capacityunitsconfiguration-querycapacityunits"></a>
The amount of extra query capacity for an index and [GetQuerySuggestions](https://docs.aws.amazon.com/kendra/latest/dg/API_GetQuerySuggestions.html) capacity\.  
A single extra capacity unit for an index provides 0\.5 queries per second or approximately 40,000 queries per day\.  
 `GetQuerySuggestions` capacity is 5 times the provisioned query capacity for an index\. For example, the base capacity for an index is 0\.5 queries per second, so GetQuerySuggestions capacity is 2\.5 calls per second\. If adding another 0\.5 queries per second to total 1 queries per second for an index, the `GetQuerySuggestions` capacity is 5 calls per second\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageCapacityUnits`  <a name="cfn-kendra-index-capacityunitsconfiguration-storagecapacityunits"></a>
The amount of extra storage capacity for an index\. A single capacity unit for an index provides 150 GB of storage space or 500,000 documents, whichever is reached first\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)