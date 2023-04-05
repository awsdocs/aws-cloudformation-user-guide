# AWS::QuickSight::Dashboard TableFieldLinkContentConfiguration<a name="aws-properties-quicksight-dashboard-tablefieldlinkcontentconfiguration"></a>

The URL content \(text, icon\) for the table link configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablefieldlinkcontentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablefieldlinkcontentconfiguration-syntax.json"></a>

```
{
  "[CustomIconContent](#cfn-quicksight-dashboard-tablefieldlinkcontentconfiguration-customiconcontent)" : TableFieldCustomIconContent,
  "[CustomTextContent](#cfn-quicksight-dashboard-tablefieldlinkcontentconfiguration-customtextcontent)" : TableFieldCustomTextContent
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablefieldlinkcontentconfiguration-syntax.yaml"></a>

```
  [CustomIconContent](#cfn-quicksight-dashboard-tablefieldlinkcontentconfiguration-customiconcontent): 
    TableFieldCustomIconContent
  [CustomTextContent](#cfn-quicksight-dashboard-tablefieldlinkcontentconfiguration-customtextcontent): 
    TableFieldCustomTextContent
```

## Properties<a name="aws-properties-quicksight-dashboard-tablefieldlinkcontentconfiguration-properties"></a>

`CustomIconContent`  <a name="cfn-quicksight-dashboard-tablefieldlinkcontentconfiguration-customiconcontent"></a>
The custom icon content for the table link content configuration\.  
*Required*: No  
*Type*: [TableFieldCustomIconContent](aws-properties-quicksight-dashboard-tablefieldcustomiconcontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomTextContent`  <a name="cfn-quicksight-dashboard-tablefieldlinkcontentconfiguration-customtextcontent"></a>
The custom text content \(value, font configuration\) for the table link content configuration\.  
*Required*: No  
*Type*: [TableFieldCustomTextContent](aws-properties-quicksight-dashboard-tablefieldcustomtextcontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)