# AWS::Kendra::DataSource SalesforceKnowledgeArticleConfiguration<a name="aws-properties-kendra-datasource-salesforceknowledgearticleconfiguration"></a>

Specifies configuration information for the knowlege article types that Amazon Kendra indexes\. Amazon Kendra indexes standard knowledge articles and the standard fields of knowledge articles, or the custom fields of custom knowledge articles, but not both 

## Syntax<a name="aws-properties-kendra-datasource-salesforceknowledgearticleconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforceknowledgearticleconfiguration-syntax.json"></a>

```
{
  "[CustomKnowledgeArticleTypeConfigurations](#cfn-kendra-datasource-salesforceknowledgearticleconfiguration-customknowledgearticletypeconfigurations)" : SalesforceCustomKnowledgeArticleTypeConfigurationList,
  "[IncludedStates](#cfn-kendra-datasource-salesforceknowledgearticleconfiguration-includedstates)" : SalesforceKnowledgeArticleStateList,
  "[StandardKnowledgeArticleTypeConfiguration](#cfn-kendra-datasource-salesforceknowledgearticleconfiguration-standardknowledgearticletypeconfiguration)" : SalesforceStandardKnowledgeArticleTypeConfiguration
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforceknowledgearticleconfiguration-syntax.yaml"></a>

```
  [CustomKnowledgeArticleTypeConfigurations](#cfn-kendra-datasource-salesforceknowledgearticleconfiguration-customknowledgearticletypeconfigurations): 
    SalesforceCustomKnowledgeArticleTypeConfigurationList
  [IncludedStates](#cfn-kendra-datasource-salesforceknowledgearticleconfiguration-includedstates): 
    SalesforceKnowledgeArticleStateList
  [StandardKnowledgeArticleTypeConfiguration](#cfn-kendra-datasource-salesforceknowledgearticleconfiguration-standardknowledgearticletypeconfiguration): 
    SalesforceStandardKnowledgeArticleTypeConfiguration
```

## Properties<a name="aws-properties-kendra-datasource-salesforceknowledgearticleconfiguration-properties"></a>

`CustomKnowledgeArticleTypeConfigurations`  <a name="cfn-kendra-datasource-salesforceknowledgearticleconfiguration-customknowledgearticletypeconfigurations"></a>
Provides configuration information for custom Salesforce knowledge articles\.  
*Required*: No  
*Type*: [SalesforceCustomKnowledgeArticleTypeConfigurationList](aws-properties-kendra-datasource-salesforcecustomknowledgearticletypeconfigurationlist.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludedStates`  <a name="cfn-kendra-datasource-salesforceknowledgearticleconfiguration-includedstates"></a>
Specifies the document states that should be included when Amazon Kendra indexes knowledge articles\. You must specify at least one state\.  
*Required*: Yes  
*Type*: [SalesforceKnowledgeArticleStateList](aws-properties-kendra-datasource-salesforceknowledgearticlestatelist.md)  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StandardKnowledgeArticleTypeConfiguration`  <a name="cfn-kendra-datasource-salesforceknowledgearticleconfiguration-standardknowledgearticletypeconfiguration"></a>
Provides configuration information for standard Salesforce knowledge articles\.  
*Required*: No  
*Type*: [SalesforceStandardKnowledgeArticleTypeConfiguration](aws-properties-kendra-datasource-salesforcestandardknowledgearticletypeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)