# AWS::IoTTwinMaker::ComponentType DataType<a name="aws-properties-iottwinmaker-componenttype-datatype"></a>

An object that specifies the data type of a property\.

## Syntax<a name="aws-properties-iottwinmaker-componenttype-datatype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-componenttype-datatype-syntax.json"></a>

```
{
  "[AllowedValues](#cfn-iottwinmaker-componenttype-datatype-allowedvalues)" : [ DataValue, ... ],
  "[NestedType](#cfn-iottwinmaker-componenttype-datatype-nestedtype)" : DataType,
  "[Relationship](#cfn-iottwinmaker-componenttype-datatype-relationship)" : Relationship,
  "[Type](#cfn-iottwinmaker-componenttype-datatype-type)" : String,
  "[UnitOfMeasure](#cfn-iottwinmaker-componenttype-datatype-unitofmeasure)" : String
}
```

### YAML<a name="aws-properties-iottwinmaker-componenttype-datatype-syntax.yaml"></a>

```
  [AllowedValues](#cfn-iottwinmaker-componenttype-datatype-allowedvalues): 
    - DataValue
  [NestedType](#cfn-iottwinmaker-componenttype-datatype-nestedtype): 
    DataType
  [Relationship](#cfn-iottwinmaker-componenttype-datatype-relationship): 
    Relationship
  [Type](#cfn-iottwinmaker-componenttype-datatype-type): String
  [UnitOfMeasure](#cfn-iottwinmaker-componenttype-datatype-unitofmeasure): String
```

## Properties<a name="aws-properties-iottwinmaker-componenttype-datatype-properties"></a>

`AllowedValues`  <a name="cfn-iottwinmaker-componenttype-datatype-allowedvalues"></a>
The allowed values for this data type\.  
*Required*: No  
*Type*: List of [DataValue](aws-properties-iottwinmaker-componenttype-datavalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NestedType`  <a name="cfn-iottwinmaker-componenttype-datatype-nestedtype"></a>
The nested type in the data type\.  
*Required*: No  
*Type*: [DataType](#aws-properties-iottwinmaker-componenttype-datatype)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Relationship`  <a name="cfn-iottwinmaker-componenttype-datatype-relationship"></a>
A relationship that associates a component with another component\.  
*Required*: No  
*Type*: [Relationship](aws-properties-iottwinmaker-componenttype-relationship.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iottwinmaker-componenttype-datatype-type"></a>
The underlying type of the data type\.  
Valid Values: `RELATIONSHIP | STRING | LONG | BOOLEAN | INTEGER | DOUBLE | LIST | MAP`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnitOfMeasure`  <a name="cfn-iottwinmaker-componenttype-datatype-unitofmeasure"></a>
The unit of measure used in this data type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)