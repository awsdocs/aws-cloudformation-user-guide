# AWS::Wisdom::KnowledgeBase AppIntegrationsConfiguration<a name="aws-properties-wisdom-knowledgebase-appintegrationsconfiguration"></a>

Configuration information for Amazon AppIntegrations to automatically ingest content\.

## Syntax<a name="aws-properties-wisdom-knowledgebase-appintegrationsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wisdom-knowledgebase-appintegrationsconfiguration-syntax.json"></a>

```
{
  "[AppIntegrationArn](#cfn-wisdom-knowledgebase-appintegrationsconfiguration-appintegrationarn)" : String,
  "[ObjectFields](#cfn-wisdom-knowledgebase-appintegrationsconfiguration-objectfields)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-wisdom-knowledgebase-appintegrationsconfiguration-syntax.yaml"></a>

```
  [AppIntegrationArn](#cfn-wisdom-knowledgebase-appintegrationsconfiguration-appintegrationarn): String
  [ObjectFields](#cfn-wisdom-knowledgebase-appintegrationsconfiguration-objectfields): 
    - String
```

## Properties<a name="aws-properties-wisdom-knowledgebase-appintegrationsconfiguration-properties"></a>

`AppIntegrationArn`  <a name="cfn-wisdom-knowledgebase-appintegrationsconfiguration-appintegrationarn"></a>
The Amazon Resource Name \(ARN\) of the AppIntegrations DataIntegration to use for ingesting content\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^arn:[a-z-]+?:[a-z-]+?:[a-z0-9-]*?:([0-9]{12})?:[a-zA-Z0-9-:/]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ObjectFields`  <a name="cfn-wisdom-knowledgebase-appintegrationsconfiguration-objectfields"></a>
The fields from the source that are made available to your agents in Wisdom\.   
+  For [ Salesforce](https://developer.salesforce.com/docs/atlas.en-us.knowledge_dev.meta/knowledge_dev/sforce_api_objects_knowledge__kav.htm), you must include at least `Id`, `ArticleNumber`, `VersionNumber`, `Title`, `PublishStatus`, and `IsDeleted`\. 
+ For [ ServiceNow](https://developer.servicenow.com/dev.do#!/reference/api/rome/rest/knowledge-management-api), you must include at least `number`, `short_description`, `sys_mod_count`, `workflow_state`, and `active`\. 
Make sure to include additional fields\. These fields are indexed and used to source recommendations\.   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)