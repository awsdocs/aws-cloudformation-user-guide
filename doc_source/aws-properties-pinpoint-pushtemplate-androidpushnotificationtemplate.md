# AWS::Pinpoint::PushTemplate AndroidPushNotificationTemplate<a name="aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate"></a>

The AWS::Pinpoint::PushTemplate AndroidPushNotificationTemplate resource defines channel\-specific content and settings for a message template that can be used in push notifications that are sent through the following channels: ADM \(Amazon Device Messaging\), Baidu \(Baidu Cloud Push\), or GCM \(Firebase Cloud Messaging, formerly Google Cloud Messaging\)\.

## Syntax<a name="aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate-syntax.json"></a>

```
{
  "[Action](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-action)" : String,
  "[Body](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-body)" : String,
  "[ImageIconUrl](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-imageiconurl)" : String,
  "[ImageUrl](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-imageurl)" : String,
  "[SmallImageIconUrl](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-smallimageiconurl)" : String,
  "[Sound](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-sound)" : String,
  "[Title](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-title)" : String,
  "[Url](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-url)" : String
}
```

### YAML<a name="aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate-syntax.yaml"></a>

```
  [Action](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-action): String
  [Body](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-body): String
  [ImageIconUrl](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-imageiconurl): String
  [ImageUrl](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-imageurl): String
  [SmallImageIconUrl](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-smallimageiconurl): String
  [Sound](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-sound): String
  [Title](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-title): String
  [Url](#cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-url): String
```

## Properties<a name="aws-properties-pinpoint-pushtemplate-androidpushnotificationtemplate-properties"></a>

`Action`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-action"></a>
The action to occur if a recipient taps a push notification that's based on the message template\. Valid values are:  
+  `OPEN_APP` \- Your app opens or it becomes the foreground app if it was sent to the background\. This is the default action\.
+  `DEEP_LINK` \- Your app opens and displays a designated user interface in the app\. This action uses the deep\-linking features of the Android platform\.
+  `URL` \- The default mobile browser on the recipient's device opens and loads the web page at a URL that you specify\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-body"></a>
The message body to use in a push notification that's based on the message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageIconUrl`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-imageiconurl"></a>
The URL of the large icon image to display in the content view of a push notification that's based on the message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageUrl`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-imageurl"></a>
The URL of an image to display in a push notification that's based on the message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallImageIconUrl`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-smallimageiconurl"></a>
The URL of the small icon image to display in the status bar and the content view of a push notification that's based on the message template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sound`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-sound"></a>
The sound to play when a recipient receives a push notification that's based on the message template\. You can use the default stream or specify the file name of a sound resource that's bundled in your app\. On an Android platform, the sound file must reside in `/res/raw/`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-title"></a>
The title to use in a push notification that's based on the message template\. This title appears above the notification message on a recipient's device\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-pinpoint-pushtemplate-androidpushnotificationtemplate-url"></a>
The URL to open in a recipient's default mobile browser, if a recipient taps a push notification that's based on the message template and the value of the `Action` property is `URL`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)