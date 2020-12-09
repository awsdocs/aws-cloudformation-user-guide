# AWS::DynamoDB::Table PointInTimeRecoverySpecification<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification"></a>

The settings used to enable point in time recovery\.

## Syntax<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-syntax.json"></a>

```
{
  "[PointInTimeRecoveryEnabled](#cfn-dynamodb-table-pointintimerecoveryspecification-pointintimerecoveryenabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-syntax.yaml"></a>

```
  [PointInTimeRecoveryEnabled](#cfn-dynamodb-table-pointintimerecoveryspecification-pointintimerecoveryenabled): Boolean
```

## Properties<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-properties"></a>

`PointInTimeRecoveryEnabled`  <a name="cfn-dynamodb-table-pointintimerecoveryspecification-pointintimerecoveryenabled"></a>
Indicates whether point in time recovery is enabled \(true\) or disabled \(false\) on the table\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification--seealso"></a>

 [PointInTimeRecoverySpecification](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_PointInTimeRecoverySpecification.html) in the Amazon DynamoDB API Reference\. 