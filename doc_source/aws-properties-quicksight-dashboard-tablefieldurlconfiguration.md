# AWS::QuickSight::Dashboard TableFieldURLConfiguration<a name="aws-properties-quicksight-dashboard-tablefieldurlconfiguration"></a>

The URL configuration for a table field\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablefieldurlconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablefieldurlconfiguration-syntax.json"></a>

```
{
  "[ImageConfiguration](#cfn-quicksight-dashboard-tablefieldurlconfiguration-imageconfiguration)" : TableFieldImageConfiguration,
  "[LinkConfiguration](#cfn-quicksight-dashboard-tablefieldurlconfiguration-linkconfiguration)" : TableFieldLinkConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablefieldurlconfiguration-syntax.yaml"></a>

```
  [ImageConfiguration](#cfn-quicksight-dashboard-tablefieldurlconfiguration-imageconfiguration): 
    TableFieldImageConfiguration
  [LinkConfiguration](#cfn-quicksight-dashboard-tablefieldurlconfiguration-linkconfiguration): 
    TableFieldLinkConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-tablefieldurlconfiguration-properties"></a>

`ImageConfiguration`  <a name="cfn-quicksight-dashboard-tablefieldurlconfiguration-imageconfiguration"></a>
The image configuration of a table field URL\.  
*Required*: No  
*Type*: [TableFieldImageConfiguration](aws-properties-quicksight-dashboard-tablefieldimageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LinkConfiguration`  <a name="cfn-quicksight-dashboard-tablefieldurlconfiguration-linkconfiguration"></a>
The link configuration of a table field URL\.  
*Required*: No  
*Type*: [TableFieldLinkConfiguration](aws-properties-quicksight-dashboard-tablefieldlinkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)