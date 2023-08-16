# AWS::QuickSight::Analysis PivotTableFieldCollapseStateOption<a name="aws-properties-quicksight-analysis-pivottablefieldcollapsestateoption"></a>

The collapse state options for the pivot table field options\.

## Syntax<a name="aws-properties-quicksight-analysis-pivottablefieldcollapsestateoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-pivottablefieldcollapsestateoption-syntax.json"></a>

```
{
  "[State](#cfn-quicksight-analysis-pivottablefieldcollapsestateoption-state)" : String,
  "[Target](#cfn-quicksight-analysis-pivottablefieldcollapsestateoption-target)" : PivotTableFieldCollapseStateTarget
}
```

### YAML<a name="aws-properties-quicksight-analysis-pivottablefieldcollapsestateoption-syntax.yaml"></a>

```
  [State](#cfn-quicksight-analysis-pivottablefieldcollapsestateoption-state): String
  [Target](#cfn-quicksight-analysis-pivottablefieldcollapsestateoption-target): 
    PivotTableFieldCollapseStateTarget
```

## Properties<a name="aws-properties-quicksight-analysis-pivottablefieldcollapsestateoption-properties"></a>

`State`  <a name="cfn-quicksight-analysis-pivottablefieldcollapsestateoption-state"></a>
The state of the field target of a pivot table\. Choose one of the following options:  
+  `COLLAPSED` 
+  `EXPANDED` 
*Required*: No  
*Type*: String  
*Allowed values*: `COLLAPSED | EXPANDED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-quicksight-analysis-pivottablefieldcollapsestateoption-target"></a>
A tagged\-union object that sets the collapse state\.  
*Required*: Yes  
*Type*: [PivotTableFieldCollapseStateTarget](aws-properties-quicksight-analysis-pivottablefieldcollapsestatetarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)