# AWS::EntityResolution::MatchingWorkflow OutputAttribute<a name="aws-properties-entityresolution-matchingworkflow-outputattribute"></a>

A list of `OutputAttribute` objects, each of which have the fields `Name` and `Hashed`\. Each of these objects selects a column to be included in the output table, and whether the values of the column should be hashed\.

## Syntax<a name="aws-properties-entityresolution-matchingworkflow-outputattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-entityresolution-matchingworkflow-outputattribute-syntax.json"></a>

```
{
  "[Hashed](#cfn-entityresolution-matchingworkflow-outputattribute-hashed)" : Boolean,
  "[Name](#cfn-entityresolution-matchingworkflow-outputattribute-name)" : String
}
```

### YAML<a name="aws-properties-entityresolution-matchingworkflow-outputattribute-syntax.yaml"></a>

```
  [Hashed](#cfn-entityresolution-matchingworkflow-outputattribute-hashed): Boolean
  [Name](#cfn-entityresolution-matchingworkflow-outputattribute-name): String
```

## Properties<a name="aws-properties-entityresolution-matchingworkflow-outputattribute-properties"></a>

`Hashed`  <a name="cfn-entityresolution-matchingworkflow-outputattribute-hashed"></a>
Enables the ability to hash the column values in the output\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-entityresolution-matchingworkflow-outputattribute-name"></a>
A name of a column to be written to the output\. This must be an `InputField` name in the schema mapping\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)