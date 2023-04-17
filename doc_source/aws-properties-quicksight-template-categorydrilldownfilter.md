# AWS::QuickSight::Template CategoryDrillDownFilter<a name="aws-properties-quicksight-template-categorydrilldownfilter"></a>

The numeric equality type drill down filter\.

## Syntax<a name="aws-properties-quicksight-template-categorydrilldownfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-categorydrilldownfilter-syntax.json"></a>

```
{
  "[CategoryValues](#cfn-quicksight-template-categorydrilldownfilter-categoryvalues)" : [ String, ... ],
  "[Column](#cfn-quicksight-template-categorydrilldownfilter-column)" : ColumnIdentifier
}
```

### YAML<a name="aws-properties-quicksight-template-categorydrilldownfilter-syntax.yaml"></a>

```
  [CategoryValues](#cfn-quicksight-template-categorydrilldownfilter-categoryvalues): 
    - String
  [Column](#cfn-quicksight-template-categorydrilldownfilter-column): 
    ColumnIdentifier
```

## Properties<a name="aws-properties-quicksight-template-categorydrilldownfilter-properties"></a>

`CategoryValues`  <a name="cfn-quicksight-template-categorydrilldownfilter-categoryvalues"></a>
A list of the string inputs that are the values of the category drill down filter\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-template-categorydrilldownfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)