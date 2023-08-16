# AWS::QuickSight::Template GeospatialPointStyleOptions<a name="aws-properties-quicksight-template-geospatialpointstyleoptions"></a>

The point style of the geospatial map\.

## Syntax<a name="aws-properties-quicksight-template-geospatialpointstyleoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-geospatialpointstyleoptions-syntax.json"></a>

```
{
  "[ClusterMarkerConfiguration](#cfn-quicksight-template-geospatialpointstyleoptions-clustermarkerconfiguration)" : ClusterMarkerConfiguration,
  "[HeatmapConfiguration](#cfn-quicksight-template-geospatialpointstyleoptions-heatmapconfiguration)" : GeospatialHeatmapConfiguration,
  "[SelectedPointStyle](#cfn-quicksight-template-geospatialpointstyleoptions-selectedpointstyle)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-geospatialpointstyleoptions-syntax.yaml"></a>

```
  [ClusterMarkerConfiguration](#cfn-quicksight-template-geospatialpointstyleoptions-clustermarkerconfiguration): 
    ClusterMarkerConfiguration
  [HeatmapConfiguration](#cfn-quicksight-template-geospatialpointstyleoptions-heatmapconfiguration): 
    GeospatialHeatmapConfiguration
  [SelectedPointStyle](#cfn-quicksight-template-geospatialpointstyleoptions-selectedpointstyle): String
```

## Properties<a name="aws-properties-quicksight-template-geospatialpointstyleoptions-properties"></a>

`ClusterMarkerConfiguration`  <a name="cfn-quicksight-template-geospatialpointstyleoptions-clustermarkerconfiguration"></a>
The cluster marker configuration of the geospatial point style\.  
*Required*: No  
*Type*: [ClusterMarkerConfiguration](aws-properties-quicksight-template-clustermarkerconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeatmapConfiguration`  <a name="cfn-quicksight-template-geospatialpointstyleoptions-heatmapconfiguration"></a>
The heatmap configuration of the geospatial point style\.  
*Required*: No  
*Type*: [GeospatialHeatmapConfiguration](aws-properties-quicksight-template-geospatialheatmapconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedPointStyle`  <a name="cfn-quicksight-template-geospatialpointstyleoptions-selectedpointstyle"></a>
The selected point styles \(point, cluster\) of the geospatial map\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CLUSTER | HEATMAP | POINT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)