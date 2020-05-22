# AWS::DMS::Endpoint DynamoDbSettings<a name="aws-properties-dms-endpoint-dynamodbsettings"></a>

Provides the Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role used to define an Amazon DynamoDB target endpoint\.

## Syntax<a name="aws-properties-dms-endpoint-dynamodbsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-dynamodbsettings-syntax.json"></a>

```
{
  "[ServiceAccessRoleArn](#cfn-dms-endpoint-dynamodbsettings-serviceaccessrolearn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-dynamodbsettings-syntax.yaml"></a>

```
  [ServiceAccessRoleArn](#cfn-dms-endpoint-dynamodbsettings-serviceaccessrolearn): String
```

## Properties<a name="aws-properties-dms-endpoint-dynamodbsettings-properties"></a>

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-dynamodbsettings-serviceaccessrolearn"></a>
 The Amazon Resource Name \(ARN\) used by the service access IAM role\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)