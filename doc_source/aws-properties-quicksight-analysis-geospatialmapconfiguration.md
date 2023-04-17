# AWS::QuickSight::Analysis GeospatialMapConfiguration<a name="aws-properties-quicksight-analysis-geospatialmapconfiguration"></a>

The configuration of a `GeospatialMapVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-geospatialmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-geospatialmapconfiguration-syntax.json"></a>

```
{
  "[FieldWells](#cfn-quicksight-analysis-geospatialmapconfiguration-fieldwells)" : GeospatialMapFieldWells,
  "[Legend](#cfn-quicksight-analysis-geospatialmapconfiguration-legend)" : LegendOptions,
  "[MapStyleOptions](#cfn-quicksight-analysis-geospatialmapconfiguration-mapstyleoptions)" : GeospatialMapStyleOptions,
  "[PointStyleOptions](#cfn-quicksight-analysis-geospatialmapconfiguration-pointstyleoptions)" : GeospatialPointStyleOptions,
  "[Tooltip](#cfn-quicksight-analysis-geospatialmapconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-analysis-geospatialmapconfiguration-visualpalette)" : VisualPalette,
  "[WindowOptions](#cfn-quicksight-analysis-geospatialmapconfiguration-windowoptions)" : GeospatialWindowOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-geospatialmapconfiguration-syntax.yaml"></a>

```
  [FieldWells](#cfn-quicksight-analysis-geospatialmapconfiguration-fieldwells): 
    GeospatialMapFieldWells
  [Legend](#cfn-quicksight-analysis-geospatialmapconfiguration-legend): 
    LegendOptions
  [MapStyleOptions](#cfn-quicksight-analysis-geospatialmapconfiguration-mapstyleoptions): 
    GeospatialMapStyleOptions
  [PointStyleOptions](#cfn-quicksight-analysis-geospatialmapconfiguration-pointstyleoptions): 
    GeospatialPointStyleOptions
  [Tooltip](#cfn-quicksight-analysis-geospatialmapconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-analysis-geospatialmapconfiguration-visualpalette): 
    VisualPalette
  [WindowOptions](#cfn-quicksight-analysis-geospatialmapconfiguration-windowoptions): 
    GeospatialWindowOptions
```

## Properties<a name="aws-properties-quicksight-analysis-geospatialmapconfiguration-properties"></a>

`FieldWells`  <a name="cfn-quicksight-analysis-geospatialmapconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [GeospatialMapFieldWells](aws-properties-quicksight-analysis-geospatialmapfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-analysis-geospatialmapconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-analysis-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapStyleOptions`  <a name="cfn-quicksight-analysis-geospatialmapconfiguration-mapstyleoptions"></a>
The map style options of the geospatial map\.  
*Required*: No  
*Type*: [GeospatialMapStyleOptions](aws-properties-quicksight-analysis-geospatialmapstyleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PointStyleOptions`  <a name="cfn-quicksight-analysis-geospatialmapconfiguration-pointstyleoptions"></a>
The point style options of the geospatial map\.  
*Required*: No  
*Type*: [GeospatialPointStyleOptions](aws-properties-quicksight-analysis-geospatialpointstyleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-analysis-geospatialmapconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-analysis-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-analysis-geospatialmapconfiguration-visualpalette"></a>
Property description not available\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-analysis-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowOptions`  <a name="cfn-quicksight-analysis-geospatialmapconfiguration-windowoptions"></a>
The window options of the geospatial map\.  
*Required*: No  
*Type*: [GeospatialWindowOptions](aws-properties-quicksight-analysis-geospatialwindowoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)