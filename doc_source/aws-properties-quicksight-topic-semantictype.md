# AWS::QuickSight::Topic SemanticType<a name="aws-properties-quicksight-topic-semantictype"></a>

A structure that represents a semantic type\.

## Syntax<a name="aws-properties-quicksight-topic-semantictype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-semantictype-syntax.json"></a>

```
{
  "[FalseyCellValue](#cfn-quicksight-topic-semantictype-falseycellvalue)" : String,
  "[FalseyCellValueSynonyms](#cfn-quicksight-topic-semantictype-falseycellvaluesynonyms)" : [ String, ... ],
  "[SubTypeName](#cfn-quicksight-topic-semantictype-subtypename)" : String,
  "[TruthyCellValue](#cfn-quicksight-topic-semantictype-truthycellvalue)" : String,
  "[TruthyCellValueSynonyms](#cfn-quicksight-topic-semantictype-truthycellvaluesynonyms)" : [ String, ... ],
  "[TypeName](#cfn-quicksight-topic-semantictype-typename)" : String,
  "[TypeParameters](#cfn-quicksight-topic-semantictype-typeparameters)" : {Key: Value, ...}
}
```

### YAML<a name="aws-properties-quicksight-topic-semantictype-syntax.yaml"></a>

```
  [FalseyCellValue](#cfn-quicksight-topic-semantictype-falseycellvalue): String
  [FalseyCellValueSynonyms](#cfn-quicksight-topic-semantictype-falseycellvaluesynonyms): 
    - String
  [SubTypeName](#cfn-quicksight-topic-semantictype-subtypename): String
  [TruthyCellValue](#cfn-quicksight-topic-semantictype-truthycellvalue): String
  [TruthyCellValueSynonyms](#cfn-quicksight-topic-semantictype-truthycellvaluesynonyms): 
    - String
  [TypeName](#cfn-quicksight-topic-semantictype-typename): String
  [TypeParameters](#cfn-quicksight-topic-semantictype-typeparameters): 
    Key: Value
```

## Properties<a name="aws-properties-quicksight-topic-semantictype-properties"></a>

`FalseyCellValue`  <a name="cfn-quicksight-topic-semantictype-falseycellvalue"></a>
The semantic type falsey cell value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FalseyCellValueSynonyms`  <a name="cfn-quicksight-topic-semantictype-falseycellvaluesynonyms"></a>
The other names or aliases for the false cell value\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubTypeName`  <a name="cfn-quicksight-topic-semantictype-subtypename"></a>
The semantic type sub type name\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TruthyCellValue`  <a name="cfn-quicksight-topic-semantictype-truthycellvalue"></a>
The semantic type truthy cell value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TruthyCellValueSynonyms`  <a name="cfn-quicksight-topic-semantictype-truthycellvaluesynonyms"></a>
The other names or aliases for the true cell value\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeName`  <a name="cfn-quicksight-topic-semantictype-typename"></a>
The semantic type name\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeParameters`  <a name="cfn-quicksight-topic-semantictype-typeparameters"></a>
The semantic type parameters\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)