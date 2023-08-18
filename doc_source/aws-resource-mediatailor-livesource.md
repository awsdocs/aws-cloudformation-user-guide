# AWS::MediaTailor::LiveSource<a name="aws-resource-mediatailor-livesource"></a>

Live source configuration parameters\.

## Syntax<a name="aws-resource-mediatailor-livesource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediatailor-livesource-syntax.json"></a>

```
{
  "Type" : "AWS::MediaTailor::LiveSource",
  "Properties" : {
      "[HttpPackageConfigurations](#cfn-mediatailor-livesource-httppackageconfigurations)" : [ HttpPackageConfiguration, ... ],
      "[LiveSourceName](#cfn-mediatailor-livesource-livesourcename)" : String,
      "[SourceLocationName](#cfn-mediatailor-livesource-sourcelocationname)" : String,
      "[Tags](#cfn-mediatailor-livesource-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediatailor-livesource-syntax.yaml"></a>

```
Type: AWS::MediaTailor::LiveSource
Properties: 
  [HttpPackageConfigurations](#cfn-mediatailor-livesource-httppackageconfigurations): 
    - HttpPackageConfiguration
  [LiveSourceName](#cfn-mediatailor-livesource-livesourcename): String
  [SourceLocationName](#cfn-mediatailor-livesource-sourcelocationname): String
  [Tags](#cfn-mediatailor-livesource-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediatailor-livesource-properties"></a>

`HttpPackageConfigurations`  <a name="cfn-mediatailor-livesource-httppackageconfigurations"></a>
The HTTP package configurations for the live source\.  
*Required*: Yes  
*Type*: List of [HttpPackageConfiguration](aws-properties-mediatailor-livesource-httppackageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LiveSourceName`  <a name="cfn-mediatailor-livesource-livesourcename"></a>
The name that's used to refer to a live source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceLocationName`  <a name="cfn-mediatailor-livesource-sourcelocationname"></a>
The name of the source location\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-mediatailor-livesource-tags"></a>
The tags assigned to the live source\. Tags are key\-value pairs that you can associate with Amazon resources to help with organization, access control, and cost tracking\. For more information, see [Tagging AWS Elemental MediaTailor Resources](https://docs.aws.amazon.com/mediatailor/latest/ug/tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediatailor-livesource-return-values"></a>

### Ref<a name="aws-resource-mediatailor-livesource-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-mediatailor-livesource-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediatailor-livesource-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.