# AWS::QuickSight::Template PivotTableFieldCollapseStateTarget<a name="aws-properties-quicksight-template-pivottablefieldcollapsestatetarget"></a>

The target of a pivot table field collapse state\.

## Syntax<a name="aws-properties-quicksight-template-pivottablefieldcollapsestatetarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivottablefieldcollapsestatetarget-syntax.json"></a>

```
{
  "[FieldDataPathValues](#cfn-quicksight-template-pivottablefieldcollapsestatetarget-fielddatapathvalues)" : [ DataPathValue, ... ],
  "[FieldId](#cfn-quicksight-template-pivottablefieldcollapsestatetarget-fieldid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-pivottablefieldcollapsestatetarget-syntax.yaml"></a>

```
  [FieldDataPathValues](#cfn-quicksight-template-pivottablefieldcollapsestatetarget-fielddatapathvalues): 
    - DataPathValue
  [FieldId](#cfn-quicksight-template-pivottablefieldcollapsestatetarget-fieldid): String
```

## Properties<a name="aws-properties-quicksight-template-pivottablefieldcollapsestatetarget-properties"></a>

`FieldDataPathValues`  <a name="cfn-quicksight-template-pivottablefieldcollapsestatetarget-fielddatapathvalues"></a>
The data path of the pivot table's header\. Used to set the collapse state\.  
*Required*: No  
*Type*: List of [DataPathValue](aws-properties-quicksight-template-datapathvalue.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-template-pivottablefieldcollapsestatetarget-fieldid"></a>
The field ID of the pivot table that the collapse state needs to be set to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)