# AWS::Athena::DataCatalog Tags<a name="aws-properties-athena-datacatalog-tags"></a>

A tag is a label that you assign to a data catalog resource\. Each tag consists of a key and an optional value that you define\. For example, you can use tags to categorize Athena data catalogs by purpose, owner, or environment\. Use a consistent set of tag keys to make it easier to search and filter data catalogs in your account\. Tag keys can be from 1 to 128 UTF\-8 Unicode characters\. Tags can use letters and numbers representable in UTF\-8, and the following characters: \+ \- = \. \_ : / @\. Tag keys are case\-sensitive and must be unique per resource\. 

## Syntax<a name="aws-properties-athena-datacatalog-tags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-datacatalog-tags-syntax.json"></a>

```
{
  "[Tags](#cfn-athena-datacatalog-tags-tags)" : [ Tag, ... ]
}
```

### YAML<a name="aws-properties-athena-datacatalog-tags-syntax.yaml"></a>

```
  [Tags](#cfn-athena-datacatalog-tags-tags): 
    - Tag
```

## Properties<a name="aws-properties-athena-datacatalog-tags-properties"></a>

`Tags`  <a name="cfn-athena-datacatalog-tags-tags"></a>
A list of tags for the data catalog\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: [List](#aws-properties-athena-datacatalog-tags) of [Tag](#aws-properties-athena-datacatalog-tags)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)