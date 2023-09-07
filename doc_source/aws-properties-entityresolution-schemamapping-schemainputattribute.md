# AWS::EntityResolution::SchemaMapping SchemaInputAttribute<a name="aws-properties-entityresolution-schemamapping-schemainputattribute"></a>

An object containing `FieldField`, `Type`, `GroupName`, and `MatchKey`\.

## Syntax<a name="aws-properties-entityresolution-schemamapping-schemainputattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-entityresolution-schemamapping-schemainputattribute-syntax.json"></a>

```
{
  "[FieldName](#cfn-entityresolution-schemamapping-schemainputattribute-fieldname)" : String,
  "[GroupName](#cfn-entityresolution-schemamapping-schemainputattribute-groupname)" : String,
  "[MatchKey](#cfn-entityresolution-schemamapping-schemainputattribute-matchkey)" : String,
  "[Type](#cfn-entityresolution-schemamapping-schemainputattribute-type)" : String
}
```

### YAML<a name="aws-properties-entityresolution-schemamapping-schemainputattribute-syntax.yaml"></a>

```
  [FieldName](#cfn-entityresolution-schemamapping-schemainputattribute-fieldname): String
  [GroupName](#cfn-entityresolution-schemamapping-schemainputattribute-groupname): String
  [MatchKey](#cfn-entityresolution-schemamapping-schemainputattribute-matchkey): String
  [Type](#cfn-entityresolution-schemamapping-schemainputattribute-type): String
```

## Properties<a name="aws-properties-entityresolution-schemamapping-schemainputattribute-properties"></a>

`FieldName`  <a name="cfn-entityresolution-schemamapping-schemainputattribute-fieldname"></a>
A string containing the field name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroupName`  <a name="cfn-entityresolution-schemamapping-schemainputattribute-groupname"></a>
Instruct AWS Entity Resolution to combine several columns into a unified column with the identical attribute type\. For example, when working with columns such as first\_name, middle\_name, and last\_name, assigning them a common `GroupName` will prompt AWS Entity Resolution to concatenate them into a single value\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MatchKey`  <a name="cfn-entityresolution-schemamapping-schemainputattribute-matchkey"></a>
A key that allows grouping of multiple input attributes into a unified matching group\. For example, let's consider a scenario where the source table contains various addresses, such as business\_address and shipping\_address\. By assigning the `MatchKey` *Address* to both attributes, AWS Entity Resolution will match records across these fields to create a consolidated matching group\. If no `MatchKey` is specified for a column, it won't be utilized for matching purposes but will still be included in the output table\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-entityresolution-schemamapping-schemainputattribute-type"></a>
The type of the attribute, selected from a list of values\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)