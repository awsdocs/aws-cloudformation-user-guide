# AWS::MediaPackage::Channel<a name="aws-resource-mediapackage-channel"></a>

Creates a channel to receive content\.

After it's created, a channel provides static input URLs\. These URLs remain the same throughout the lifetime of the channel, regardless of any failures or upgrades that might occur\. Use these URLs to configure the outputs of your upstream encoder\.

## Syntax<a name="aws-resource-mediapackage-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackage-channel-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackage::Channel",
  "Properties" : {
      "[Description](#cfn-mediapackage-channel-description)" : String,
      "[Id](#cfn-mediapackage-channel-id)" : String,
      "[Tags](#cfn-mediapackage-channel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediapackage-channel-syntax.yaml"></a>

```
Type: AWS::MediaPackage::Channel
Properties: 
  [Description](#cfn-mediapackage-channel-description): String
  [Id](#cfn-mediapackage-channel-id): String
  [Tags](#cfn-mediapackage-channel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediapackage-channel-properties"></a>

`Description`  <a name="cfn-mediapackage-channel-description"></a>
Any descriptive information that you want to add to the channel for future identification purposes\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-mediapackage-channel-id"></a>
Unique identifier that you assign to the channel\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-mediapackage-channel-tags"></a>
The tags to assign to the channel\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-mediapackage-channel-return-values"></a>

### Ref<a name="aws-resource-mediapackage-channel-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-mediapackage-channel-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediapackage-channel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The channel's unique system\-generated resource name, based on the AWS record\.

`HlsIngest`  <a name="HlsIngest-fn::getatt"></a>
System\-generated information about the channel\.