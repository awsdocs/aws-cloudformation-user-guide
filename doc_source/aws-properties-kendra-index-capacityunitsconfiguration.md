# AWS::Kendra::Index CapacityUnitsConfiguration<a name="aws-properties-kendra-index-capacityunitsconfiguration"></a>

Specifies capacity units configured for your index\. You can add and remove capacity units to tune an index to your requirements\.

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
The amount of extra query capacity for an index\. Each capacity unit provides 0\.5 queries per second and 40,000 queries per day\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageCapacityUnits`  <a name="cfn-kendra-index-capacityunitsconfiguration-storagecapacityunits"></a>
The amount of extra storage capacity for an index\. Each capacity unit provides 150 Gb of storage space or 500,000 documents, whichever is reached first\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)