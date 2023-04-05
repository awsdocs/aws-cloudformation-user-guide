# AWS::QuickSight::Template Layout<a name="aws-properties-quicksight-template-layout"></a>

A `Layout` defines the placement of elements within a sheet\.

For more information, see [Types of layout](https://docs.aws.amazon.com/quicksight/latest/user/types-of-layout.html) in the *Amazon QuickSight User Guide*\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-layout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-layout-syntax.json"></a>

```
{
  "[Configuration](#cfn-quicksight-template-layout-configuration)" : LayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-layout-syntax.yaml"></a>

```
  [Configuration](#cfn-quicksight-template-layout-configuration): 
    LayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-template-layout-properties"></a>

`Configuration`  <a name="cfn-quicksight-template-layout-configuration"></a>
The configuration that determines what the type of layout for a sheet\.  
*Required*: Yes  
*Type*: [LayoutConfiguration](aws-properties-quicksight-template-layoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)