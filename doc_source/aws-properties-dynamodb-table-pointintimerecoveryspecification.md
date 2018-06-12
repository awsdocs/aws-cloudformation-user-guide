# DynamoDB Table PointInTimeRecoverySpecification<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification"></a>

<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-description"></a>The `PointInTimeRecoverySpecification` property type enables point in time recovery in a DynamoDB table\.

<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-inheritance"></a> `PointInTimeRecoverySpecification` is a property of the [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource\.

## Syntax<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax.json"></a>

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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-seealso"></a>
+ [PointInTimeRecoverySpecification](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_PointInTimeRecoverySpecification.html) in the *Amazon DynamoDB API Reference*