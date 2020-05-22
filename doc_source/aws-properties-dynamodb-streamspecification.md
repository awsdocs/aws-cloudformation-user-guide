# AWS::DynamoDB::Table StreamSpecification<a name="aws-properties-dynamodb-streamspecification"></a>

Represents the DynamoDB Streams configuration for a table in DynamoDB\.

## Syntax<a name="aws-properties-dynamodb-streamspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-streamspecification-syntax.json"></a>

```
{
  "[StreamViewType](#cfn-dynamodb-streamspecification-streamviewtype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-streamspecification-syntax.yaml"></a>

```
  [StreamViewType](#cfn-dynamodb-streamspecification-streamviewtype): String
```

## Properties<a name="aws-properties-dynamodb-streamspecification-properties"></a>

`StreamViewType`  <a name="cfn-dynamodb-streamspecification-streamviewtype"></a>
 When an item in the table is modified, `StreamViewType` determines what information is written to the stream for this table\. Valid values for `StreamViewType` are:  
+  `KEYS_ONLY` \- Only the key attributes of the modified item are written to the stream\.
+  `NEW_IMAGE` \- The entire item, as it appears after it was modified, is written to the stream\.
+  `OLD_IMAGE` \- The entire item, as it appeared before it was modified, is written to the stream\.
+  `NEW_AND_OLD_IMAGES` \- Both the new and the old item images of the item are written to the stream\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)