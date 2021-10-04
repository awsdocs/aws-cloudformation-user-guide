# AWS::Elasticsearch::Domain ZoneAwarenessConfig<a name="aws-properties-elasticsearch-domain-zoneawarenessconfig"></a>

Specifies zone awareness configuration options\. Only use if `ZoneAwarenessEnabled` is `true`\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-elasticsearch-domain-zoneawarenessconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-zoneawarenessconfig-syntax.json"></a>

```
{
  "[AvailabilityZoneCount](#cfn-elasticsearch-domain-zoneawarenessconfig-availabilityzonecount)" : Integer
}
```

### YAML<a name="aws-properties-elasticsearch-domain-zoneawarenessconfig-syntax.yaml"></a>

```
  [AvailabilityZoneCount](#cfn-elasticsearch-domain-zoneawarenessconfig-availabilityzonecount): Integer
```

## Properties<a name="aws-properties-elasticsearch-domain-zoneawarenessconfig-properties"></a>

`AvailabilityZoneCount`  <a name="cfn-elasticsearch-domain-zoneawarenessconfig-availabilityzonecount"></a>
If you enabled multiple Availability Zones \(AZs\), the number of AZs that you want the domain to use\.  
Valid values are `2` and `3`\. Default is 2\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)