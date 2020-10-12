# AWS::Kendra::DataSource SalesforceKnowledgeArticleStateList<a name="aws-properties-kendra-datasource-salesforceknowledgearticlestatelist"></a>

Specifies document states that should be included when Amazon Kendra indexes knowledge articles\.

## Syntax<a name="aws-properties-kendra-datasource-salesforceknowledgearticlestatelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforceknowledgearticlestatelist-syntax.json"></a>

```
{
  "[SalesforceKnowledgeArticleStateList](#cfn-kendra-datasource-salesforceknowledgearticlestatelist-salesforceknowledgearticlestatelist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforceknowledgearticlestatelist-syntax.yaml"></a>

```
  [SalesforceKnowledgeArticleStateList](#cfn-kendra-datasource-salesforceknowledgearticlestatelist-salesforceknowledgearticlestatelist): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-salesforceknowledgearticlestatelist-properties"></a>

`SalesforceKnowledgeArticleStateList`  <a name="cfn-kendra-datasource-salesforceknowledgearticlestatelist-salesforceknowledgearticlestatelist"></a>
A list of document states that should be included when Amazon Kendra indexes knowledge articles\. You must specify at least one state\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-salesforceknowledgearticlestatelist) of [String](#aws-properties-kendra-datasource-salesforceknowledgearticlestatelist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)