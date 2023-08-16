# AWS::QuickSight::Dashboard TableCellImageSizingConfiguration<a name="aws-properties-quicksight-dashboard-tablecellimagesizingconfiguration"></a>

The sizing options for the table image configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablecellimagesizingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablecellimagesizingconfiguration-syntax.json"></a>

```
{
  "[TableCellImageScalingConfiguration](#cfn-quicksight-dashboard-tablecellimagesizingconfiguration-tablecellimagescalingconfiguration)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablecellimagesizingconfiguration-syntax.yaml"></a>

```
  [TableCellImageScalingConfiguration](#cfn-quicksight-dashboard-tablecellimagesizingconfiguration-tablecellimagescalingconfiguration): String
```

## Properties<a name="aws-properties-quicksight-dashboard-tablecellimagesizingconfiguration-properties"></a>

`TableCellImageScalingConfiguration`  <a name="cfn-quicksight-dashboard-tablecellimagesizingconfiguration-tablecellimagescalingconfiguration"></a>
The cell scaling configuration of the sizing options for the table image configuration\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DO_NOT_SCALE | FIT_TO_CELL_HEIGHT | FIT_TO_CELL_WIDTH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)