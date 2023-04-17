# AWS::QuickSight::Template SameSheetTargetVisualConfiguration<a name="aws-properties-quicksight-template-samesheettargetvisualconfiguration"></a>

The configuration of the same\-sheet target visuals that you want to be filtered\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-samesheettargetvisualconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-samesheettargetvisualconfiguration-syntax.json"></a>

```
{
  "[TargetVisualOptions](#cfn-quicksight-template-samesheettargetvisualconfiguration-targetvisualoptions)" : String,
  "[TargetVisuals](#cfn-quicksight-template-samesheettargetvisualconfiguration-targetvisuals)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-samesheettargetvisualconfiguration-syntax.yaml"></a>

```
  [TargetVisualOptions](#cfn-quicksight-template-samesheettargetvisualconfiguration-targetvisualoptions): String
  [TargetVisuals](#cfn-quicksight-template-samesheettargetvisualconfiguration-targetvisuals): 
    - String
```

## Properties<a name="aws-properties-quicksight-template-samesheettargetvisualconfiguration-properties"></a>

`TargetVisualOptions`  <a name="cfn-quicksight-template-samesheettargetvisualconfiguration-targetvisualoptions"></a>
The options that choose the target visual in the same sheet\.  
Valid values are defined as follows:  
+  `ALL_VISUALS`: Applies the filter operation to all visuals in the same sheet\.
*Required*: No  
*Type*: String  
*Allowed values*: `ALL_VISUALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetVisuals`  <a name="cfn-quicksight-template-samesheettargetvisualconfiguration-targetvisuals"></a>
A list of the target visual IDs that are located in the same sheet of the analysis\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)