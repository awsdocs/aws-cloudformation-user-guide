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
+  For [ Salesforce](https://developer.salesforce.com/docs/atlas.en-us.knowledge_dev.meta/knowledge_dev/sforce_api_objects_knowledge__kav.htm), your AppIntegrations DataIntegration must have an ObjectConfiguration if objectFields is not provided, including at least `Id`, `ArticleNumber`, `VersionNumber`, `Title`, `PublishStatus`, and `IsDeleted` as source fields\. 
+  For [ ServiceNow](https://developer.servicenow.com/dev.do#!/reference/api/rome/rest/knowledge-management-api), your AppIntegrations DataIntegration must have an ObjectConfiguration if objectFields is not provided, including at least `number`, `short_description`, `sys_mod_count`, `workflow_state`, and `active` as source fields\. 
+  For [ Zendesk](https://developer.zendesk.com/api-reference/help_center/help-center-api/articles/), your AppIntegrations DataIntegration must have an ObjectConfiguration if `objectFields` is not provided, including at least `id`, `title`, `updated_at`, and `draft` as source fields\. 
+  For [ SharePoint](https://learn.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-net-server-csom-jsom-and-rest-api-index), your AppIntegrations DataIntegration must have a FileConfiguration, including only file extensions that are among `docx`, `pdf`, `html`, `htm`, and `txt`\. 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^arn:[a-z-]+?:[a-z-]+?:[a-z0-9-]*?:([0-9]{12})?:[a-zA-Z0-9-:/]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ObjectFields`  <a name="cfn-wisdom-knowledgebase-appintegrationsconfiguration-objectfields"></a>
The fields from the source that are made available to your agents in Wisdom\. Optional if ObjectConfiguration is included in the provided DataIntegration\.   
+  For [ Salesforce](https://developer.salesforce.com/docs/atlas.en-us.knowledge_dev.meta/knowledge_dev/sforce_api_objects_knowledge__kav.htm), you must include at least `Id`, `ArticleNumber`, `VersionNumber`, `Title`, `PublishStatus`, and `IsDeleted`\. 
+ For [ ServiceNow](https://developer.servicenow.com/dev.do#!/reference/api/rome/rest/knowledge-management-api), you must include at least `number`, `short_description`, `sys_mod_count`, `workflow_state`, and `active`\. 
+ For [ Zendesk](https://developer.zendesk.com/api-reference/help_center/help-center-api/articles/), you must include at least `id`, `title`, `updated_at`, and `draft`\. 
Make sure to include additional fields\. These fields are indexed and used to source recommendations\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)