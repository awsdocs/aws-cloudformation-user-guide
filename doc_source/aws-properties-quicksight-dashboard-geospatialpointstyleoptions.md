# AWS::QuickSight::Dashboard GeospatialPointStyleOptions<a name="aws-properties-quicksight-dashboard-geospatialpointstyleoptions"></a>

The point style of the geospatial map\.

## Syntax<a name="aws-properties-quicksight-dashboard-geospatialpointstyleoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-geospatialpointstyleoptions-syntax.json"></a>

```
{
  "[ClusterMarkerConfiguration](#cfn-quicksight-dashboard-geospatialpointstyleoptions-clustermarkerconfiguration)" : ClusterMarkerConfiguration,
  "[SelectedPointStyle](#cfn-quicksight-dashboard-geospatialpointstyleoptions-selectedpointstyle)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-geospatialpointstyleoptions-syntax.yaml"></a>

```
  [ClusterMarkerConfiguration](#cfn-quicksight-dashboard-geospatialpointstyleoptions-clustermarkerconfiguration): 
    ClusterMarkerConfiguration
  [SelectedPointStyle](#cfn-quicksight-dashboard-geospatialpointstyleoptions-selectedpointstyle): String
```

## Properties<a name="aws-properties-quicksight-dashboard-geospatialpointstyleoptions-properties"></a>

`ClusterMarkerConfiguration`  <a name="cfn-quicksight-dashboard-geospatialpointstyleoptions-clustermarkerconfiguration"></a>
The cluster marker configuration of the geospatial point style\.  
*Required*: No  
*Type*: [ClusterMarkerConfiguration](aws-properties-quicksight-dashboard-clustermarkerconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedPointStyle`  <a name="cfn-quicksight-dashboard-geospatialpointstyleoptions-selectedpointstyle"></a>
The selected point styles \(point, cluster\) of the geospatial map\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CLUSTER | HEATMAP | POINT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)