# AWS::DynamoDB::GlobalTable PointInTimeRecoverySpecification<a name="aws-properties-dynamodb-globaltable-pointintimerecoveryspecification"></a>

Represents the settings used to enable point in time recovery\.

## Syntax<a name="aws-properties-dynamodb-globaltable-pointintimerecoveryspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-pointintimerecoveryspecification-syntax.json"></a>

```
{
  "[PointInTimeRecoveryEnabled](#cfn-dynamodb-globaltable-pointintimerecoveryspecification-pointintimerecoveryenabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-pointintimerecoveryspecification-syntax.yaml"></a>

```
  [PointInTimeRecoveryEnabled](#cfn-dynamodb-globaltable-pointintimerecoveryspecification-pointintimerecoveryenabled): Boolean
```

## Properties<a name="aws-properties-dynamodb-globaltable-pointintimerecoveryspecification-properties"></a>

`PointInTimeRecoveryEnabled`  <a name="cfn-dynamodb-globaltable-pointintimerecoveryspecification-pointintimerecoveryenabled"></a>
Indicates whether point in time recovery is enabled \(true\) or disabled \(false\) on the table\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)