# AWS::DynamoDB::Table TimeToLiveSpecification<a name="aws-properties-dynamodb-timetolivespecification"></a>

Represents the settings used to enable or disable Time to Live for the specified table\.

## Syntax<a name="aws-properties-dynamodb-timetolivespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-timetolivespecification-syntax.json"></a>

```
{
  "[AttributeName](#cfn-dynamodb-timetolivespecification-attributename)" : String,
  "[Enabled](#cfn-dynamodb-timetolivespecification-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-timetolivespecification-syntax.yaml"></a>

```
  [AttributeName](#cfn-dynamodb-timetolivespecification-attributename): String
  [Enabled](#cfn-dynamodb-timetolivespecification-enabled): Boolean
```

## Properties<a name="aws-properties-dynamodb-timetolivespecification-properties"></a>

`AttributeName`  <a name="cfn-dynamodb-timetolivespecification-attributename"></a>
The name of the Time to Live attribute used to store the expiration time for items in the table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-dynamodb-timetolivespecification-enabled"></a>
Indicates whether Time To Live is to be enabled \(true\) or disabled \(false\) on the table\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)