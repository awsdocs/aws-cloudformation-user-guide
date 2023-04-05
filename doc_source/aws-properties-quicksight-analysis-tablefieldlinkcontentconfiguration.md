# AWS::QuickSight::Analysis TableFieldLinkContentConfiguration<a name="aws-properties-quicksight-analysis-tablefieldlinkcontentconfiguration"></a>

The URL content \(text, icon\) for the table link configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-tablefieldlinkcontentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tablefieldlinkcontentconfiguration-syntax.json"></a>

```
{
  "[CustomIconContent](#cfn-quicksight-analysis-tablefieldlinkcontentconfiguration-customiconcontent)" : TableFieldCustomIconContent,
  "[CustomTextContent](#cfn-quicksight-analysis-tablefieldlinkcontentconfiguration-customtextcontent)" : TableFieldCustomTextContent
}
```

### YAML<a name="aws-properties-quicksight-analysis-tablefieldlinkcontentconfiguration-syntax.yaml"></a>

```
  [CustomIconContent](#cfn-quicksight-analysis-tablefieldlinkcontentconfiguration-customiconcontent): 
    TableFieldCustomIconContent
  [CustomTextContent](#cfn-quicksight-analysis-tablefieldlinkcontentconfiguration-customtextcontent): 
    TableFieldCustomTextContent
```

## Properties<a name="aws-properties-quicksight-analysis-tablefieldlinkcontentconfiguration-properties"></a>

`CustomIconContent`  <a name="cfn-quicksight-analysis-tablefieldlinkcontentconfiguration-customiconcontent"></a>
The custom icon content for the table link content configuration\.  
*Required*: No  
*Type*: [TableFieldCustomIconContent](aws-properties-quicksight-analysis-tablefieldcustomiconcontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomTextContent`  <a name="cfn-quicksight-analysis-tablefieldlinkcontentconfiguration-customtextcontent"></a>
The custom text content \(value, font configuration\) for the table link content configuration\.  
*Required*: No  
*Type*: [TableFieldCustomTextContent](aws-properties-quicksight-analysis-tablefieldcustomtextcontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)