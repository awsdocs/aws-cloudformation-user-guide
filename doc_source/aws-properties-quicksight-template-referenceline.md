# AWS::QuickSight::Template ReferenceLine<a name="aws-properties-quicksight-template-referenceline"></a>

The reference line visual display options\.

## Syntax<a name="aws-properties-quicksight-template-referenceline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-referenceline-syntax.json"></a>

```
{
  "[DataConfiguration](#cfn-quicksight-template-referenceline-dataconfiguration)" : ReferenceLineDataConfiguration,
  "[LabelConfiguration](#cfn-quicksight-template-referenceline-labelconfiguration)" : ReferenceLineLabelConfiguration,
  "[Status](#cfn-quicksight-template-referenceline-status)" : String,
  "[StyleConfiguration](#cfn-quicksight-template-referenceline-styleconfiguration)" : ReferenceLineStyleConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-referenceline-syntax.yaml"></a>

```
  [DataConfiguration](#cfn-quicksight-template-referenceline-dataconfiguration): 
    ReferenceLineDataConfiguration
  [LabelConfiguration](#cfn-quicksight-template-referenceline-labelconfiguration): 
    ReferenceLineLabelConfiguration
  [Status](#cfn-quicksight-template-referenceline-status): String
  [StyleConfiguration](#cfn-quicksight-template-referenceline-styleconfiguration): 
    ReferenceLineStyleConfiguration
```

## Properties<a name="aws-properties-quicksight-template-referenceline-properties"></a>

`DataConfiguration`  <a name="cfn-quicksight-template-referenceline-dataconfiguration"></a>
The data configuration of the reference line\.  
*Required*: Yes  
*Type*: [ReferenceLineDataConfiguration](aws-properties-quicksight-template-referencelinedataconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelConfiguration`  <a name="cfn-quicksight-template-referenceline-labelconfiguration"></a>
The label configuration of the reference line\.  
*Required*: No  
*Type*: [ReferenceLineLabelConfiguration](aws-properties-quicksight-template-referencelinelabelconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-quicksight-template-referenceline-status"></a>
The status of the reference line\. Choose one of the following options:  
+  `ENABLE` 
+  `DISABLE` 
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StyleConfiguration`  <a name="cfn-quicksight-template-referenceline-styleconfiguration"></a>
The style configuration of the reference line\.  
*Required*: No  
*Type*: [ReferenceLineStyleConfiguration](aws-properties-quicksight-template-referencelinestyleconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)