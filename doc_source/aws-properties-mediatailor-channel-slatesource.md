# AWS::MediaTailor::Channel SlateSource<a name="aws-properties-mediatailor-channel-slatesource"></a>

Slate VOD source configuration\.

## Syntax<a name="aws-properties-mediatailor-channel-slatesource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-channel-slatesource-syntax.json"></a>

```
{
  "[SourceLocationName](#cfn-mediatailor-channel-slatesource-sourcelocationname)" : String,
  "[VodSourceName](#cfn-mediatailor-channel-slatesource-vodsourcename)" : String
}
```

### YAML<a name="aws-properties-mediatailor-channel-slatesource-syntax.yaml"></a>

```
  [SourceLocationName](#cfn-mediatailor-channel-slatesource-sourcelocationname): String
  [VodSourceName](#cfn-mediatailor-channel-slatesource-vodsourcename): String
```

## Properties<a name="aws-properties-mediatailor-channel-slatesource-properties"></a>

`SourceLocationName`  <a name="cfn-mediatailor-channel-slatesource-sourcelocationname"></a>
The name of the source location where the slate VOD source is stored\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VodSourceName`  <a name="cfn-mediatailor-channel-slatesource-vodsourcename"></a>
The slate VOD source name\. The VOD source must already exist in a source location before it can be used for slate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)