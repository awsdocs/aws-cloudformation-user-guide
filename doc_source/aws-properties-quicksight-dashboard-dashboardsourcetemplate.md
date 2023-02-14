# AWS::QuickSight::Dashboard DashboardSourceTemplate<a name="aws-properties-quicksight-dashboard-dashboardsourcetemplate"></a>

Dashboard source template\.

## Syntax<a name="aws-properties-quicksight-dashboard-dashboardsourcetemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-dashboardsourcetemplate-syntax.json"></a>

```
{
  "[Arn](#cfn-quicksight-dashboard-dashboardsourcetemplate-arn)" : String,
  "[DataSetReferences](#cfn-quicksight-dashboard-dashboardsourcetemplate-datasetreferences)" : [ DataSetReference, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-dashboardsourcetemplate-syntax.yaml"></a>

```
  [Arn](#cfn-quicksight-dashboard-dashboardsourcetemplate-arn): String
  [DataSetReferences](#cfn-quicksight-dashboard-dashboardsourcetemplate-datasetreferences): 
    - DataSetReference
```

## Properties<a name="aws-properties-quicksight-dashboard-dashboardsourcetemplate-properties"></a>

`Arn`  <a name="cfn-quicksight-dashboard-dashboardsourcetemplate-arn"></a>
The Amazon Resource Name \(ARN\) of the resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetReferences`  <a name="cfn-quicksight-dashboard-dashboardsourcetemplate-datasetreferences"></a>
Dataset references\.  
*Required*: Yes  
*Type*: List of [DataSetReference](aws-properties-quicksight-dashboard-datasetreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)