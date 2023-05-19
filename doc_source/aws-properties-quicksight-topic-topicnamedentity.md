# AWS::QuickSight::Topic TopicNamedEntity<a name="aws-properties-quicksight-topic-topicnamedentity"></a>

A structure that represents a named entity\.

## Syntax<a name="aws-properties-quicksight-topic-topicnamedentity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topicnamedentity-syntax.json"></a>

```
{
  "[Definition](#cfn-quicksight-topic-topicnamedentity-definition)" : [ NamedEntityDefinition, ... ],
  "[EntityDescription](#cfn-quicksight-topic-topicnamedentity-entitydescription)" : String,
  "[EntityName](#cfn-quicksight-topic-topicnamedentity-entityname)" : String,
  "[EntitySynonyms](#cfn-quicksight-topic-topicnamedentity-entitysynonyms)" : [ String, ... ],
  "[SemanticEntityType](#cfn-quicksight-topic-topicnamedentity-semanticentitytype)" : SemanticEntityType
}
```

### YAML<a name="aws-properties-quicksight-topic-topicnamedentity-syntax.yaml"></a>

```
  [Definition](#cfn-quicksight-topic-topicnamedentity-definition): 
    - NamedEntityDefinition
  [EntityDescription](#cfn-quicksight-topic-topicnamedentity-entitydescription): String
  [EntityName](#cfn-quicksight-topic-topicnamedentity-entityname): String
  [EntitySynonyms](#cfn-quicksight-topic-topicnamedentity-entitysynonyms): 
    - String
  [SemanticEntityType](#cfn-quicksight-topic-topicnamedentity-semanticentitytype): 
    SemanticEntityType
```

## Properties<a name="aws-properties-quicksight-topic-topicnamedentity-properties"></a>

`Definition`  <a name="cfn-quicksight-topic-topicnamedentity-definition"></a>
The definition of a named entity\.  
*Required*: No  
*Type*: List of [NamedEntityDefinition](aws-properties-quicksight-topic-namedentitydefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityDescription`  <a name="cfn-quicksight-topic-topicnamedentity-entitydescription"></a>
The description of the named entity\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityName`  <a name="cfn-quicksight-topic-topicnamedentity-entityname"></a>
The name of the named entity\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntitySynonyms`  <a name="cfn-quicksight-topic-topicnamedentity-entitysynonyms"></a>
The other names or aliases for the named entity\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SemanticEntityType`  <a name="cfn-quicksight-topic-topicnamedentity-semanticentitytype"></a>
The type of named entity that a topic represents\.  
*Required*: No  
*Type*: [SemanticEntityType](aws-properties-quicksight-topic-semanticentitytype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)