# AWS::Pinpoint::Campaign Message<a name="aws-properties-pinpoint-campaign-message"></a>

Specifies the content and settings for a push notification that's sent to recipients of a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-message-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-message-syntax.json"></a>

```
{
  "[Action](#cfn-pinpoint-campaign-message-action)" : String,
  "[Body](#cfn-pinpoint-campaign-message-body)" : String,
  "[ImageIconUrl](#cfn-pinpoint-campaign-message-imageiconurl)" : String,
  "[ImageSmallIconUrl](#cfn-pinpoint-campaign-message-imagesmalliconurl)" : String,
  "[ImageUrl](#cfn-pinpoint-campaign-message-imageurl)" : String,
  "[JsonBody](#cfn-pinpoint-campaign-message-jsonbody)" : String,
  "[MediaUrl](#cfn-pinpoint-campaign-message-mediaurl)" : String,
  "[RawContent](#cfn-pinpoint-campaign-message-rawcontent)" : String,
  "[SilentPush](#cfn-pinpoint-campaign-message-silentpush)" : Boolean,
  "[TimeToLive](#cfn-pinpoint-campaign-message-timetolive)" : Integer,
  "[Title](#cfn-pinpoint-campaign-message-title)" : String,
  "[Url](#cfn-pinpoint-campaign-message-url)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-message-syntax.yaml"></a>

```
  [Action](#cfn-pinpoint-campaign-message-action): String
  [Body](#cfn-pinpoint-campaign-message-body): String
  [ImageIconUrl](#cfn-pinpoint-campaign-message-imageiconurl): String
  [ImageSmallIconUrl](#cfn-pinpoint-campaign-message-imagesmalliconurl): String
  [ImageUrl](#cfn-pinpoint-campaign-message-imageurl): String
  [JsonBody](#cfn-pinpoint-campaign-message-jsonbody): String
  [MediaUrl](#cfn-pinpoint-campaign-message-mediaurl): String
  [RawContent](#cfn-pinpoint-campaign-message-rawcontent): String
  [SilentPush](#cfn-pinpoint-campaign-message-silentpush): Boolean
  [TimeToLive](#cfn-pinpoint-campaign-message-timetolive): Integer
  [Title](#cfn-pinpoint-campaign-message-title): String
  [Url](#cfn-pinpoint-campaign-message-url): String
```

## Properties<a name="aws-properties-pinpoint-campaign-message-properties"></a>

`Action`  <a name="cfn-pinpoint-campaign-message-action"></a>
The action to occur if a recipient taps the push notification\. Valid values are:  
+  `OPEN_APP` \- Your app opens or it becomes the foreground app if it was sent to the background\. This is the default action\.
+  `DEEP_LINK` \- Your app opens and displays a designated user interface in the app\. This setting uses the deep\-linking features of iOS and Android\.
+  `URL` \- The default mobile browser on the recipient's device opens and loads the web page at a URL that you specify\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-pinpoint-campaign-message-body"></a>
The body of the notification message\. The maximum number of characters is 200\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageIconUrl`  <a name="cfn-pinpoint-campaign-message-imageiconurl"></a>
The URL of the image to display as the push\-notification icon, such as the icon for the app\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageSmallIconUrl`  <a name="cfn-pinpoint-campaign-message-imagesmalliconurl"></a>
The URL of the image to display as the small, push\-notification icon, such as a small version of the icon for the app\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageUrl`  <a name="cfn-pinpoint-campaign-message-imageurl"></a>
The URL of an image to display in the push notification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JsonBody`  <a name="cfn-pinpoint-campaign-message-jsonbody"></a>
The JSON payload to use for a silent push notification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaUrl`  <a name="cfn-pinpoint-campaign-message-mediaurl"></a>
The URL of the image or video to display in the push notification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RawContent`  <a name="cfn-pinpoint-campaign-message-rawcontent"></a>
The raw, JSON\-formatted string to use as the payload for the notification message\. If specified, this value overrides all other content for the message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SilentPush`  <a name="cfn-pinpoint-campaign-message-silentpush"></a>
Specifies whether the notification is a silent push notification, which is a push notification that doesn't display on a recipient's device\. Silent push notifications can be used for cases such as updating an app's configuration, displaying messages in an in\-app message center, or supporting phone home functionality\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeToLive`  <a name="cfn-pinpoint-campaign-message-timetolive"></a>
The number of seconds that the push\-notification service should keep the message, if the service is unable to deliver the notification the first time\. This value is converted to an expiration value when it's sent to a push\-notification service\. If this value is `0`, the service treats the notification as if it expires immediately and the service doesn't store or try to deliver the notification again\.  
This value doesn't apply to messages that are sent through the Amazon Device Messaging \(ADM\) service\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-pinpoint-campaign-message-title"></a>
The title to display above the notification message on a recipient's device\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-pinpoint-campaign-message-url"></a>
The URL to open in a recipient's default mobile browser, if a recipient taps the push notification and the value of the `Action` property is `URL`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)