# AWS::Kendra::DataSource InlineCustomDocumentEnrichmentConfiguration<a name="aws-properties-kendra-datasource-inlinecustomdocumentenrichmentconfiguration"></a>

Provides the configuration information for applying basic logic to alter document metadata and content when ingesting documents into Amazon Kendra\. To apply advanced logic, to go beyond what you can do with basic logic, see [HookConfiguration](https://docs.aws.amazon.com/kendra/latest/dg/API_HookConfiguration.html)\.

For more information, see [Customizing document metadata during the ingestion process](https://docs.aws.amazon.com/kendra/latest/dg/custom-document-enrichment.html)\.

## Syntax<a name="aws-properties-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-syntax.json"></a>

```
{
  "[Condition](#cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-condition)" : DocumentAttributeCondition,
  "[DocumentContentDeletion](#cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-documentcontentdeletion)" : Boolean,
  "[Target](#cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-target)" : DocumentAttributeTarget
}
```

### YAML<a name="aws-properties-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-syntax.yaml"></a>

```
  [Condition](#cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-condition): 
    DocumentAttributeCondition
  [DocumentContentDeletion](#cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-documentcontentdeletion): Boolean
  [Target](#cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-target): 
    DocumentAttributeTarget
```

## Properties<a name="aws-properties-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-properties"></a>

`Condition`  <a name="cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-condition"></a>
Configuration of the condition used for the target document attribute or metadata field when ingesting documents into Amazon Kendra\.  
*Required*: No  
*Type*: [DocumentAttributeCondition](aws-properties-kendra-datasource-documentattributecondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentContentDeletion`  <a name="cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-documentcontentdeletion"></a>
 `TRUE` to delete content if the condition used for the target attribute is met\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-kendra-datasource-inlinecustomdocumentenrichmentconfiguration-target"></a>
Configuration of the target document attribute or metadata field when ingesting documents into Amazon Kendra\. You can also include a value\.  
*Required*: No  
*Type*: [DocumentAttributeTarget](aws-properties-kendra-datasource-documentattributetarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)