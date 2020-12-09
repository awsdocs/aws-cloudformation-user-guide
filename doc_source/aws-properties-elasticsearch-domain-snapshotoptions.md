# AWS::Elasticsearch::Domain SnapshotOptions<a name="aws-properties-elasticsearch-domain-snapshotoptions"></a>

The automated snapshot configuration for the Amazon ES domain indices\.

## Syntax<a name="aws-properties-elasticsearch-domain-snapshotoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-snapshotoptions-syntax.json"></a>

```
{
  "[AutomatedSnapshotStartHour](#cfn-elasticsearch-domain-snapshotoptions-automatedsnapshotstarthour)" : Integer
}
```

### YAML<a name="aws-properties-elasticsearch-domain-snapshotoptions-syntax.yaml"></a>

```
  [AutomatedSnapshotStartHour](#cfn-elasticsearch-domain-snapshotoptions-automatedsnapshotstarthour): Integer
```

## Properties<a name="aws-properties-elasticsearch-domain-snapshotoptions-properties"></a>

`AutomatedSnapshotStartHour`  <a name="cfn-elasticsearch-domain-snapshotoptions-automatedsnapshotstarthour"></a>
The hour in UTC during which the service takes an automated daily snapshot of the indices in the Amazon ES domain\. For example, if you specify 0, Amazon ES takes an automated snapshot everyday between midnight and 1 am\. You can specify a value between 0 and 23\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)