# AWS::MediaPackageV2::OriginEndpoint Scte<a name="aws-properties-mediapackagev2-originendpoint-scte"></a>

The SCTE\-35 configuration associated with the origin endpoint\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-scte-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-scte-syntax.json"></a>

```
{
  "[ScteFilter](#cfn-mediapackagev2-originendpoint-scte-sctefilter)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-scte-syntax.yaml"></a>

```
  [ScteFilter](#cfn-mediapackagev2-originendpoint-scte-sctefilter): 
    - String
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-scte-properties"></a>

`ScteFilter`  <a name="cfn-mediapackagev2-originendpoint-scte-sctefilter"></a>
The filter associated with the SCTE\-35 configuration\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)