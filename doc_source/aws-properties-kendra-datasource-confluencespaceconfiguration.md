# AWS::Kendra::DataSource ConfluenceSpaceConfiguration<a name="aws-properties-kendra-datasource-confluencespaceconfiguration"></a>

Specifies the configuration for indexing Confluence spaces\.

## Syntax<a name="aws-properties-kendra-datasource-confluencespaceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluencespaceconfiguration-syntax.json"></a>

```
{
  "[CrawlArchivedSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-crawlarchivedspaces)" : Boolean,
  "[CrawlPersonalSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-crawlpersonalspaces)" : Boolean,
  "[ExcludeSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-excludespaces)" : ConfluenceSpaceList,
  "[IncludeSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-includespaces)" : ConfluenceSpaceList,
  "[SpaceFieldMappings](#cfn-kendra-datasource-confluencespaceconfiguration-spacefieldmappings)" : ConfluenceSpaceFieldMappingsList
}
```

### YAML<a name="aws-properties-kendra-datasource-confluencespaceconfiguration-syntax.yaml"></a>

```
  [CrawlArchivedSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-crawlarchivedspaces): Boolean
  [CrawlPersonalSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-crawlpersonalspaces): Boolean
  [ExcludeSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-excludespaces): 
    ConfluenceSpaceList
  [IncludeSpaces](#cfn-kendra-datasource-confluencespaceconfiguration-includespaces): 
    ConfluenceSpaceList
  [SpaceFieldMappings](#cfn-kendra-datasource-confluencespaceconfiguration-spacefieldmappings): 
    ConfluenceSpaceFieldMappingsList
```

## Properties<a name="aws-properties-kendra-datasource-confluencespaceconfiguration-properties"></a>

`CrawlArchivedSpaces`  <a name="cfn-kendra-datasource-confluencespaceconfiguration-crawlarchivedspaces"></a>
Specifies whether Amazon Kendra should index archived spaces\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrawlPersonalSpaces`  <a name="cfn-kendra-datasource-confluencespaceconfiguration-crawlpersonalspaces"></a>
Specifies whether Amazon Kendra should index personal spaces\. Users can add restrictions to items in personal spaces\. If personal spaces are indexed, queries without user context information may return restricted items from a personal space in their results\. For more information, see [Filtering on user context](https://docs.aws.amazon.com/kendra/latest/dg/user-context-filter.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeSpaces`  <a name="cfn-kendra-datasource-confluencespaceconfiguration-excludespaces"></a>
A list of space keys of Confluence spaces\. If you include a key, the blogs, documents, and attachments in the space are not indexed\. If a space is in both the `ExcludeSpaces` and the `IncludeSpaces` list, the space is excluded\.  
*Required*: No  
*Type*: [ConfluenceSpaceList](aws-properties-kendra-datasource-confluencespacelist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeSpaces`  <a name="cfn-kendra-datasource-confluencespaceconfiguration-includespaces"></a>
A list of space keys for Confluence spaces\. If you include a key, the blogs, documents, and attachments in the space are indexed\. Spaces that aren't in the list aren't indexed\. A space in the list must exist\. Otherwise, Amazon Kendra logs an error when the data source is synchronized\. If a space is in both the `IncludeSpaces` and the `ExcludeSpaces` list, the space is excluded\.  
*Required*: No  
*Type*: [ConfluenceSpaceList](aws-properties-kendra-datasource-confluencespacelist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpaceFieldMappings`  <a name="cfn-kendra-datasource-confluencespaceconfiguration-spacefieldmappings"></a>
Defines how space metadata fields should be mapped to index fields\. Before you can map a field, you must first create an index field with a matching type using the console or the `UpdateIndex` operation\.  
If you specify the `SpaceFieldMappings` parameter, you must specify at least one field mapping\.  
*Required*: No  
*Type*: [ConfluenceSpaceFieldMappingsList](aws-properties-kendra-datasource-confluencespacefieldmappingslist.md)  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)