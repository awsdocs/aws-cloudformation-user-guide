# AWS::IoTThingsGraph::FlowTemplate DefinitionDocument<a name="aws-properties-iotthingsgraph-flowtemplate-definitiondocument"></a>

A document that defines an entity\. 

## Syntax<a name="aws-properties-iotthingsgraph-flowtemplate-definitiondocument-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotthingsgraph-flowtemplate-definitiondocument-syntax.json"></a>

```
{
  "[Language](#cfn-iotthingsgraph-flowtemplate-definitiondocument-language)" : String,
  "[Text](#cfn-iotthingsgraph-flowtemplate-definitiondocument-text)" : String
}
```

### YAML<a name="aws-properties-iotthingsgraph-flowtemplate-definitiondocument-syntax.yaml"></a>

```
  [Language](#cfn-iotthingsgraph-flowtemplate-definitiondocument-language): String
  [Text](#cfn-iotthingsgraph-flowtemplate-definitiondocument-text): String
```

## Properties<a name="aws-properties-iotthingsgraph-flowtemplate-definitiondocument-properties"></a>

`Language`  <a name="cfn-iotthingsgraph-flowtemplate-definitiondocument-language"></a>
The language used to define the entity\. `GRAPHQL` is the only valid value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Text`  <a name="cfn-iotthingsgraph-flowtemplate-definitiondocument-text"></a>
The GraphQL text that defines the entity\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)