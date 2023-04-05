# AWS::QuickSight::Dashboard ItemsLimitConfiguration<a name="aws-properties-quicksight-dashboard-itemslimitconfiguration"></a>

The limit configuration of the visual display for an axis\.

## Syntax<a name="aws-properties-quicksight-dashboard-itemslimitconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-itemslimitconfiguration-syntax.json"></a>

```
{
  "[ItemsLimit](#cfn-quicksight-dashboard-itemslimitconfiguration-itemslimit)" : Double,
  "[OtherCategories](#cfn-quicksight-dashboard-itemslimitconfiguration-othercategories)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-itemslimitconfiguration-syntax.yaml"></a>

```
  [ItemsLimit](#cfn-quicksight-dashboard-itemslimitconfiguration-itemslimit): Double
  [OtherCategories](#cfn-quicksight-dashboard-itemslimitconfiguration-othercategories): String
```

## Properties<a name="aws-properties-quicksight-dashboard-itemslimitconfiguration-properties"></a>

`ItemsLimit`  <a name="cfn-quicksight-dashboard-itemslimitconfiguration-itemslimit"></a>
The limit on how many items of a field are showed in the chart\. For example, the number of slices that are displayed in a pie chart\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OtherCategories`  <a name="cfn-quicksight-dashboard-itemslimitconfiguration-othercategories"></a>
The `Show other` of an axis in the chart\. Choose one of the following options:  
+  `INCLUDE` 
+  `EXCLUDE` 
*Required*: No  
*Type*: String  
*Allowed values*: `EXCLUDE | INCLUDE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)