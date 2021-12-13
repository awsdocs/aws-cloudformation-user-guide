# AWS::MediaLive::Channel AudioHlsRenditionSelection<a name="aws-properties-medialive-channel-audiohlsrenditionselection"></a>

Selector for HLS audio rendition\.

The parent of this entity is AudioSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-audiohlsrenditionselection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiohlsrenditionselection-syntax.json"></a>

```
{
  "[GroupId](#cfn-medialive-channel-audiohlsrenditionselection-groupid)" : String,
  "[Name](#cfn-medialive-channel-audiohlsrenditionselection-name)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-audiohlsrenditionselection-syntax.yaml"></a>

```
  [GroupId](#cfn-medialive-channel-audiohlsrenditionselection-groupid): String
  [Name](#cfn-medialive-channel-audiohlsrenditionselection-name): String
```

## Properties<a name="aws-properties-medialive-channel-audiohlsrenditionselection-properties"></a>

`GroupId`  <a name="cfn-medialive-channel-audiohlsrenditionselection-groupid"></a>
Specifies the GROUP\-ID in the \#EXT\-X\-MEDIA tag of the target HLS audio rendition\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-channel-audiohlsrenditionselection-name"></a>
Specifies the NAME in the \#EXT\-X\-MEDIA tag of the target HLS audio rendition\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)