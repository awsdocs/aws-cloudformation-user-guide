# AWS::Kendra::Index DocumentMetadataConfiguration<a name="aws-properties-kendra-index-documentmetadataconfiguration"></a>

Specifies the properties of a custom index field\.

## Syntax<a name="aws-properties-kendra-index-documentmetadataconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-documentmetadataconfiguration-syntax.json"></a>

```
{
  "[Name](#cfn-kendra-index-documentmetadataconfiguration-name)" : String,
  "[Relevance](#cfn-kendra-index-documentmetadataconfiguration-relevance)" : Relevance,
  "[Search](#cfn-kendra-index-documentmetadataconfiguration-search)" : Search,
  "[Type](#cfn-kendra-index-documentmetadataconfiguration-type)" : String
}
```

### YAML<a name="aws-properties-kendra-index-documentmetadataconfiguration-syntax.yaml"></a>

```
  [Name](#cfn-kendra-index-documentmetadataconfiguration-name): String
  [Relevance](#cfn-kendra-index-documentmetadataconfiguration-relevance): 
    Relevance
  [Search](#cfn-kendra-index-documentmetadataconfiguration-search): 
    Search
  [Type](#cfn-kendra-index-documentmetadataconfiguration-type): String
```

## Properties<a name="aws-properties-kendra-index-documentmetadataconfiguration-properties"></a>

`Name`  <a name="cfn-kendra-index-documentmetadataconfiguration-name"></a>
The name of the index field\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Relevance`  <a name="cfn-kendra-index-documentmetadataconfiguration-relevance"></a>
Provides manual tuning parameters to determine how the field affects the search results\.  
*Required*: No  
*Type*: [Relevance](aws-properties-kendra-index-relevance.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Search`  <a name="cfn-kendra-index-documentmetadataconfiguration-search"></a>
Provides information about how the field is used during a search\.  
*Required*: No  
*Type*: [Search](aws-properties-kendra-index-search.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-kendra-index-documentmetadataconfiguration-type"></a>
The data type of the index field\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `DATE_VALUE | LONG_VALUE | STRING_LIST_VALUE | STRING_VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)