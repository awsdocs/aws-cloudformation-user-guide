# AWS::QuickSight::Dashboard FilledMapConfiguration<a name="aws-properties-quicksight-dashboard-filledmapconfiguration"></a>

The configuration for a `FilledMapVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-filledmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filledmapconfiguration-syntax.json"></a>

```
{
  "[FieldWells](#cfn-quicksight-dashboard-filledmapconfiguration-fieldwells)" : FilledMapFieldWells,
  "[Legend](#cfn-quicksight-dashboard-filledmapconfiguration-legend)" : LegendOptions,
  "[MapStyleOptions](#cfn-quicksight-dashboard-filledmapconfiguration-mapstyleoptions)" : GeospatialMapStyleOptions,
  "[SortConfiguration](#cfn-quicksight-dashboard-filledmapconfiguration-sortconfiguration)" : FilledMapSortConfiguration,
  "[Tooltip](#cfn-quicksight-dashboard-filledmapconfiguration-tooltip)" : TooltipOptions,
  "[WindowOptions](#cfn-quicksight-dashboard-filledmapconfiguration-windowoptions)" : GeospatialWindowOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filledmapconfiguration-syntax.yaml"></a>

```
  [FieldWells](#cfn-quicksight-dashboard-filledmapconfiguration-fieldwells): 
    FilledMapFieldWells
  [Legend](#cfn-quicksight-dashboard-filledmapconfiguration-legend): 
    LegendOptions
  [MapStyleOptions](#cfn-quicksight-dashboard-filledmapconfiguration-mapstyleoptions): 
    GeospatialMapStyleOptions
  [SortConfiguration](#cfn-quicksight-dashboard-filledmapconfiguration-sortconfiguration): 
    FilledMapSortConfiguration
  [Tooltip](#cfn-quicksight-dashboard-filledmapconfiguration-tooltip): 
    TooltipOptions
  [WindowOptions](#cfn-quicksight-dashboard-filledmapconfiguration-windowoptions): 
    GeospatialWindowOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-filledmapconfiguration-properties"></a>

`FieldWells`  <a name="cfn-quicksight-dashboard-filledmapconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [FilledMapFieldWells](aws-properties-quicksight-dashboard-filledmapfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-dashboard-filledmapconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-dashboard-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapStyleOptions`  <a name="cfn-quicksight-dashboard-filledmapconfiguration-mapstyleoptions"></a>
The map style options of the filled map visual\.  
*Required*: No  
*Type*: [GeospatialMapStyleOptions](aws-properties-quicksight-dashboard-geospatialmapstyleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-filledmapconfiguration-sortconfiguration"></a>
The sort configuration of a `FilledMapVisual`\.  
*Required*: No  
*Type*: [FilledMapSortConfiguration](aws-properties-quicksight-dashboard-filledmapsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-dashboard-filledmapconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-dashboard-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowOptions`  <a name="cfn-quicksight-dashboard-filledmapconfiguration-windowoptions"></a>
The window options of the filled map visual\.  
*Required*: No  
*Type*: [GeospatialWindowOptions](aws-properties-quicksight-dashboard-geospatialwindowoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)