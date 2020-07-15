# AWS::Pinpoint::BaiduChannel<a name="aws-resource-pinpoint-baiduchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the Baidu channel to send notifications to the Baidu Cloud Push notification service\. Before you can use Amazon Pinpoint to send notifications to the Baidu Cloud Push service, you have to enable the Baidu channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::BaiduChannel resource defines the status and authentication settings of the Baidu channel for an application\.

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
The unique identifier for the application that the Baidu channel applies to\.  
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

## Return values<a name="aws-resource-pinpoint-baiduchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-baiduchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.