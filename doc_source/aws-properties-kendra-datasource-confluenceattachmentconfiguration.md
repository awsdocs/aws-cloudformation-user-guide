# AWS::Kendra::DataSource ConfluenceAttachmentConfiguration<a name="aws-properties-kendra-datasource-confluenceattachmentconfiguration"></a>

Specifies the attachment settings for the Confluence data source\. Attachment settings are optional, if you don't specify settings attachments, Amazon Kendra won't index them\.

## Syntax<a name="aws-properties-kendra-datasource-confluenceattachmentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluenceattachmentconfiguration-syntax.json"></a>

```
{
  "[AttachmentFieldMappings](#cfn-kendra-datasource-confluenceattachmentconfiguration-attachmentfieldmappings)" : ConfluenceAttachmentFieldMappingsList,
  "[CrawlAttachments](#cfn-kendra-datasource-confluenceattachmentconfiguration-crawlattachments)" : Boolean
}
```

### YAML<a name="aws-properties-kendra-datasource-confluenceattachmentconfiguration-syntax.yaml"></a>

```
  [AttachmentFieldMappings](#cfn-kendra-datasource-confluenceattachmentconfiguration-attachmentfieldmappings): 
    ConfluenceAttachmentFieldMappingsList
  [CrawlAttachments](#cfn-kendra-datasource-confluenceattachmentconfiguration-crawlattachments): Boolean
```

## Properties<a name="aws-properties-kendra-datasource-confluenceattachmentconfiguration-properties"></a>

`AttachmentFieldMappings`  <a name="cfn-kendra-datasource-confluenceattachmentconfiguration-attachmentfieldmappings"></a>
Defines how attachment metadata fields should be mapped to index fields\. Before you can map a field, you must first create an index field with a matching type using the console or the `UpdateIndex` operation\.  
If you specify the `AttachentFieldMappings` parameter, you must specify at least one field mapping\.  
*Required*: No  
*Type*: [ConfluenceAttachmentFieldMappingsList](aws-properties-kendra-datasource-confluenceattachmentfieldmappingslist.md)  
*Maximum*: `11`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrawlAttachments`  <a name="cfn-kendra-datasource-confluenceattachmentconfiguration-crawlattachments"></a>
Indicates whether Amazon Kendra indexes attachments to the pages and blogs in the Confluence data source\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)