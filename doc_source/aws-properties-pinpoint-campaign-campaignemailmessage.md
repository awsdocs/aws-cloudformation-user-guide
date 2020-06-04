# AWS::Pinpoint::Campaign CampaignEmailMessage<a name="aws-properties-pinpoint-campaign-campaignemailmessage"></a>

Specifies the content and "From" address for an email message that's sent to recipients of a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-campaignemailmessage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-campaignemailmessage-syntax.json"></a>

```
{
  "[Body](#cfn-pinpoint-campaign-campaignemailmessage-body)" : String,
  "[FromAddress](#cfn-pinpoint-campaign-campaignemailmessage-fromaddress)" : String,
  "[HtmlBody](#cfn-pinpoint-campaign-campaignemailmessage-htmlbody)" : String,
  "[Title](#cfn-pinpoint-campaign-campaignemailmessage-title)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-campaignemailmessage-syntax.yaml"></a>

```
  [Body](#cfn-pinpoint-campaign-campaignemailmessage-body): String
  [FromAddress](#cfn-pinpoint-campaign-campaignemailmessage-fromaddress): String
  [HtmlBody](#cfn-pinpoint-campaign-campaignemailmessage-htmlbody): String
  [Title](#cfn-pinpoint-campaign-campaignemailmessage-title): String
```

## Properties<a name="aws-properties-pinpoint-campaign-campaignemailmessage-properties"></a>

`Body`  <a name="cfn-pinpoint-campaign-campaignemailmessage-body"></a>
The body of the email for recipients whose email clients don't render HTML content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FromAddress`  <a name="cfn-pinpoint-campaign-campaignemailmessage-fromaddress"></a>
The verified email address to send the email from\. The default address is the `FromAddress` specified for the email channel for the application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HtmlBody`  <a name="cfn-pinpoint-campaign-campaignemailmessage-htmlbody"></a>
The body of the email, in HTML format, for recipients whose email clients render HTML content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-pinpoint-campaign-campaignemailmessage-title"></a>
The subject line, or title, of the email\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)