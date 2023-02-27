# AWS::OpenSearchService::Domain SnapshotOptions<a name="aws-properties-opensearchservice-domain-snapshotoptions"></a>

**DEPRECATED**\. This setting is only relevant to domains running legacy Elasticsearch OSS versions earlier than 5\.3\. It does not apply to OpenSearch domains\.

The automated snapshot configuration for the OpenSearch Service domain indexes\.

## Syntax<a name="aws-properties-opensearchservice-domain-snapshotoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-snapshotoptions-syntax.json"></a>

```
{
  "[AutomatedSnapshotStartHour](#cfn-opensearchservice-domain-snapshotoptions-automatedsnapshotstarthour)" : Integer
}
```

### YAML<a name="aws-properties-opensearchservice-domain-snapshotoptions-syntax.yaml"></a>

```
  [AutomatedSnapshotStartHour](#cfn-opensearchservice-domain-snapshotoptions-automatedsnapshotstarthour): Integer
```

## Properties<a name="aws-properties-opensearchservice-domain-snapshotoptions-properties"></a>

`AutomatedSnapshotStartHour`  <a name="cfn-opensearchservice-domain-snapshotoptions-automatedsnapshotstarthour"></a>
The hour in UTC during which the service takes an automated daily snapshot of the indexes in the OpenSearch Service domain\. For example, if you specify 0, OpenSearch Service takes an automated snapshot everyday between midnight and 1 am\. You can specify a value between 0 and 23\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)