# AWS::Kendra::Index ValueImportanceItems<a name="aws-properties-kendra-index-valueimportanceitems"></a>

An array of key\-value pairs that contains an array of values that should be given a different boost when they appear in the search result list\. For example, if you are boosting query terms that match the department field in the result, query terms that match the department field are boosted in the result\. You can add entries from the department field to boost documents with those values higher\.

For example, you can add entries to the map with names of departments\. If you add "HR", 5 and "Legal",3 those departments are given special attention when they appear in the metadata of a document\.

## Syntax<a name="aws-properties-kendra-index-valueimportanceitems-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-valueimportanceitems-syntax.json"></a>

```
{
  "[ValueImportanceItems](#cfn-kendra-index-valueimportanceitems-valueimportanceitems)" : [ ValueImportanceItem, ... ]
}
```

### YAML<a name="aws-properties-kendra-index-valueimportanceitems-syntax.yaml"></a>

```
  [ValueImportanceItems](#cfn-kendra-index-valueimportanceitems-valueimportanceitems): 
    - ValueImportanceItem
```

## Properties<a name="aws-properties-kendra-index-valueimportanceitems-properties"></a>

`ValueImportanceItems`  <a name="cfn-kendra-index-valueimportanceitems-valueimportanceitems"></a>
A key\-value pair that indicates the key should be boosted by the amount in the value when it appears in the result of a search\. For example, if you add "HR",5 that key is boosted by 5 when it appears in the metadata of a document\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-index-valueimportanceitems) of [ValueImportanceItem](aws-properties-kendra-index-valueimportanceitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)