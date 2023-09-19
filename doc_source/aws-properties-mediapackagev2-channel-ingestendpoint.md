# AWS::MediaPackageV2::Channel IngestEndpoint<a name="aws-properties-mediapackagev2-channel-ingestendpoint"></a>

The input URL where the source stream should be sent\.

## Syntax<a name="aws-properties-mediapackagev2-channel-ingestendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-channel-ingestendpoint-syntax.json"></a>

```
{
  "[Id](#cfn-mediapackagev2-channel-ingestendpoint-id)" : String,
  "[Url](#cfn-mediapackagev2-channel-ingestendpoint-url)" : String
}
```

### YAML<a name="aws-properties-mediapackagev2-channel-ingestendpoint-syntax.yaml"></a>

```
  [Id](#cfn-mediapackagev2-channel-ingestendpoint-id): String
  [Url](#cfn-mediapackagev2-channel-ingestendpoint-url): String
```

## Properties<a name="aws-properties-mediapackagev2-channel-ingestendpoint-properties"></a>

`Id`  <a name="cfn-mediapackagev2-channel-ingestendpoint-id"></a>
The identifier associated with the ingest endpoint of the channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackagev2-channel-ingestendpoint-url"></a>
The URL associated with the ingest endpoint of the channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)