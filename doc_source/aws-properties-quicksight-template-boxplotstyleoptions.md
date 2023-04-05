# AWS::QuickSight::Template BoxPlotStyleOptions<a name="aws-properties-quicksight-template-boxplotstyleoptions"></a>

The style options of the box plot\.

## Syntax<a name="aws-properties-quicksight-template-boxplotstyleoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-boxplotstyleoptions-syntax.json"></a>

```
{
  "[FillStyle](#cfn-quicksight-template-boxplotstyleoptions-fillstyle)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-boxplotstyleoptions-syntax.yaml"></a>

```
  [FillStyle](#cfn-quicksight-template-boxplotstyleoptions-fillstyle): String
```

## Properties<a name="aws-properties-quicksight-template-boxplotstyleoptions-properties"></a>

`FillStyle`  <a name="cfn-quicksight-template-boxplotstyleoptions-fillstyle"></a>
The fill styles \(solid, transparent\) of the box plot\.  
*Required*: No  
*Type*: String  
*Allowed values*: `SOLID | TRANSPARENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)