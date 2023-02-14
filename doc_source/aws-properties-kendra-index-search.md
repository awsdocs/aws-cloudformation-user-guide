# AWS::Kendra::Index Search<a name="aws-properties-kendra-index-search"></a>

Provides information about how a custom index field is used during a search\.

## Syntax<a name="aws-properties-kendra-index-search-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-search-syntax.json"></a>

```
{
  "[Displayable](#cfn-kendra-index-search-displayable)" : Boolean,
  "[Facetable](#cfn-kendra-index-search-facetable)" : Boolean,
  "[Searchable](#cfn-kendra-index-search-searchable)" : Boolean,
  "[Sortable](#cfn-kendra-index-search-sortable)" : Boolean
}
```

### YAML<a name="aws-properties-kendra-index-search-syntax.yaml"></a>

```
  [Displayable](#cfn-kendra-index-search-displayable): Boolean
  [Facetable](#cfn-kendra-index-search-facetable): Boolean
  [Searchable](#cfn-kendra-index-search-searchable): Boolean
  [Sortable](#cfn-kendra-index-search-sortable): Boolean
```

## Properties<a name="aws-properties-kendra-index-search-properties"></a>

`Displayable`  <a name="cfn-kendra-index-search-displayable"></a>
Determines whether the field is returned in the query response\. The default is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Facetable`  <a name="cfn-kendra-index-search-facetable"></a>
Indicates that the field can be used to create search facets, a count of results for each value in the field\. The default is `false` \.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Searchable`  <a name="cfn-kendra-index-search-searchable"></a>
Determines whether the field is used in the search\. If the `Searchable` field is `true`, you can use relevance tuning to manually tune how Amazon Kendra weights the field in the search\. The default is `true` for string fields and `false` for number and date fields\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sortable`  <a name="cfn-kendra-index-search-sortable"></a>
Indicates that the field can be used to sort the search results\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)