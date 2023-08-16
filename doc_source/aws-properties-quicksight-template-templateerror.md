# AWS::QuickSight::Template TemplateError<a name="aws-properties-quicksight-template-templateerror"></a>

List of errors that occurred when the template version creation failed\.

## Syntax<a name="aws-properties-quicksight-template-templateerror-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-templateerror-syntax.json"></a>

```
{
  "[Message](#cfn-quicksight-template-templateerror-message)" : String,
  "[Type](#cfn-quicksight-template-templateerror-type)" : String,
  "[ViolatedEntities](#cfn-quicksight-template-templateerror-violatedentities)" : [ Entity, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-templateerror-syntax.yaml"></a>

```
  [Message](#cfn-quicksight-template-templateerror-message): String
  [Type](#cfn-quicksight-template-templateerror-type): String
  [ViolatedEntities](#cfn-quicksight-template-templateerror-violatedentities): 
    - Entity
```

## Properties<a name="aws-properties-quicksight-template-templateerror-properties"></a>

`Message`  <a name="cfn-quicksight-template-templateerror-message"></a>
Description of the error type\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-template-templateerror-type"></a>
Type of error\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACCESS_DENIED | DATA_SET_NOT_FOUND | INTERNAL_FAILURE | SOURCE_NOT_FOUND`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ViolatedEntities`  <a name="cfn-quicksight-template-templateerror-violatedentities"></a>
An error path that shows which entities caused the template error\.  
*Required*: No  
*Type*: List of [Entity](aws-properties-quicksight-template-entity.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)