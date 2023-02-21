# AWS::Pinpoint::InAppTemplate DefaultButtonConfiguration<a name="aws-properties-pinpoint-inapptemplate-defaultbuttonconfiguration"></a>

Specifies the default behavior of a button that appears in an in\-app message\. You can optionally add button configurations that specifically apply to iOS, Android, or web browser users\. 

## Syntax<a name="aws-properties-pinpoint-inapptemplate-defaultbuttonconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-inapptemplate-defaultbuttonconfiguration-syntax.json"></a>

```
{
  "[BackgroundColor](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-backgroundcolor)" : String,
  "[BorderRadius](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-borderradius)" : Integer,
  "[ButtonAction](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-buttonaction)" : String,
  "[Link](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-link)" : String,
  "[Text](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-text)" : String,
  "[TextColor](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-textcolor)" : String
}
```

### YAML<a name="aws-properties-pinpoint-inapptemplate-defaultbuttonconfiguration-syntax.yaml"></a>

```
  [BackgroundColor](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-backgroundcolor): String
  [BorderRadius](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-borderradius): Integer
  [ButtonAction](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-buttonaction): String
  [Link](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-link): String
  [Text](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-text): String
  [TextColor](#cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-textcolor): String
```

## Properties<a name="aws-properties-pinpoint-inapptemplate-defaultbuttonconfiguration-properties"></a>

`BackgroundColor`  <a name="cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-backgroundcolor"></a>
The background color of a button, expressed as a hex color code \(such as \#000000 for black\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BorderRadius`  <a name="cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-borderradius"></a>
The border radius of a button\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ButtonAction`  <a name="cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-buttonaction"></a>
The action that occurs when a recipient chooses a button in an in\-app message\. You can specify one of the following:  
+  `LINK` – A link to a web destination\.
+  `DEEP_LINK` – A link to a specific page in an application\.
+  `CLOSE` – Dismisses the message\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Link`  <a name="cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-link"></a>
The destination \(such as a URL\) for a button\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Text`  <a name="cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-text"></a>
The text that appears on a button in an in\-app message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextColor`  <a name="cfn-pinpoint-inapptemplate-defaultbuttonconfiguration-textcolor"></a>
The color of the body text in a button, expressed as a hex color code \(such as \#000000 for black\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)