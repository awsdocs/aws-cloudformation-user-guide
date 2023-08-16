# AWS::QuickSight::Template TableFieldURLConfiguration<a name="aws-properties-quicksight-template-tablefieldurlconfiguration"></a>

The URL configuration for a table field\.

## Syntax<a name="aws-properties-quicksight-template-tablefieldurlconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tablefieldurlconfiguration-syntax.json"></a>

```
{
  "[ImageConfiguration](#cfn-quicksight-template-tablefieldurlconfiguration-imageconfiguration)" : TableFieldImageConfiguration,
  "[LinkConfiguration](#cfn-quicksight-template-tablefieldurlconfiguration-linkconfiguration)" : TableFieldLinkConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-tablefieldurlconfiguration-syntax.yaml"></a>

```
  [ImageConfiguration](#cfn-quicksight-template-tablefieldurlconfiguration-imageconfiguration): 
    TableFieldImageConfiguration
  [LinkConfiguration](#cfn-quicksight-template-tablefieldurlconfiguration-linkconfiguration): 
    TableFieldLinkConfiguration
```

## Properties<a name="aws-properties-quicksight-template-tablefieldurlconfiguration-properties"></a>

`ImageConfiguration`  <a name="cfn-quicksight-template-tablefieldurlconfiguration-imageconfiguration"></a>
The image configuration of a table field URL\.  
*Required*: No  
*Type*: [TableFieldImageConfiguration](aws-properties-quicksight-template-tablefieldimageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LinkConfiguration`  <a name="cfn-quicksight-template-tablefieldurlconfiguration-linkconfiguration"></a>
The link configuration of a table field URL\.  
*Required*: No  
*Type*: [TableFieldLinkConfiguration](aws-properties-quicksight-template-tablefieldlinkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)