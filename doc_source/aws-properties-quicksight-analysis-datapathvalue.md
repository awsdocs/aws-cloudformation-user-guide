# AWS::QuickSight::Analysis DataPathValue<a name="aws-properties-quicksight-analysis-datapathvalue"></a>

The data path that needs to be sorted\.

## Syntax<a name="aws-properties-quicksight-analysis-datapathvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datapathvalue-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-analysis-datapathvalue-fieldid)" : String,
  "[FieldValue](#cfn-quicksight-analysis-datapathvalue-fieldvalue)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-datapathvalue-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-analysis-datapathvalue-fieldid): String
  [FieldValue](#cfn-quicksight-analysis-datapathvalue-fieldvalue): String
```

## Properties<a name="aws-properties-quicksight-analysis-datapathvalue-properties"></a>

`FieldId`  <a name="cfn-quicksight-analysis-datapathvalue-fieldid"></a>
The field ID of the field that needs to be sorted\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldValue`  <a name="cfn-quicksight-analysis-datapathvalue-fieldvalue"></a>
The actual value of the field that needs to be sorted\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)