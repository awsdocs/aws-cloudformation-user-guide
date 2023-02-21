# AWS::NimbleStudio::StreamingImage<a name="aws-resource-nimblestudio-streamingimage"></a>

The `AWS::NimbleStudio::StreamingImage` resource creates a streaming image in a studio\. A streaming image defines the operating system and software to be used in an Amazon Nimble Studio streaming session\.

## Syntax<a name="aws-resource-nimblestudio-streamingimage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-nimblestudio-streamingimage-syntax.json"></a>

```
{
  "Type" : "AWS::NimbleStudio::StreamingImage",
  "Properties" : {
      "[Description](#cfn-nimblestudio-streamingimage-description)" : String,
      "[Ec2ImageId](#cfn-nimblestudio-streamingimage-ec2imageid)" : String,
      "[Name](#cfn-nimblestudio-streamingimage-name)" : String,
      "[StudioId](#cfn-nimblestudio-streamingimage-studioid)" : String,
      "[Tags](#cfn-nimblestudio-streamingimage-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-nimblestudio-streamingimage-syntax.yaml"></a>

```
Type: AWS::NimbleStudio::StreamingImage
Properties: 
  [Description](#cfn-nimblestudio-streamingimage-description): String
  [Ec2ImageId](#cfn-nimblestudio-streamingimage-ec2imageid): String
  [Name](#cfn-nimblestudio-streamingimage-name): String
  [StudioId](#cfn-nimblestudio-streamingimage-studioid): String
  [Tags](#cfn-nimblestudio-streamingimage-tags): 
    Key : Value
```

## Properties<a name="aws-resource-nimblestudio-streamingimage-properties"></a>

`Description`  <a name="cfn-nimblestudio-streamingimage-description"></a>
A human\-readable description of the streaming image\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2ImageId`  <a name="cfn-nimblestudio-streamingimage-ec2imageid"></a>
The ID of an EC2 machine image with which to create the streaming image\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-nimblestudio-streamingimage-name"></a>
A friendly name for a streaming image resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StudioId`  <a name="cfn-nimblestudio-streamingimage-studioid"></a>
The unique identifier for a studio resource\. In Nimble Studio, all other resources are contained in a studio resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-nimblestudio-streamingimage-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-nimblestudio-streamingimage-return-values"></a>

### Fn::GetAtt<a name="aws-resource-nimblestudio-streamingimage-return-values-fn--getatt"></a>

#### <a name="aws-resource-nimblestudio-streamingimage-return-values-fn--getatt-fn--getatt"></a>

`EncryptionConfiguration`  <a name="EncryptionConfiguration-fn::getatt"></a>
Property description not available\.

`EncryptionConfiguration.KeyArn`  <a name="EncryptionConfiguration.KeyArn-fn::getatt"></a>
Property description not available\.

`EncryptionConfiguration.KeyType`  <a name="EncryptionConfiguration.KeyType-fn::getatt"></a>
Property description not available\.

`EulaIds`  <a name="EulaIds-fn::getatt"></a>
The list of IDs of EULAs that must be accepted before a streaming session can be started using this streaming image\.

`Owner`  <a name="Owner-fn::getatt"></a>
The owner of the streaming image, either the studioId that contains the streaming image or 'amazon' for images that are provided by Amazon Nimble Studio\.

`Platform`  <a name="Platform-fn::getatt"></a>
The platform of the streaming image, either WINDOWS or LINUX\.

`StreamingImageId`  <a name="StreamingImageId-fn::getatt"></a>
The unique identifier for the streaming image resource\.