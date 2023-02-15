# AWS::Wisdom::KnowledgeBase RenderingConfiguration<a name="aws-properties-wisdom-knowledgebase-renderingconfiguration"></a>

Information about how to render the content\.

## Syntax<a name="aws-properties-wisdom-knowledgebase-renderingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wisdom-knowledgebase-renderingconfiguration-syntax.json"></a>

```
{
  "[TemplateUri](#cfn-wisdom-knowledgebase-renderingconfiguration-templateuri)" : String
}
```

### YAML<a name="aws-properties-wisdom-knowledgebase-renderingconfiguration-syntax.yaml"></a>

```
  [TemplateUri](#cfn-wisdom-knowledgebase-renderingconfiguration-templateuri): String
```

## Properties<a name="aws-properties-wisdom-knowledgebase-renderingconfiguration-properties"></a>

`TemplateUri`  <a name="cfn-wisdom-knowledgebase-renderingconfiguration-templateuri"></a>
A URI template containing exactly one variable in `${variableName} `format\. This can only be set for `EXTERNAL` knowledge bases\. For Salesforce and ServiceNow, the variable must be one of the following:  
+ Salesforce: `Id`, `ArticleNumber`, `VersionNumber`, `Title`, `PublishStatus`, or `IsDeleted`
+ ServiceNow: `number`, `short_description`, `sys_mod_count`, `workflow_state`, or `active`
The variable is replaced with the actual value for a piece of content when calling [GetContent](https://docs.aws.amazon.com/wisdom/latest/APIReference/API_GetContent.html)\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)