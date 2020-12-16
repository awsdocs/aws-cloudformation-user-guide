# AWS::MediaPackage::Asset EgressEndpoint<a name="aws-properties-mediapackage-asset-egressendpoint"></a>

The playback endpoint for a packaging configuration on an asset\.

## Syntax<a name="aws-properties-mediapackage-asset-egressendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-asset-egressendpoint-syntax.json"></a>

```
{
  "[PackagingConfigurationId](#cfn-mediapackage-asset-egressendpoint-packagingconfigurationid)" : String,
  "[Url](#cfn-mediapackage-asset-egressendpoint-url)" : String
}
```

### YAML<a name="aws-properties-mediapackage-asset-egressendpoint-syntax.yaml"></a>

```
  [PackagingConfigurationId](#cfn-mediapackage-asset-egressendpoint-packagingconfigurationid): String
  [Url](#cfn-mediapackage-asset-egressendpoint-url): String
```

## Properties<a name="aws-properties-mediapackage-asset-egressendpoint-properties"></a>

`PackagingConfigurationId`  <a name="cfn-mediapackage-asset-egressendpoint-packagingconfigurationid"></a>
The ID of a packaging configuration that's applied to this asset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackage-asset-egressendpoint-url"></a>
The URL that's used to request content from this endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)