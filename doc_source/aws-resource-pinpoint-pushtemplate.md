# AWS::Pinpoint::PushTemplate<a name="aws-resource-pinpoint-pushtemplate"></a>

The AWS::Pinpoint::PushTemplate resource is a message template that you can use in messages that are sent through a push notification channel\. A *message template* is a set of content and settings that you can define, save, and reuse in messages for one or more Amazon Pinpoint applications\.

## Syntax<a name="aws-resource-pinpoint-pushtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-pushtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::PushTemplate",
  "Properties" : {
      "[ADM](#cfn-pinpoint-pushtemplate-adm)" : AndroidPushNotificationTemplate,
      "[APNS](#cfn-pinpoint-pushtemplate-apns)" : APNSPushNotificationTemplate,
      "[Baidu](#cfn-pinpoint-pushtemplate-baidu)" : AndroidPushNotificationTemplate,
      "[Default](#cfn-pinpoint-pushtemplate-default)" : DefaultPushNotificationTemplate,
      "[DefaultSubstitutions](#cfn-pinpoint-pushtemplate-defaultsubstitutions)" : String,
      "[GCM](#cfn-pinpoint-pushtemplate-gcm)" : AndroidPushNotificationTemplate,
      "[Tags](#cfn-pinpoint-pushtemplate-tags)" : Json,
      "[TemplateDescription](#cfn-pinpoint-pushtemplate-templatedescription)" : String,
      "[TemplateName](#cfn-pinpoint-pushtemplate-templatename)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-pushtemplate-syntax.yaml"></a>

```
Type: AWS::Pinpoint::PushTemplate
Properties: 
  [ADM](#cfn-pinpoint-pushtemplate-adm): 
    AndroidPushNotificationTemplate
  [APNS](#cfn-pinpoint-pushtemplate-apns): 
    APNSPushNotificationTemplate
  [Baidu](#cfn-pinpoint-pushtemplate-baidu): 
    AndroidPushNotificationTemplate
  [Default](#cfn-pinpoint-pushtemplate-default): 
    DefaultPushNotificationTemplate
  [DefaultSubstitutions](#cfn-pinpoint-pushtemplate-defaultsubstitutions): String
  [GCM](#cfn-pinpoint-pushtemplate-gcm): 
    AndroidPushNotificationTemplate
  [Tags](#cfn-pinpoint-pushtemplate-tags): Json
  [TemplateDescription](#cfn-pinpoint-pushtemplate-templatedescription): String
  [TemplateName](#cfn-pinpoint-pushtemplate-templatename): String
```

## Properties<a name="aws-resource-pinpoint-pushtemplate-properties"></a>

`ADM`  <a name="cfn-pinpoint-pushtemplate-adm"></a>
The message template to use for the ADM \(Amazon Device Messaging\) channel\. This message template overrides the default template for push notification channels \(`Default`\)\.  
*Required*: No  
*Type*: [AndroidPushNotificationTemplate](aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`APNS`  <a name="cfn-pinpoint-pushtemplate-apns"></a>
The message template to use for the APNs \(Apple Push Notification service\) channel\. This message template overrides the default template for push notification channels \(`Default`\)\.  
*Required*: No  
*Type*: [APNSPushNotificationTemplate](aws-properties-pinpoint-pushtemplate-apnspushnotificationtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Baidu`  <a name="cfn-pinpoint-pushtemplate-baidu"></a>
The message template to use for the Baidu \(Baidu Cloud Push\) channel\. This message template overrides the default template for push notification channels \(`Default`\)\.  
*Required*: No  
*Type*: [AndroidPushNotificationTemplate](aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Default`  <a name="cfn-pinpoint-pushtemplate-default"></a>
The default message template to use for push notification channels\.  
*Required*: No  
*Type*: [DefaultPushNotificationTemplate](aws-properties-pinpoint-pushtemplate-defaultpushnotificationtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultSubstitutions`  <a name="cfn-pinpoint-pushtemplate-defaultsubstitutions"></a>
A JSON object that specifies the default values to use for message variables in the message template\. This object is a set of key\-value pairs\. Each key defines a message variable in the template\. The corresponding value defines the default value for that variable\. When you create a message that's based on the template, you can override these defaults with message\-specific and address\-specific variables and values\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GCM`  <a name="cfn-pinpoint-pushtemplate-gcm"></a>
The message template to use for the GCM channel, which is used to send notifications through the Firebase Cloud Messaging \(FCM\), formerly Google Cloud Messaging \(GCM\), service\. This message template overrides the default template for push notification channels \(`Default`\)\.  
*Required*: No  
*Type*: [AndroidPushNotificationTemplate](aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-pinpoint-pushtemplate-tags"></a>
A string\-to\-string map of key\-value pairs that defines the tags to associate with the message template\. Each tag consists of a required tag key and an associated tag value\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateDescription`  <a name="cfn-pinpoint-pushtemplate-templatedescription"></a>
A custom description of the message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-pinpoint-pushtemplate-templatename"></a>
The name of the message template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-pinpoint-pushtemplate-return-values"></a>

### Ref<a name="aws-resource-pinpoint-pushtemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the message template \(`TemplateName`\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpoint-pushtemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pinpoint-pushtemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the message template\.