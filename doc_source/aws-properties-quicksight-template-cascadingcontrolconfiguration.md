# AWS::QuickSight::Template CascadingControlConfiguration<a name="aws-properties-quicksight-template-cascadingcontrolconfiguration"></a>

The values that are displayed in a control can be configured to only show values that are valid based on what's selected in other controls\.

## Syntax<a name="aws-properties-quicksight-template-cascadingcontrolconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-cascadingcontrolconfiguration-syntax.json"></a>

```
{
  "[SourceControls](#cfn-quicksight-template-cascadingcontrolconfiguration-sourcecontrols)" : [ CascadingControlSource, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-cascadingcontrolconfiguration-syntax.yaml"></a>

```
  [SourceControls](#cfn-quicksight-template-cascadingcontrolconfiguration-sourcecontrols): 
    - CascadingControlSource
```

## Properties<a name="aws-properties-quicksight-template-cascadingcontrolconfiguration-properties"></a>

`SourceControls`  <a name="cfn-quicksight-template-cascadingcontrolconfiguration-sourcecontrols"></a>
A list of source controls that determine the values that are used in the current control\.  
*Required*: No  
*Type*: List of [CascadingControlSource](aws-properties-quicksight-template-cascadingcontrolsource.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)