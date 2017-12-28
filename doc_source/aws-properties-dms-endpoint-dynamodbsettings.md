# AWS DMS Endpoint DynamoDBSettings<a name="aws-properties-dms-endpoint-dynamodbsettings"></a>

Use the `DynamoDBSettings` property to specify settings for an DynamoDB endpoint for an  resource\.

## Syntax<a name="w3ab2c21c14d496b5"></a>

### JSON<a name="aws-properties-dms-endpoint-dynamodbsettings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-dynamodbsettings-serviceaccessrolearn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-dynamodbsettings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-dynamodbsettings-serviceaccessrolearn): String
```

## Properties<a name="w3ab2c21c14d496b7"></a>

For more information about option settings, see [Using an Amazon DynamoDB Database as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html) in the *AWS Database Migration Service User Guide*

`ServiceAccessRoleArn`  
The Amazon Resource Name \(ARN\) used by the service access IAM role\.  
*Required: *Yes  
*Type*: String