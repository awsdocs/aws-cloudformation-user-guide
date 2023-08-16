# AWS::QuickSight::Template GridLayoutElement<a name="aws-properties-quicksight-template-gridlayoutelement"></a>

An element within a grid layout\.

## Syntax<a name="aws-properties-quicksight-template-gridlayoutelement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-gridlayoutelement-syntax.json"></a>

```
{
  "[ColumnIndex](#cfn-quicksight-template-gridlayoutelement-columnindex)" : Double,
  "[ColumnSpan](#cfn-quicksight-template-gridlayoutelement-columnspan)" : Double,
  "[ElementId](#cfn-quicksight-template-gridlayoutelement-elementid)" : String,
  "[ElementType](#cfn-quicksight-template-gridlayoutelement-elementtype)" : String,
  "[RowIndex](#cfn-quicksight-template-gridlayoutelement-rowindex)" : Double,
  "[RowSpan](#cfn-quicksight-template-gridlayoutelement-rowspan)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-gridlayoutelement-syntax.yaml"></a>

```
  [ColumnIndex](#cfn-quicksight-template-gridlayoutelement-columnindex): Double
  [ColumnSpan](#cfn-quicksight-template-gridlayoutelement-columnspan): Double
  [ElementId](#cfn-quicksight-template-gridlayoutelement-elementid): String
  [ElementType](#cfn-quicksight-template-gridlayoutelement-elementtype): String
  [RowIndex](#cfn-quicksight-template-gridlayoutelement-rowindex): Double
  [RowSpan](#cfn-quicksight-template-gridlayoutelement-rowspan): Double
```

## Properties<a name="aws-properties-quicksight-template-gridlayoutelement-properties"></a>

`ColumnIndex`  <a name="cfn-quicksight-template-gridlayoutelement-columnindex"></a>
The column index for the upper left corner of an element\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `35`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnSpan`  <a name="cfn-quicksight-template-gridlayoutelement-columnspan"></a>
The width of a grid element expressed as a number of grid columns\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `36`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElementId`  <a name="cfn-quicksight-template-gridlayoutelement-elementid"></a>
A unique identifier for an element within a grid layout\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElementType`  <a name="cfn-quicksight-template-gridlayoutelement-elementtype"></a>
The type of element\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FILTER_CONTROL | PARAMETER_CONTROL | TEXT_BOX | VISUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowIndex`  <a name="cfn-quicksight-template-gridlayoutelement-rowindex"></a>
The row index for the upper left corner of an element\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `9009`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowSpan`  <a name="cfn-quicksight-template-gridlayoutelement-rowspan"></a>
The height of a grid element expressed as a number of grid rows\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `21`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)