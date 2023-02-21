# AWS::IoTTwinMaker::ComponentType DataValue<a name="aws-properties-iottwinmaker-componenttype-datavalue"></a>

An object that specifies a value for a property\.

## Syntax<a name="aws-properties-iottwinmaker-componenttype-datavalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-componenttype-datavalue-syntax.json"></a>

```
{
  "[BooleanValue](#cfn-iottwinmaker-componenttype-datavalue-booleanvalue)" : Boolean,
  "[DoubleValue](#cfn-iottwinmaker-componenttype-datavalue-doublevalue)" : Double,
  "[Expression](#cfn-iottwinmaker-componenttype-datavalue-expression)" : String,
  "[IntegerValue](#cfn-iottwinmaker-componenttype-datavalue-integervalue)" : Integer,
  "[ListValue](#cfn-iottwinmaker-componenttype-datavalue-listvalue)" : [ DataValue, ... ],
  "[LongValue](#cfn-iottwinmaker-componenttype-datavalue-longvalue)" : Double,
  "[MapValue](#cfn-iottwinmaker-componenttype-datavalue-mapvalue)" : {Key : Value, ...},
  "[RelationshipValue](#cfn-iottwinmaker-componenttype-datavalue-relationshipvalue)" : RelationshipValue,
  "[StringValue](#cfn-iottwinmaker-componenttype-datavalue-stringvalue)" : String
}
```

### YAML<a name="aws-properties-iottwinmaker-componenttype-datavalue-syntax.yaml"></a>

```
  [BooleanValue](#cfn-iottwinmaker-componenttype-datavalue-booleanvalue): 
    Boolean
  [DoubleValue](#cfn-iottwinmaker-componenttype-datavalue-doublevalue): 
    Double
  [Expression](#cfn-iottwinmaker-componenttype-datavalue-expression): String
  [IntegerValue](#cfn-iottwinmaker-componenttype-datavalue-integervalue): 
    Integer
  [ListValue](#cfn-iottwinmaker-componenttype-datavalue-listvalue): 
    - DataValue
  [LongValue](#cfn-iottwinmaker-componenttype-datavalue-longvalue): Double
  [MapValue](#cfn-iottwinmaker-componenttype-datavalue-mapvalue): 
    Key : Value
  [RelationshipValue](#cfn-iottwinmaker-componenttype-datavalue-relationshipvalue): 
    RelationshipValue
  [StringValue](#cfn-iottwinmaker-componenttype-datavalue-stringvalue): 
    String
```

## Properties<a name="aws-properties-iottwinmaker-componenttype-datavalue-properties"></a>

`BooleanValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-booleanvalue"></a>
A boolean value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DoubleValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-doublevalue"></a>
A double value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-iottwinmaker-componenttype-datavalue-expression"></a>
An expression that produces the value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-integervalue"></a>
An integer value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ListValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-listvalue"></a>
A list of multiple values\.  
*Required*: No  
*Type*: List of [DataValue](#aws-properties-iottwinmaker-componenttype-datavalue)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LongValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-longvalue"></a>
A long value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-mapvalue"></a>
An object that maps strings to multiple `DataValue` objects\.  
*Required*: No  
*Type*: Map of [DataValue](#aws-properties-iottwinmaker-componenttype-datavalue)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelationshipValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-relationshipvalue"></a>
A value that relates a component to another component\.  
*Required*: No  
*Type*: [RelationshipValue](aws-properties-iottwinmaker-componenttype-relationshipvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValue`  <a name="cfn-iottwinmaker-componenttype-datavalue-stringvalue"></a>
A string value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)