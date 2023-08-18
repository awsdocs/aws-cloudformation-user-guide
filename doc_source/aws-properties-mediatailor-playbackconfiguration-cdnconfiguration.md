# AWS::MediaTailor::PlaybackConfiguration CdnConfiguration<a name="aws-properties-mediatailor-playbackconfiguration-cdnconfiguration"></a>

<a name="aws-properties-mediatailor-playbackconfiguration-cdnconfiguration-description"></a>The `CdnConfiguration` property type specifies Property description not available\. for an [AWS::MediaTailor::PlaybackConfiguration](aws-resource-mediatailor-playbackconfiguration.md)\.

## Syntax<a name="aws-properties-mediatailor-playbackconfiguration-cdnconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-playbackconfiguration-cdnconfiguration-syntax.json"></a>

```
{
  "[AdSegmentUrlPrefix](#cfn-mediatailor-playbackconfiguration-cdnconfiguration-adsegmenturlprefix)" : String,
  "[ContentSegmentUrlPrefix](#cfn-mediatailor-playbackconfiguration-cdnconfiguration-contentsegmenturlprefix)" : String
}
```

### YAML<a name="aws-properties-mediatailor-playbackconfiguration-cdnconfiguration-syntax.yaml"></a>

```
  [AdSegmentUrlPrefix](#cfn-mediatailor-playbackconfiguration-cdnconfiguration-adsegmenturlprefix): String
  [ContentSegmentUrlPrefix](#cfn-mediatailor-playbackconfiguration-cdnconfiguration-contentsegmenturlprefix): String
```

## Properties<a name="aws-properties-mediatailor-playbackconfiguration-cdnconfiguration-properties"></a>

`AdSegmentUrlPrefix`  <a name="cfn-mediatailor-playbackconfiguration-cdnconfiguration-adsegmenturlprefix"></a>
A non\-default content delivery network \(CDN\) to serve ad segments\. By default, AWS Elemental MediaTailor uses Amazon CloudFront with default cache settings as its CDN for ad segments\. To set up an alternate CDN, create a rule in your CDN for the origin ads\.mediatailor\.*<region>*\.amazonaws\.com\. Then specify the rule's name in this `AdSegmentUrlPrefix`\. When AWS Elemental MediaTailor serves a manifest, it reports your CDN as the source for ad segments\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentSegmentUrlPrefix`  <a name="cfn-mediatailor-playbackconfiguration-cdnconfiguration-contentsegmenturlprefix"></a>
A content delivery network \(CDN\) to cache content segments, so that content requests don’t always have to go to the origin server\. First, create a rule in your CDN for the content segment origin server\. Then specify the rule's name in this `ContentSegmentUrlPrefix`\. When AWS Elemental MediaTailor serves a manifest, it reports your CDN as the source for content segments\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)