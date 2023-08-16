# AWS::QuickSight::Dashboard DonutOptions<a name="aws-properties-quicksight-dashboard-donutoptions"></a>

The options for configuring a donut chart or pie chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-donutoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-donutoptions-syntax.json"></a>

```
{
  "[ArcOptions](#cfn-quicksight-dashboard-donutoptions-arcoptions)" : ArcOptions,
  "[DonutCenterOptions](#cfn-quicksight-dashboard-donutoptions-donutcenteroptions)" : DonutCenterOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-donutoptions-syntax.yaml"></a>

```
  [ArcOptions](#cfn-quicksight-dashboard-donutoptions-arcoptions): 
    ArcOptions
  [DonutCenterOptions](#cfn-quicksight-dashboard-donutoptions-donutcenteroptions): 
    DonutCenterOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-donutoptions-properties"></a>

`ArcOptions`  <a name="cfn-quicksight-dashboard-donutoptions-arcoptions"></a>
The option for define the arc of the chart shape\. Valid values are as follows:  
+  `WHOLE` \- A pie chart
+  `SMALL`\- A small\-sized donut chart
+  `MEDIUM`\- A medium\-sized donut chart
+  `LARGE`\- A large\-sized donut chart
*Required*: No  
*Type*: [ArcOptions](aws-properties-quicksight-dashboard-arcoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DonutCenterOptions`  <a name="cfn-quicksight-dashboard-donutoptions-donutcenteroptions"></a>
The label options of the label that is displayed in the center of a donut chart\. This option isn't available for pie charts\.  
*Required*: No  
*Type*: [DonutCenterOptions](aws-properties-quicksight-dashboard-donutcenteroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)