# AWS::MediaPackage::Channel IngestEndpoint<a name="aws-properties-mediapackage-channel-ingestendpoint"></a>

An endpoint for ingesting source content for a channel\.

## Syntax<a name="aws-properties-mediapackage-channel-ingestendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-channel-ingestendpoint-syntax.json"></a>

```
{
  "[Id](#cfn-mediapackage-channel-ingestendpoint-id)" : String,
  "[Password](#cfn-mediapackage-channel-ingestendpoint-password)" : String,
  "[Url](#cfn-mediapackage-channel-ingestendpoint-url)" : String,
  "[Username](#cfn-mediapackage-channel-ingestendpoint-username)" : String
}
```

### YAML<a name="aws-properties-mediapackage-channel-ingestendpoint-syntax.yaml"></a>

```
  [Id](#cfn-mediapackage-channel-ingestendpoint-id): String
  [Password](#cfn-mediapackage-channel-ingestendpoint-password): String
  [Url](#cfn-mediapackage-channel-ingestendpoint-url): String
  [Username](#cfn-mediapackage-channel-ingestendpoint-username): String
```

## Properties<a name="aws-properties-mediapackage-channel-ingestendpoint-properties"></a>

`Id`  <a name="cfn-mediapackage-channel-ingestendpoint-id"></a>
The endpoint identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-mediapackage-channel-ingestendpoint-password"></a>
The system\-generated password for WebDAV input authentication\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackage-channel-ingestendpoint-url"></a>
The input URL where the source stream should be sent\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-mediapackage-channel-ingestendpoint-username"></a>
The system\-generated username for WebDAV input authentication\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)