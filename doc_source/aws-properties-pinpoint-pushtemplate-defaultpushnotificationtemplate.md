# AWS::Pinpoint::PushTemplate DefaultPushNotificationTemplate<a name="aws-properties-pinpoint-pushtemplate-defaultpushnotificationtemplate"></a>

The AWS::Pinpoint::PushTemplate DefaultPushNotificationTemplate resource defines the default settings and content for a message template that can be used in messages that are sent through a push notification channel\.

## Syntax<a name="aws-properties-pinpoint-pushtemplate-defaultpushnotificationtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-pushtemplate-defaultpushnotificationtemplate-syntax.json"></a>

```
{
  "[Action](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-action)" : String,
  "[Body](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-body)" : String,
  "[Sound](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-sound)" : String,
  "[Title](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-title)" : String,
  "[Url](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-url)" : String
}
```

### YAML<a name="aws-properties-pinpoint-pushtemplate-defaultpushnotificationtemplate-syntax.yaml"></a>

```
  [Action](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-action): String
  [Body](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-body): String
  [Sound](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-sound): String
  [Title](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-title): String
  [Url](#cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-url): String
```

## Properties<a name="aws-properties-pinpoint-pushtemplate-defaultpushnotificationtemplate-properties"></a>

`Action`  <a name="cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-action"></a>
The action to occur if a recipient taps a push notification that's based on the message template\. Valid values are:  
+  `OPEN_APP` \- Your app opens or it becomes the foreground app if it was sent to the background\. This is the default action\.
+  `DEEP_LINK` \- Your app opens and displays a designated user interface in the app\. This setting uses the deep\-linking features of the iOS and Android platforms\.
+  `URL` \- The default mobile browser on the recipient's device opens and loads the web page at a URL that you specify\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-body"></a>
The message body to use in push notifications that are based on the message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sound`  <a name="cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-sound"></a>
The sound to play when a recipient receives a push notification that's based on the message template\. You can use the default stream or specify the file name of a sound resource that's bundled in your app\. On an Android platform, the sound file must reside in `/res/raw/`\.  
For an iOS platform, this value is the key for the name of a sound file in your app's main bundle or the `Library/Sounds` folder in your app's data container\. If the sound file can't be found or you specify `default` for the value, the system plays the default alert sound\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-title"></a>
The title to use in push notifications that are based on the message template\. This title appears above the notification message on a recipient's device\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-pinpoint-pushtemplate-defaultpushnotificationtemplate-url"></a>
The URL to open in a recipient's default mobile browser, if a recipient taps a push notification that's based on the message template and the value of the `Action` property is `URL`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)