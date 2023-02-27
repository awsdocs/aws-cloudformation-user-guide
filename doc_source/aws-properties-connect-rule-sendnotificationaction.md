# AWS::Connect::Rule SendNotificationAction<a name="aws-properties-connect-rule-sendnotificationaction"></a>

Information about the send notification action\.

## Syntax<a name="aws-properties-connect-rule-sendnotificationaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-rule-sendnotificationaction-syntax.json"></a>

```
{
  "[Content](#cfn-connect-rule-sendnotificationaction-content)" : String,
  "[ContentType](#cfn-connect-rule-sendnotificationaction-contenttype)" : String,
  "[DeliveryMethod](#cfn-connect-rule-sendnotificationaction-deliverymethod)" : String,
  "[Recipient](#cfn-connect-rule-sendnotificationaction-recipient)" : NotificationRecipientType,
  "[Subject](#cfn-connect-rule-sendnotificationaction-subject)" : String
}
```

### YAML<a name="aws-properties-connect-rule-sendnotificationaction-syntax.yaml"></a>

```
  [Content](#cfn-connect-rule-sendnotificationaction-content): String
  [ContentType](#cfn-connect-rule-sendnotificationaction-contenttype): String
  [DeliveryMethod](#cfn-connect-rule-sendnotificationaction-deliverymethod): String
  [Recipient](#cfn-connect-rule-sendnotificationaction-recipient): 
    NotificationRecipientType
  [Subject](#cfn-connect-rule-sendnotificationaction-subject): String
```

## Properties<a name="aws-properties-connect-rule-sendnotificationaction-properties"></a>

`Content`  <a name="cfn-connect-rule-sendnotificationaction-content"></a>
Notification content\. Supports variable injection\. For more information, see [JSONPath reference](https://docs.aws.amazon.com/connect/latest/adminguide/contact-lens-variable-injection.html) in the *Amazon Connect Administrators Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentType`  <a name="cfn-connect-rule-sendnotificationaction-contenttype"></a>
Content type format\.  
*Allowed value*: `PLAIN_TEXT`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeliveryMethod`  <a name="cfn-connect-rule-sendnotificationaction-deliverymethod"></a>
Notification delivery method\.  
*Allowed value*: `EMAIL`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Recipient`  <a name="cfn-connect-rule-sendnotificationaction-recipient"></a>
Notification recipient\.  
*Required*: Yes  
*Type*: [NotificationRecipientType](aws-properties-connect-rule-notificationrecipienttype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subject`  <a name="cfn-connect-rule-sendnotificationaction-subject"></a>
The subject of the email if the delivery method is `EMAIL`\. Supports variable injection\. For more information, see [JSONPath reference](https://docs.aws.amazon.com/connect/latest/adminguide/contact-lens-variable-injection.html) in the *Amazon Connect Administrators Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)