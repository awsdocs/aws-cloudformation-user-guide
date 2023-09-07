# AWS::EntityResolution::MatchingWorkflow InputSource<a name="aws-properties-entityresolution-matchingworkflow-inputsource"></a>

An object containing `InputSourceARN`, `SchemaName`, and `ApplyNormalization`\.

## Syntax<a name="aws-properties-entityresolution-matchingworkflow-inputsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-entityresolution-matchingworkflow-inputsource-syntax.json"></a>

```
{
  "[ApplyNormalization](#cfn-entityresolution-matchingworkflow-inputsource-applynormalization)" : Boolean,
  "[InputSourceARN](#cfn-entityresolution-matchingworkflow-inputsource-inputsourcearn)" : String,
  "[SchemaArn](#cfn-entityresolution-matchingworkflow-inputsource-schemaarn)" : String
}
```

### YAML<a name="aws-properties-entityresolution-matchingworkflow-inputsource-syntax.yaml"></a>

```
  [ApplyNormalization](#cfn-entityresolution-matchingworkflow-inputsource-applynormalization): Boolean
  [InputSourceARN](#cfn-entityresolution-matchingworkflow-inputsource-inputsourcearn): String
  [SchemaArn](#cfn-entityresolution-matchingworkflow-inputsource-schemaarn): String
```

## Properties<a name="aws-properties-entityresolution-matchingworkflow-inputsource-properties"></a>

`ApplyNormalization`  <a name="cfn-entityresolution-matchingworkflow-inputsource-applynormalization"></a>
Normalizes the attributes defined in the schema in the input data\. For example, if an attribute has an `AttributeType` of `PHONE_NUMBER`, and the data in the input table is in a format of 1234567890, AWS Entity Resolution will normalize this field in the output to \(123\)\-456\-7890\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputSourceARN`  <a name="cfn-entityresolution-matchingworkflow-inputsource-inputsourcearn"></a>
An object containing `InputSourceARN`, `SchemaName`, and `ApplyNormalization`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaArn`  <a name="cfn-entityresolution-matchingworkflow-inputsource-schemaarn"></a>
The name of the schema\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)