# AWS::Forecast::Dataset Schema<a name="aws-properties-forecast-dataset-schema"></a>

Defines the fields of a dataset\.

## Syntax<a name="aws-properties-forecast-dataset-schema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-forecast-dataset-schema-syntax.json"></a>

```
{
  "[Attributes](#cfn-forecast-dataset-schema-attributes)" : [ AttributesItems, ... ]
}
```

### YAML<a name="aws-properties-forecast-dataset-schema-syntax.yaml"></a>

```
  [Attributes](#cfn-forecast-dataset-schema-attributes): 
    - AttributesItems
```

## Properties<a name="aws-properties-forecast-dataset-schema-properties"></a>

`Attributes`  <a name="cfn-forecast-dataset-schema-attributes"></a>
An array of attributes specifying the name and type of each field in a dataset\.  
*Required*: No  
*Type*: List of [AttributesItems](aws-properties-forecast-dataset-attributesitems.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)