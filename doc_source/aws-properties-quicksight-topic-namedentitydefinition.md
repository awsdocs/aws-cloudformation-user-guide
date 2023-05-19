# AWS::QuickSight::Topic NamedEntityDefinition<a name="aws-properties-quicksight-topic-namedentitydefinition"></a>

A structure that represents a named entity\.

## Syntax<a name="aws-properties-quicksight-topic-namedentitydefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-namedentitydefinition-syntax.json"></a>

```
{
  "[FieldName](#cfn-quicksight-topic-namedentitydefinition-fieldname)" : String,
  "[Metric](#cfn-quicksight-topic-namedentitydefinition-metric)" : NamedEntityDefinitionMetric,
  "[PropertyName](#cfn-quicksight-topic-namedentitydefinition-propertyname)" : String,
  "[PropertyRole](#cfn-quicksight-topic-namedentitydefinition-propertyrole)" : String,
  "[PropertyUsage](#cfn-quicksight-topic-namedentitydefinition-propertyusage)" : String
}
```

### YAML<a name="aws-properties-quicksight-topic-namedentitydefinition-syntax.yaml"></a>

```
  [FieldName](#cfn-quicksight-topic-namedentitydefinition-fieldname): String
  [Metric](#cfn-quicksight-topic-namedentitydefinition-metric): 
    NamedEntityDefinitionMetric
  [PropertyName](#cfn-quicksight-topic-namedentitydefinition-propertyname): String
  [PropertyRole](#cfn-quicksight-topic-namedentitydefinition-propertyrole): String
  [PropertyUsage](#cfn-quicksight-topic-namedentitydefinition-propertyusage): String
```

## Properties<a name="aws-properties-quicksight-topic-namedentitydefinition-properties"></a>

`FieldName`  <a name="cfn-quicksight-topic-namedentitydefinition-fieldname"></a>
The name of the entity\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metric`  <a name="cfn-quicksight-topic-namedentitydefinition-metric"></a>
The definition of a metric\.  
*Required*: No  
*Type*: [NamedEntityDefinitionMetric](aws-properties-quicksight-topic-namedentitydefinitionmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyName`  <a name="cfn-quicksight-topic-namedentitydefinition-propertyname"></a>
The property name to be used for the named entity\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyRole`  <a name="cfn-quicksight-topic-namedentitydefinition-propertyrole"></a>
The property role\. Valid values for this structure are `PRIMARY` and `ID`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ID | PRIMARY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyUsage`  <a name="cfn-quicksight-topic-namedentitydefinition-propertyusage"></a>
The property usage\. Valid values for this structure are `INHERIT`, `DIMENSION`, and `MEASURE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DIMENSION | INHERIT | MEASURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)