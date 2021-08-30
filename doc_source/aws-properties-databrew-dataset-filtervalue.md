# AWS::DataBrew::Dataset FilterValue<a name="aws-properties-databrew-dataset-filtervalue"></a>

Represents a single entry in the `ValuesMap` of a `FilterExpression`\. A `FilterValue` associates the name of a substitution variable in an expression to its value\.

## Syntax<a name="aws-properties-databrew-dataset-filtervalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-filtervalue-syntax.json"></a>

```
{
  "[Value](#cfn-databrew-dataset-filtervalue-value)" : String,
  "[ValueReference](#cfn-databrew-dataset-filtervalue-valuereference)" : String
}
```

### YAML<a name="aws-properties-databrew-dataset-filtervalue-syntax.yaml"></a>

```
  [Value](#cfn-databrew-dataset-filtervalue-value): String
  [ValueReference](#cfn-databrew-dataset-filtervalue-valuereference): String
```

## Properties<a name="aws-properties-databrew-dataset-filtervalue-properties"></a>

`Value`  <a name="cfn-databrew-dataset-filtervalue-value"></a>
The value to be associated with the substitution variable\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueReference`  <a name="cfn-databrew-dataset-filtervalue-valuereference"></a>
The substitution variable reference\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)