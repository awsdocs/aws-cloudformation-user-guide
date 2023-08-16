# AWS::QuickSight::Analysis Layout<a name="aws-properties-quicksight-analysis-layout"></a>

A `Layout` defines the placement of elements within a sheet\.

For more information, see [Types of layout](https://docs.aws.amazon.com/quicksight/latest/user/types-of-layout.html) in the *Amazon QuickSight User Guide*\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-layout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-layout-syntax.json"></a>

```
{
  "[Configuration](#cfn-quicksight-analysis-layout-configuration)" : LayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-layout-syntax.yaml"></a>

```
  [Configuration](#cfn-quicksight-analysis-layout-configuration): 
    LayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-layout-properties"></a>

`Configuration`  <a name="cfn-quicksight-analysis-layout-configuration"></a>
The configuration that determines what the type of layout for a sheet\.  
*Required*: Yes  
*Type*: [LayoutConfiguration](aws-properties-quicksight-analysis-layoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)