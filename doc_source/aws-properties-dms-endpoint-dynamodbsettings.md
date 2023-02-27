# AWS::DMS::Endpoint DynamoDbSettings<a name="aws-properties-dms-endpoint-dynamodbsettings"></a>

Provides information, including the Amazon Resource Name \(ARN\) of the IAM role used to define an Amazon DynamoDB target endpoint\. This information also includes the output format of records applied to the endpoint and details of transaction and control table data information\. For information about other available settings, see [ Using object mapping to migrate data to DynamoDB](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html#CHAP_Target.DynamoDB.ObjectMapping) in the *AWS Database Migration Service User Guide*\.

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
 The Amazon Resource Name \(ARN\) used by the service to access the IAM role\. The role must allow the `iam:PassRole` action\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)