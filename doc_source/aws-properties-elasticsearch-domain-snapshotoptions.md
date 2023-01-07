# AWS::Elasticsearch::Domain SnapshotOptions<a name="aws-properties-elasticsearch-domain-snapshotoptions"></a>

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

**DEPRECATED**\. For domains running Elasticsearch 5\.3 and later, OpenSearch Service takes hourly automated snapshots, making this setting irrelevant\. For domains running earlier versions of Elasticsearch, OpenSearch Service takes daily automated snapshots\.

The automated snapshot configuration for the OpenSearch Service domain indices\.

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
The hour in UTC during which the service takes an automated daily snapshot of the indices in the OpenSearch Service domain\. For example, if you specify 0, OpenSearch Service takes an automated snapshot everyday between midnight and 1 am\. You can specify a value between 0 and 23\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)