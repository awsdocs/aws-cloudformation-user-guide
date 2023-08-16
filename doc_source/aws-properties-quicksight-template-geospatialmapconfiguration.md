# AWS::QuickSight::Template GeospatialMapConfiguration<a name="aws-properties-quicksight-template-geospatialmapconfiguration"></a>

The configuration of a `GeospatialMapVisual`\.

## Syntax<a name="aws-properties-quicksight-template-geospatialmapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-geospatialmapconfiguration-syntax.json"></a>

```
{
  "[FieldWells](#cfn-quicksight-template-geospatialmapconfiguration-fieldwells)" : GeospatialMapFieldWells,
  "[Legend](#cfn-quicksight-template-geospatialmapconfiguration-legend)" : LegendOptions,
  "[MapStyleOptions](#cfn-quicksight-template-geospatialmapconfiguration-mapstyleoptions)" : GeospatialMapStyleOptions,
  "[PointStyleOptions](#cfn-quicksight-template-geospatialmapconfiguration-pointstyleoptions)" : GeospatialPointStyleOptions,
  "[Tooltip](#cfn-quicksight-template-geospatialmapconfiguration-tooltip)" : TooltipOptions,
  "[VisualPalette](#cfn-quicksight-template-geospatialmapconfiguration-visualpalette)" : VisualPalette,
  "[WindowOptions](#cfn-quicksight-template-geospatialmapconfiguration-windowoptions)" : GeospatialWindowOptions
}
```

### YAML<a name="aws-properties-quicksight-template-geospatialmapconfiguration-syntax.yaml"></a>

```
  [FieldWells](#cfn-quicksight-template-geospatialmapconfiguration-fieldwells): 
    GeospatialMapFieldWells
  [Legend](#cfn-quicksight-template-geospatialmapconfiguration-legend): 
    LegendOptions
  [MapStyleOptions](#cfn-quicksight-template-geospatialmapconfiguration-mapstyleoptions): 
    GeospatialMapStyleOptions
  [PointStyleOptions](#cfn-quicksight-template-geospatialmapconfiguration-pointstyleoptions): 
    GeospatialPointStyleOptions
  [Tooltip](#cfn-quicksight-template-geospatialmapconfiguration-tooltip): 
    TooltipOptions
  [VisualPalette](#cfn-quicksight-template-geospatialmapconfiguration-visualpalette): 
    VisualPalette
  [WindowOptions](#cfn-quicksight-template-geospatialmapconfiguration-windowoptions): 
    GeospatialWindowOptions
```

## Properties<a name="aws-properties-quicksight-template-geospatialmapconfiguration-properties"></a>

`FieldWells`  <a name="cfn-quicksight-template-geospatialmapconfiguration-fieldwells"></a>
The field wells of the visual\.  
*Required*: No  
*Type*: [GeospatialMapFieldWells](aws-properties-quicksight-template-geospatialmapfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Legend`  <a name="cfn-quicksight-template-geospatialmapconfiguration-legend"></a>
The legend display setup of the visual\.  
*Required*: No  
*Type*: [LegendOptions](aws-properties-quicksight-template-legendoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapStyleOptions`  <a name="cfn-quicksight-template-geospatialmapconfiguration-mapstyleoptions"></a>
The map style options of the geospatial map\.  
*Required*: No  
*Type*: [GeospatialMapStyleOptions](aws-properties-quicksight-template-geospatialmapstyleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PointStyleOptions`  <a name="cfn-quicksight-template-geospatialmapconfiguration-pointstyleoptions"></a>
The point style options of the geospatial map\.  
*Required*: No  
*Type*: [GeospatialPointStyleOptions](aws-properties-quicksight-template-geospatialpointstyleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tooltip`  <a name="cfn-quicksight-template-geospatialmapconfiguration-tooltip"></a>
The tooltip display setup of the visual\.  
*Required*: No  
*Type*: [TooltipOptions](aws-properties-quicksight-template-tooltipoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualPalette`  <a name="cfn-quicksight-template-geospatialmapconfiguration-visualpalette"></a>
Property description not available\.  
*Required*: No  
*Type*: [VisualPalette](aws-properties-quicksight-template-visualpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowOptions`  <a name="cfn-quicksight-template-geospatialmapconfiguration-windowoptions"></a>
The window options of the geospatial map\.  
*Required*: No  
*Type*: [GeospatialWindowOptions](aws-properties-quicksight-template-geospatialwindowoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)