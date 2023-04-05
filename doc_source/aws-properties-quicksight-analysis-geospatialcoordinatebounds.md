# AWS::QuickSight::Analysis GeospatialCoordinateBounds<a name="aws-properties-quicksight-analysis-geospatialcoordinatebounds"></a>

The bound options \(north, south, west, east\) of the geospatial window options\.

## Syntax<a name="aws-properties-quicksight-analysis-geospatialcoordinatebounds-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-geospatialcoordinatebounds-syntax.json"></a>

```
{
  "[East](#cfn-quicksight-analysis-geospatialcoordinatebounds-east)" : Double,
  "[North](#cfn-quicksight-analysis-geospatialcoordinatebounds-north)" : Double,
  "[South](#cfn-quicksight-analysis-geospatialcoordinatebounds-south)" : Double,
  "[West](#cfn-quicksight-analysis-geospatialcoordinatebounds-west)" : Double
}
```

### YAML<a name="aws-properties-quicksight-analysis-geospatialcoordinatebounds-syntax.yaml"></a>

```
  [East](#cfn-quicksight-analysis-geospatialcoordinatebounds-east): Double
  [North](#cfn-quicksight-analysis-geospatialcoordinatebounds-north): Double
  [South](#cfn-quicksight-analysis-geospatialcoordinatebounds-south): Double
  [West](#cfn-quicksight-analysis-geospatialcoordinatebounds-west): Double
```

## Properties<a name="aws-properties-quicksight-analysis-geospatialcoordinatebounds-properties"></a>

`East`  <a name="cfn-quicksight-analysis-geospatialcoordinatebounds-east"></a>
The longitude of the east bound of the geospatial coordinate bounds\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`North`  <a name="cfn-quicksight-analysis-geospatialcoordinatebounds-north"></a>
The latitude of the north bound of the geospatial coordinate bounds\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`South`  <a name="cfn-quicksight-analysis-geospatialcoordinatebounds-south"></a>
The latitude of the south bound of the geospatial coordinate bounds\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`West`  <a name="cfn-quicksight-analysis-geospatialcoordinatebounds-west"></a>
The longitude of the west bound of the geospatial coordinate bounds\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)