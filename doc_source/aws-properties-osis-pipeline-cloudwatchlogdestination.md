# AWS::OSIS::Pipeline CloudWatchLogDestination<a name="aws-properties-osis-pipeline-cloudwatchlogdestination"></a>

The destination for OpenSearch Ingestion logs sent to Amazon CloudWatch\.

## Syntax<a name="aws-properties-osis-pipeline-cloudwatchlogdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-osis-pipeline-cloudwatchlogdestination-syntax.json"></a>

```
{
  "[LogGroup](#cfn-osis-pipeline-cloudwatchlogdestination-loggroup)" : String
}
```

### YAML<a name="aws-properties-osis-pipeline-cloudwatchlogdestination-syntax.yaml"></a>

```
  [LogGroup](#cfn-osis-pipeline-cloudwatchlogdestination-loggroup): String
```

## Properties<a name="aws-properties-osis-pipeline-cloudwatchlogdestination-properties"></a>

`LogGroup`  <a name="cfn-osis-pipeline-cloudwatchlogdestination-loggroup"></a>
The name of the CloudWatch Logs group to send pipeline logs to\. You can specify an existing log group or create a new one\. For example, `/aws/OpenSearchService/IngestionService/my-pipeline`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `\/aws\/vendedlogs\/[\.\-_/#A-Za-z0-9]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)