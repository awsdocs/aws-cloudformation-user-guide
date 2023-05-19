# AWS::DynamoDB::GlobalTable Projection<a name="aws-properties-dynamodb-globaltable-projection"></a>

Represents attributes that are copied \(projected\) from the table into an index\. These are in addition to the primary key attributes and index key attributes, which are automatically projected\.

## Syntax<a name="aws-properties-dynamodb-globaltable-projection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-projection-syntax.json"></a>

```
{
  "[NonKeyAttributes](#cfn-dynamodb-globaltable-projection-nonkeyattributes)" : [ String, ... ],
  "[ProjectionType](#cfn-dynamodb-globaltable-projection-projectiontype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-projection-syntax.yaml"></a>

```
  [NonKeyAttributes](#cfn-dynamodb-globaltable-projection-nonkeyattributes): 
    - String
  [ProjectionType](#cfn-dynamodb-globaltable-projection-projectiontype): String
```

## Properties<a name="aws-properties-dynamodb-globaltable-projection-properties"></a>

`NonKeyAttributes`  <a name="cfn-dynamodb-globaltable-projection-nonkeyattributes"></a>
Represents the non\-key attribute names which will be projected into the index\.  
For local secondary indexes, the total count of `NonKeyAttributes` summed across all of the local secondary indexes, must not exceed 100\. If you project the same attribute into two different indexes, this counts as two distinct attributes when determining the total\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`ProjectionType`  <a name="cfn-dynamodb-globaltable-projection-projectiontype"></a>
The set of attributes that are projected into the index:  
+  `KEYS_ONLY` \- Only the index and primary keys are projected into the index\.
+  `INCLUDE` \- In addition to the attributes described in `KEYS_ONLY`, the secondary index will include other non\-key attributes that you specify\.
+  `ALL` \- All of the table attributes are projected into the index\.
*Required*: No  
*Type*: String  
*Allowed values*: `ALL | INCLUDE | KEYS_ONLY`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)