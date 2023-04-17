# AWS::QuickSight::Template TableFieldLinkContentConfiguration<a name="aws-properties-quicksight-template-tablefieldlinkcontentconfiguration"></a>

The URL content \(text, icon\) for the table link configuration\.

## Syntax<a name="aws-properties-quicksight-template-tablefieldlinkcontentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tablefieldlinkcontentconfiguration-syntax.json"></a>

```
{
  "[CustomIconContent](#cfn-quicksight-template-tablefieldlinkcontentconfiguration-customiconcontent)" : TableFieldCustomIconContent,
  "[CustomTextContent](#cfn-quicksight-template-tablefieldlinkcontentconfiguration-customtextcontent)" : TableFieldCustomTextContent
}
```

### YAML<a name="aws-properties-quicksight-template-tablefieldlinkcontentconfiguration-syntax.yaml"></a>

```
  [CustomIconContent](#cfn-quicksight-template-tablefieldlinkcontentconfiguration-customiconcontent): 
    TableFieldCustomIconContent
  [CustomTextContent](#cfn-quicksight-template-tablefieldlinkcontentconfiguration-customtextcontent): 
    TableFieldCustomTextContent
```

## Properties<a name="aws-properties-quicksight-template-tablefieldlinkcontentconfiguration-properties"></a>

`CustomIconContent`  <a name="cfn-quicksight-template-tablefieldlinkcontentconfiguration-customiconcontent"></a>
The custom icon content for the table link content configuration\.  
*Required*: No  
*Type*: [TableFieldCustomIconContent](aws-properties-quicksight-template-tablefieldcustomiconcontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomTextContent`  <a name="cfn-quicksight-template-tablefieldlinkcontentconfiguration-customtextcontent"></a>
The custom text content \(value, font configuration\) for the table link content configuration\.  
*Required*: No  
*Type*: [TableFieldCustomTextContent](aws-properties-quicksight-template-tablefieldcustomtextcontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)