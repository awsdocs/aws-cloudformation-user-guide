# AWS::Pinpoint::InAppTemplate OverrideButtonConfiguration<a name="aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration"></a>

Specifies the configuration of a button with settings that are specific to a certain device type\.

## Syntax<a name="aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration-syntax.json"></a>

```
{
  "[ButtonAction](#cfn-pinpoint-inapptemplate-overridebuttonconfiguration-buttonaction)" : String,
  "[Link](#cfn-pinpoint-inapptemplate-overridebuttonconfiguration-link)" : String
}
```

### YAML<a name="aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration-syntax.yaml"></a>

```
  [ButtonAction](#cfn-pinpoint-inapptemplate-overridebuttonconfiguration-buttonaction): String
  [Link](#cfn-pinpoint-inapptemplate-overridebuttonconfiguration-link): String
```

## Properties<a name="aws-properties-pinpoint-inapptemplate-overridebuttonconfiguration-properties"></a>

`ButtonAction`  <a name="cfn-pinpoint-inapptemplate-overridebuttonconfiguration-buttonaction"></a>
The action that occurs when a recipient chooses a button in an in\-app message\. You can specify one of the following:  
+  `LINK` – A link to a web destination\.
+  `DEEP_LINK` – A link to a specific page in an application\.
+  `CLOSE` – Dismisses the message\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Link`  <a name="cfn-pinpoint-inapptemplate-overridebuttonconfiguration-link"></a>
The destination \(such as a URL\) for a button\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)