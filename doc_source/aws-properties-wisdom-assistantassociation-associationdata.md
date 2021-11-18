# AWS::Wisdom::AssistantAssociation AssociationData<a name="aws-properties-wisdom-assistantassociation-associationdata"></a>

A union type that currently has a single argument, which is the knowledge base ID\.

## Syntax<a name="aws-properties-wisdom-assistantassociation-associationdata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wisdom-assistantassociation-associationdata-syntax.json"></a>

```
{
  "[KnowledgeBaseId](#cfn-wisdom-assistantassociation-associationdata-knowledgebaseid)" : String
}
```

### YAML<a name="aws-properties-wisdom-assistantassociation-associationdata-syntax.yaml"></a>

```
  [KnowledgeBaseId](#cfn-wisdom-assistantassociation-associationdata-knowledgebaseid): String
```

## Properties<a name="aws-properties-wisdom-assistantassociation-associationdata-properties"></a>

`KnowledgeBaseId`  <a name="cfn-wisdom-assistantassociation-associationdata-knowledgebaseid"></a>
The identifier of the knowledge base\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)