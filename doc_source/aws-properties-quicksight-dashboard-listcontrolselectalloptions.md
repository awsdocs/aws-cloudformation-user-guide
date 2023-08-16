# AWS::QuickSight::Dashboard ListControlSelectAllOptions<a name="aws-properties-quicksight-dashboard-listcontrolselectalloptions"></a>

The configuration of the `Select all` options in a list control\.

## Syntax<a name="aws-properties-quicksight-dashboard-listcontrolselectalloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-listcontrolselectalloptions-syntax.json"></a>

```
{
  "[Visibility](#cfn-quicksight-dashboard-listcontrolselectalloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-listcontrolselectalloptions-syntax.yaml"></a>

```
  [Visibility](#cfn-quicksight-dashboard-listcontrolselectalloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-listcontrolselectalloptions-properties"></a>

`Visibility`  <a name="cfn-quicksight-dashboard-listcontrolselectalloptions-visibility"></a>
The visibility configuration of the `Select all` options in a list control\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)