# Amazon Elasticsearch Service Domain SnapshotOptions<a name="aws-properties-elasticsearch-domain-snapshotoptions"></a>

`SnapshotOptions` is a property of the [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md) resource that configures the automated snapshot of Amazon Elasticsearch Service \(Amazon ES\) domain indices\.

## Syntax<a name="w3ab2c21c14e1052b5"></a>

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

## Properties<a name="w3ab2c21c14e1052b7"></a>

`AutomatedSnapshotStartHour`  <a name="cfn-elasticsearch-domain-snapshotoptions-automatedsnapshotstarthour"></a>
The hour in UTC during which the service takes an automated daily snapshot of the indices in the Amazon ES domain\. For example, if you specify `0`, Amazon ES takes an automated snapshot everyday between midnight and 1 am\. You can specify a value between `0` and `23`\.  
*Required*: No  
*Type*: Integer