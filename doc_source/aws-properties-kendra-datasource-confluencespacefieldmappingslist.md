# AWS::Kendra::DataSource ConfluenceSpaceFieldMappingsList<a name="aws-properties-kendra-datasource-confluencespacefieldmappingslist"></a>

Specifies one or more `ConfluenceSpaceToIndexFieldMapping` objects\.

## Syntax<a name="aws-properties-kendra-datasource-confluencespacefieldmappingslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluencespacefieldmappingslist-syntax.json"></a>

```
{
  "[ConfluenceSpaceFieldMappingsList](#cfn-kendra-datasource-confluencespacefieldmappingslist-confluencespacefieldmappingslist)" : [ ConfluenceSpaceToIndexFieldMapping, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-confluencespacefieldmappingslist-syntax.yaml"></a>

```
  [ConfluenceSpaceFieldMappingsList](#cfn-kendra-datasource-confluencespacefieldmappingslist-confluencespacefieldmappingslist): 
    - ConfluenceSpaceToIndexFieldMapping
```

## Properties<a name="aws-properties-kendra-datasource-confluencespacefieldmappingslist-properties"></a>

`ConfluenceSpaceFieldMappingsList`  <a name="cfn-kendra-datasource-confluencespacefieldmappingslist-confluencespacefieldmappingslist"></a>
A list of mappings between Confluence and Amazon Kendra index fields\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-confluencespacefieldmappingslist) of [ConfluenceSpaceToIndexFieldMapping](aws-properties-kendra-datasource-confluencespacetoindexfieldmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)