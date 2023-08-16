# AWS::Glue::Partition Column<a name="aws-properties-glue-partition-column"></a>

A column in a `Table`\.

## Syntax<a name="aws-properties-glue-partition-column-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-column-syntax.json"></a>

```
{
  "[Comment](#cfn-glue-partition-column-comment)" : String,
  "[Name](#cfn-glue-partition-column-name)" : String,
  "[Type](#cfn-glue-partition-column-type)" : String
}
```

### YAML<a name="aws-properties-glue-partition-column-syntax.yaml"></a>

```
  [Comment](#cfn-glue-partition-column-comment): String
  [Name](#cfn-glue-partition-column-name): String
  [Type](#cfn-glue-partition-column-type): String
```

## Properties<a name="aws-properties-glue-partition-column-properties"></a>

`Comment`  <a name="cfn-glue-partition-column-comment"></a>
A free\-form text comment\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-partition-column-name"></a>
The name of the `Column`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-glue-partition-column-type"></a>
The data type of the `Column`\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `131072`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)