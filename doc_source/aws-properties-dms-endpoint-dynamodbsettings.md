# AWS DMS Endpoint DynamoDBSettings<a name="aws-properties-dms-endpoint-dynamodbsettings"></a>

Use the `DynamoDBSettings` property to specify settings for an DynamoDB endpoint for an [AWS::DMS::Endpoint](aws-resource-dms-endpoint.md) resource\.

## Syntax<a name="w3ab2c21c14d578b5"></a>

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

## Properties<a name="w3ab2c21c14d578b7"></a>

For more information about option settings, see [Using an Amazon DynamoDB Database as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html) in the *AWS Database Migration Service User Guide*

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-dynamodbsettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) used by the service access IAM role\.  
*Required*: Yes  
*Type*: String