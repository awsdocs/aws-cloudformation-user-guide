# AWS::QuickSight::Template TableFieldCustomTextContent<a name="aws-properties-quicksight-template-tablefieldcustomtextcontent"></a>

The custom text content \(value, font configuration\) for the table link content configuration\.

## Syntax<a name="aws-properties-quicksight-template-tablefieldcustomtextcontent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tablefieldcustomtextcontent-syntax.json"></a>

```
{
  "[FontConfiguration](#cfn-quicksight-template-tablefieldcustomtextcontent-fontconfiguration)" : FontConfiguration,
  "[Value](#cfn-quicksight-template-tablefieldcustomtextcontent-value)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-tablefieldcustomtextcontent-syntax.yaml"></a>

```
  [FontConfiguration](#cfn-quicksight-template-tablefieldcustomtextcontent-fontconfiguration): 
    FontConfiguration
  [Value](#cfn-quicksight-template-tablefieldcustomtextcontent-value): String
```

## Properties<a name="aws-properties-quicksight-template-tablefieldcustomtextcontent-properties"></a>

`FontConfiguration`  <a name="cfn-quicksight-template-tablefieldcustomtextcontent-fontconfiguration"></a>
The font configuration of the custom text content for the table URL link content\.  
*Required*: Yes  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-template-tablefieldcustomtextcontent-value"></a>
The string value of the custom text content for the table URL link content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)