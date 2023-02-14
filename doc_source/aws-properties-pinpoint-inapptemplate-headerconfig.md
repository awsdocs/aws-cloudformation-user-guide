# AWS::Pinpoint::InAppTemplate HeaderConfig<a name="aws-properties-pinpoint-inapptemplate-headerconfig"></a>

Specifies the configuration and content of the header or title text of the in\-app message\.

## Syntax<a name="aws-properties-pinpoint-inapptemplate-headerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-inapptemplate-headerconfig-syntax.json"></a>

```
{
  "[Alignment](#cfn-pinpoint-inapptemplate-headerconfig-alignment)" : String,
  "[Header](#cfn-pinpoint-inapptemplate-headerconfig-header)" : String,
  "[TextColor](#cfn-pinpoint-inapptemplate-headerconfig-textcolor)" : String
}
```

### YAML<a name="aws-properties-pinpoint-inapptemplate-headerconfig-syntax.yaml"></a>

```
  [Alignment](#cfn-pinpoint-inapptemplate-headerconfig-alignment): String
  [Header](#cfn-pinpoint-inapptemplate-headerconfig-header): String
  [TextColor](#cfn-pinpoint-inapptemplate-headerconfig-textcolor): String
```

## Properties<a name="aws-properties-pinpoint-inapptemplate-headerconfig-properties"></a>

`Alignment`  <a name="cfn-pinpoint-inapptemplate-headerconfig-alignment"></a>
The text alignment of the title of the message\. Acceptable values: `LEFT`, `CENTER`, `RIGHT`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Header`  <a name="cfn-pinpoint-inapptemplate-headerconfig-header"></a>
The title text of the in\-app message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextColor`  <a name="cfn-pinpoint-inapptemplate-headerconfig-textcolor"></a>
The color of the title text, expressed as a hex color code \(such as \#000000 for black\)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)