# AWS::DynamoDB::GlobalTable StreamSpecification<a name="aws-properties-dynamodb-globaltable-streamspecification"></a>

Represents the DynamoDB Streams configuration for a table in DynamoDB\.

You can only modify this value if your `AWS::DynamoDB::GlobalTable` contains only one entry in `Replicas`\. You must specify a value for this property if your `AWS::DynamoDB::GlobalTable` contains more than one replica\.

## Syntax<a name="aws-properties-dynamodb-globaltable-streamspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-streamspecification-syntax.json"></a>

```
{
  "[StreamViewType](#cfn-dynamodb-globaltable-streamspecification-streamviewtype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-streamspecification-syntax.yaml"></a>

```
  [StreamViewType](#cfn-dynamodb-globaltable-streamspecification-streamviewtype): String
```

## Properties<a name="aws-properties-dynamodb-globaltable-streamspecification-properties"></a>

`StreamViewType`  <a name="cfn-dynamodb-globaltable-streamspecification-streamviewtype"></a>
 When an item in the table is modified, `StreamViewType` determines what information is written to the stream for this table\. Valid values for `StreamViewType` are:  
+  `KEYS_ONLY` \- Only the key attributes of the modified item are written to the stream\.
+  `NEW_IMAGE` \- The entire item, as it appears after it was modified, is written to the stream\.
+  `OLD_IMAGE` \- The entire item, as it appeared before it was modified, is written to the stream\.
+  `NEW_AND_OLD_IMAGES` \- Both the new and the old item images of the item are written to the stream\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `KEYS_ONLY | NEW_AND_OLD_IMAGES | NEW_IMAGE | OLD_IMAGE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)