# AWS::MediaTailor::SourceLocation<a name="aws-resource-mediatailor-sourcelocation"></a>

A source location is a container for sources\. For more information about source locations, see [Working with source locations](https://docs.aws.amazon.com/mediatailor/latest/ug/channel-assembly-source-locations.html) in the *MediaTailor User Guide*\.

## Syntax<a name="aws-resource-mediatailor-sourcelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediatailor-sourcelocation-syntax.json"></a>

```
{
  "Type" : "AWS::MediaTailor::SourceLocation",
  "Properties" : {
      "[AccessConfiguration](#cfn-mediatailor-sourcelocation-accessconfiguration)" : AccessConfiguration,
      "[DefaultSegmentDeliveryConfiguration](#cfn-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration)" : DefaultSegmentDeliveryConfiguration,
      "[HttpConfiguration](#cfn-mediatailor-sourcelocation-httpconfiguration)" : HttpConfiguration,
      "[SegmentDeliveryConfigurations](#cfn-mediatailor-sourcelocation-segmentdeliveryconfigurations)" : [ SegmentDeliveryConfiguration, ... ],
      "[SourceLocationName](#cfn-mediatailor-sourcelocation-sourcelocationname)" : String,
      "[Tags](#cfn-mediatailor-sourcelocation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediatailor-sourcelocation-syntax.yaml"></a>

```
Type: AWS::MediaTailor::SourceLocation
Properties: 
  [AccessConfiguration](#cfn-mediatailor-sourcelocation-accessconfiguration): 
    AccessConfiguration
  [DefaultSegmentDeliveryConfiguration](#cfn-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration): 
    DefaultSegmentDeliveryConfiguration
  [HttpConfiguration](#cfn-mediatailor-sourcelocation-httpconfiguration): 
    HttpConfiguration
  [SegmentDeliveryConfigurations](#cfn-mediatailor-sourcelocation-segmentdeliveryconfigurations): 
    - SegmentDeliveryConfiguration
  [SourceLocationName](#cfn-mediatailor-sourcelocation-sourcelocationname): String
  [Tags](#cfn-mediatailor-sourcelocation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediatailor-sourcelocation-properties"></a>

`AccessConfiguration`  <a name="cfn-mediatailor-sourcelocation-accessconfiguration"></a>
The access configuration for the source location\.  
*Required*: No  
*Type*: [AccessConfiguration](aws-properties-mediatailor-sourcelocation-accessconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultSegmentDeliveryConfiguration`  <a name="cfn-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration"></a>
The default segment delivery configuration\.  
*Required*: No  
*Type*: [DefaultSegmentDeliveryConfiguration](aws-properties-mediatailor-sourcelocation-defaultsegmentdeliveryconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpConfiguration`  <a name="cfn-mediatailor-sourcelocation-httpconfiguration"></a>
The HTTP configuration for the source location\.  
*Required*: Yes  
*Type*: [HttpConfiguration](aws-properties-mediatailor-sourcelocation-httpconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDeliveryConfigurations`  <a name="cfn-mediatailor-sourcelocation-segmentdeliveryconfigurations"></a>
The segment delivery configurations for the source location\.  
*Required*: No  
*Type*: List of [SegmentDeliveryConfiguration](aws-properties-mediatailor-sourcelocation-segmentdeliveryconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceLocationName`  <a name="cfn-mediatailor-sourcelocation-sourcelocationname"></a>
The name of the source location\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-mediatailor-sourcelocation-tags"></a>
The tags assigned to the source location\. Tags are key\-value pairs that you can associate with Amazon resources to help with organization, access control, and cost tracking\. For more information, see [Tagging AWS Elemental MediaTailor Resources](https://docs.aws.amazon.com/mediatailor/latest/ug/tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediatailor-sourcelocation-return-values"></a>

### Ref<a name="aws-resource-mediatailor-sourcelocation-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-mediatailor-sourcelocation-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediatailor-sourcelocation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.