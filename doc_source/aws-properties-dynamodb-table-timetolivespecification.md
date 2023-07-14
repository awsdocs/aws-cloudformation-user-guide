# AWS::DynamoDB::Table TimeToLiveSpecification<a name="aws-properties-dynamodb-table-timetolivespecification"></a>

Represents the settings used to enable or disable Time to Live \(TTL\) for the specified table\.

## Syntax<a name="aws-properties-dynamodb-table-timetolivespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-timetolivespecification-syntax.json"></a>

```
{
  "[AttributeName](#cfn-dynamodb-table-timetolivespecification-attributename)" : String,
  "[Enabled](#cfn-dynamodb-table-timetolivespecification-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-table-timetolivespecification-syntax.yaml"></a>

```
  [AttributeName](#cfn-dynamodb-table-timetolivespecification-attributename): String
  [Enabled](#cfn-dynamodb-table-timetolivespecification-enabled): Boolean
```

## Properties<a name="aws-properties-dynamodb-table-timetolivespecification-properties"></a>

`AttributeName`  <a name="cfn-dynamodb-table-timetolivespecification-attributename"></a>
The name of the TTL attribute used to store the expiration time for items in the table\.  
+ The `AttributeName` property is required when enabling the TTL, or when TTL is already enabled\.
+ To update this property, you must first disable TTL and then enable TTL with the new attribute name\.
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-dynamodb-table-timetolivespecification-enabled"></a>
Indicates whether TTL is to be enabled \(true\) or disabled \(false\) on the table\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)