# AWS::Kendra::Index Relevance<a name="aws-properties-kendra-index-relevance"></a>

Provides information for manually tuning the relevance of a field in a search\. When a query includes terms that match the field, the results are given a boost in the response based on these tuning parameters\.

## Syntax<a name="aws-properties-kendra-index-relevance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-relevance-syntax.json"></a>

```
{
  "[Duration](#cfn-kendra-index-relevance-duration)" : String,
  "[Freshness](#cfn-kendra-index-relevance-freshness)" : Boolean,
  "[Importance](#cfn-kendra-index-relevance-importance)" : Integer,
  "[RankOrder](#cfn-kendra-index-relevance-rankorder)" : String,
  "[ValueImportanceItems](#cfn-kendra-index-relevance-valueimportanceitems)" : ValueImportanceItems
}
```

### YAML<a name="aws-properties-kendra-index-relevance-syntax.yaml"></a>

```
  [Duration](#cfn-kendra-index-relevance-duration): String
  [Freshness](#cfn-kendra-index-relevance-freshness): Boolean
  [Importance](#cfn-kendra-index-relevance-importance): Integer
  [RankOrder](#cfn-kendra-index-relevance-rankorder): String
  [ValueImportanceItems](#cfn-kendra-index-relevance-valueimportanceitems): 
    ValueImportanceItems
```

## Properties<a name="aws-properties-kendra-index-relevance-properties"></a>

`Duration`  <a name="cfn-kendra-index-relevance-duration"></a>
Specifies the time period that the boost applies to\. For example, to make the boost apply to documents with the field value within the last month, you would use "2628000s"\. Once the field value is beyond the specified range, the effect of the boost drops off\. The higher the importance, the faster the effect drops off\. If you don't specify a value, the default is 3 months\. The value of the field is a numeric string followed by the character "s", for example "86400s" for one day, or "604800s" for one week\.   
Only applies to `DATE` fields\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `10`  
*Pattern*: `[0-9]+[s]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Freshness`  <a name="cfn-kendra-index-relevance-freshness"></a>
Indicates that this field determines how "fresh" a document is\. For example, if document 1 was created on November 5, and document 2 was created on October 31, document 1 is "fresher" than document 2\. You can only set the `Freshness` field on one `DATE` type field\. Only applies to `DATE` fields\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Importance`  <a name="cfn-kendra-index-relevance-importance"></a>
The relative importance of the field in the search\. Larger numbers provide more of a boost than smaller numbers\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RankOrder`  <a name="cfn-kendra-index-relevance-rankorder"></a>
Determines how values should be interpreted\.  
When the `RankOrder` field is `ASCENDING`, higher numbers are better\. For example, a document with a rating score of 10 is higher ranking than a document with a rating score of 1\.  
When the `RankOrder` field is `DESCENDING`, lower numbers are better\. For example, in a task tracking application, a priority 1 task is more important than a priority 5 task\.  
Only applies to `LONG` and `DOUBLE` fields\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ASCENDING | DESCENDING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueImportanceItems`  <a name="cfn-kendra-index-relevance-valueimportanceitems"></a>
An array of key\-value pairs that contains an array of values that should be given a different boost when they appear in the search result list\. For example, if you are boosting query terms that match the department field in the result, query terms that match the department field are boosted in the result\. You can add entries from the department field to boost documents with those values higher\.  
For example, you can add entries to the map with names of departments\. If you add "HR", 5 and "Legal",3 those departments are given special attention when they appear in the metadata of a document\.  
*Required*: No  
*Type*: [ValueImportanceItems](aws-properties-kendra-index-valueimportanceitems.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)