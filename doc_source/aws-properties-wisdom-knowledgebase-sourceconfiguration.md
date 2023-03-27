# AWS::Wisdom::KnowledgeBase SourceConfiguration<a name="aws-properties-wisdom-knowledgebase-sourceconfiguration"></a>

Configuration information about the external data source\.

## Syntax<a name="aws-properties-wisdom-knowledgebase-sourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wisdom-knowledgebase-sourceconfiguration-syntax.json"></a>

```
{
  "[AppIntegrations](#cfn-wisdom-knowledgebase-sourceconfiguration-appintegrations)" : AppIntegrationsConfiguration
}
```

### YAML<a name="aws-properties-wisdom-knowledgebase-sourceconfiguration-syntax.yaml"></a>

```
  [AppIntegrations](#cfn-wisdom-knowledgebase-sourceconfiguration-appintegrations): 
    AppIntegrationsConfiguration
```

## Properties<a name="aws-properties-wisdom-knowledgebase-sourceconfiguration-properties"></a>

`AppIntegrations`  <a name="cfn-wisdom-knowledgebase-sourceconfiguration-appintegrations"></a>
Configuration information for Amazon AppIntegrations to automatically ingest content\.  
*Required*: Yes  
*Type*: [AppIntegrationsConfiguration](aws-properties-wisdom-knowledgebase-appintegrationsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)