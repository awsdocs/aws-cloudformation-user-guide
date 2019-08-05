# AWS::Pinpoint::BaiduChannel<a name="aws-resource-pinpoint-baiduchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the Baidu channel to send notifications to the Baidu notification service\. Before you use Amazon Pinpoint to send notifications to Baidu, you have to enable the Baidu channel for an Amazon Pinpoint app\.

The Baidu Channel resource represents the status and authentication settings of the Baidu channel for a specific application\. You can use this resource to retrieve information about, update, or disable \(delete\) the Baidu channel for an app\.

## Syntax<a name="aws-resource-pinpoint-baiduchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-baiduchannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::BaiduChannel",
  "Properties" : {
      "[ApiKey](#cfn-pinpoint-baiduchannel-apikey)" : String,
      "[ApplicationId](#cfn-pinpoint-baiduchannel-applicationid)" : String,
      "[Enabled](#cfn-pinpoint-baiduchannel-enabled)" : Boolean,
      "[SecretKey](#cfn-pinpoint-baiduchannel-secretkey)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-baiduchannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::BaiduChannel
Properties:
  [ApiKey](#cfn-pinpoint-baiduchannel-apikey): String
  [ApplicationId](#cfn-pinpoint-baiduchannel-applicationid): String
  [Enabled](#cfn-pinpoint-baiduchannel-enabled): Boolean
  [SecretKey](#cfn-pinpoint-baiduchannel-secretkey): String
```

## Properties<a name="aws-resource-pinpoint-baiduchannel-properties"></a>

`ApiKey`  <a name="cfn-pinpoint-baiduchannel-apikey"></a>
The API key that you received from the Baidu Cloud Push service to communicate with the service\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationId`  <a name="cfn-pinpoint-baiduchannel-applicationid"></a>
The unique ID of the Amazon Pinpoint app that you're configuring the Baidu channel for\.
*Required*: Yes
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-pinpoint-baiduchannel-enabled"></a>
Specifies whether to enable the Baidu channel for the application\.
*Required*: No
*Type*: Boolean
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretKey`  <a name="cfn-pinpoint-baiduchannel-secretkey"></a>
The secret key that you received from the Baidu Cloud Push service to communicate with the service\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-pinpoint-baiduchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-baiduchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Amazon Pinpoint app that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.
