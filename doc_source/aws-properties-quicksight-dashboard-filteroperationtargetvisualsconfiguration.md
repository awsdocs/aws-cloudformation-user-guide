# AWS::QuickSight::Dashboard FilterOperationTargetVisualsConfiguration<a name="aws-properties-quicksight-dashboard-filteroperationtargetvisualsconfiguration"></a>

The configuration of target visuals that you want to be filtered\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-filteroperationtargetvisualsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filteroperationtargetvisualsconfiguration-syntax.json"></a>

```
{
  "[SameSheetTargetVisualConfiguration](#cfn-quicksight-dashboard-filteroperationtargetvisualsconfiguration-samesheettargetvisualconfiguration)" : SameSheetTargetVisualConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filteroperationtargetvisualsconfiguration-syntax.yaml"></a>

```
  [SameSheetTargetVisualConfiguration](#cfn-quicksight-dashboard-filteroperationtargetvisualsconfiguration-samesheettargetvisualconfiguration): 
    SameSheetTargetVisualConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-filteroperationtargetvisualsconfiguration-properties"></a>

`SameSheetTargetVisualConfiguration`  <a name="cfn-quicksight-dashboard-filteroperationtargetvisualsconfiguration-samesheettargetvisualconfiguration"></a>
The configuration of the same\-sheet target visuals that you want to be filtered\.  
*Required*: No  
*Type*: [SameSheetTargetVisualConfiguration](aws-properties-quicksight-dashboard-samesheettargetvisualconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)