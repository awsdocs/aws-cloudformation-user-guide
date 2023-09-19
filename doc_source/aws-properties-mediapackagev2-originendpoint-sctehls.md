# AWS::MediaPackageV2::OriginEndpoint ScteHls<a name="aws-properties-mediapackagev2-originendpoint-sctehls"></a>

The SCTE\-35 HLS configuration associated with the origin endpoint\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-sctehls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-sctehls-syntax.json"></a>

```
{
  "[AdMarkerHls](#cfn-mediapackagev2-originendpoint-sctehls-admarkerhls)" : String
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-sctehls-syntax.yaml"></a>

```
  [AdMarkerHls](#cfn-mediapackagev2-originendpoint-sctehls-admarkerhls): String
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-sctehls-properties"></a>

`AdMarkerHls`  <a name="cfn-mediapackagev2-originendpoint-sctehls-admarkerhls"></a>
The SCTE\-35 HLS ad\-marker configuration\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DATERANGE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)