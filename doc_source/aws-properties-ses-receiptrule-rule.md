# AWS::SES::ReceiptRule Rule<a name="aws-properties-ses-receiptrule-rule"></a>

Receipt rules enable you to specify which actions Amazon SES should take when it receives mail on behalf of one or more email addresses or domains that you own\.

Each receipt rule defines a set of email addresses or domains that it applies to\. If the email addresses or domains match at least one recipient address of the message, Amazon SES executes all of the receipt rule's actions on the message\.

For information about setting up receipt rules, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-receipt-rules.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-rule-syntax.json"></a>

```
{
  "[Actions](#cfn-ses-receiptrule-rule-actions)" : [ Action, ... ],
  "[Enabled](#cfn-ses-receiptrule-rule-enabled)" : Boolean,
  "[Name](#cfn-ses-receiptrule-rule-name)" : String,
  "[Recipients](#cfn-ses-receiptrule-rule-recipients)" : [ String, ... ],
  "[ScanEnabled](#cfn-ses-receiptrule-rule-scanenabled)" : Boolean,
  "[TlsPolicy](#cfn-ses-receiptrule-rule-tlspolicy)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-rule-syntax.yaml"></a>

```
  [Actions](#cfn-ses-receiptrule-rule-actions): 
    - Action
  [Enabled](#cfn-ses-receiptrule-rule-enabled): Boolean
  [Name](#cfn-ses-receiptrule-rule-name): String
  [Recipients](#cfn-ses-receiptrule-rule-recipients): 
    - String
  [ScanEnabled](#cfn-ses-receiptrule-rule-scanenabled): Boolean
  [TlsPolicy](#cfn-ses-receiptrule-rule-tlspolicy): String
```

## Properties<a name="aws-properties-ses-receiptrule-rule-properties"></a>

`Actions`  <a name="cfn-ses-receiptrule-rule-actions"></a>
An ordered list of actions to perform on messages that match at least one of the recipient email addresses or domains specified in the receipt rule\.  
*Required*: No  
*Type*: List of [Action](aws-properties-ses-receiptrule-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-ses-receiptrule-rule-enabled"></a>
If `true`, the receipt rule is active\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ses-receiptrule-rule-name"></a>
The name of the receipt rule\. The name must:  
+ This value can only contain ASCII letters \(a–z, A–Z\), numbers \(0–9\), underscores \(\_\), or dashes \(\-\)\.
+ Start and end with a letter or number\.
+ Contain fewer than 64 characters\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Recipients`  <a name="cfn-ses-receiptrule-rule-recipients"></a>
Contains the recipient domains and email addresses that the receipt rule applies to\. If this field isn't specified, this rule matches all recipients on all verified domains\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScanEnabled`  <a name="cfn-ses-receiptrule-rule-scanenabled"></a>
If `true`, then messages that this receipt rule applies to are scanned for spam and viruses\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TlsPolicy`  <a name="cfn-ses-receiptrule-rule-tlspolicy"></a>
Specifies whether Amazon SES should require that incoming email is delivered over a connection encrypted with Transport Layer Security \(TLS\)\. If this parameter is set to `Require`, Amazon SES bounces emails that are not received over TLS\. The default is `Optional`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)