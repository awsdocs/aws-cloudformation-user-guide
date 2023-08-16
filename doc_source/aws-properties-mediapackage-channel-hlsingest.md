# AWS::MediaPackage::Channel HlsIngest<a name="aws-properties-mediapackage-channel-hlsingest"></a>

HLS ingest configuration\.

## Syntax<a name="aws-properties-mediapackage-channel-hlsingest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-channel-hlsingest-syntax.json"></a>

```
{
  "[ingestEndpoints](#cfn-mediapackage-channel-hlsingest-ingestendpoints)" : [ IngestEndpoint, ... ]
}
```

### YAML<a name="aws-properties-mediapackage-channel-hlsingest-syntax.yaml"></a>

```
  [ingestEndpoints](#cfn-mediapackage-channel-hlsingest-ingestendpoints): 
    - IngestEndpoint
```

## Properties<a name="aws-properties-mediapackage-channel-hlsingest-properties"></a>

`ingestEndpoints`  <a name="cfn-mediapackage-channel-hlsingest-ingestendpoints"></a>
The input URL where the source stream should be sent\.  
*Required*: No  
*Type*: List of [IngestEndpoint](aws-properties-mediapackage-channel-ingestendpoint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)