# AWS::DMS::Endpoint<a name="aws-resource-dms-endpoint"></a>

The `AWS::DMS::Endpoint` resource creates an AWS DMS endpoint\.


+ [Syntax](#aws-resource-dms-endpoint-syntax)
+ [Properties](#aws-resource-dms-endpoint-properties)
+ [Return Value](#aws-resource-dms-endpoint-examples-returnvalues)
+ [Example](#aws-resource-dms-endpoint-examples)
+ [See Also](#w3ab2c21c10d315c15)

## Syntax<a name="aws-resource-dms-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-endpoint-syntax.json"></a>

```
{
  "Type": "AWS::DMS::Endpoint",
  "Properties": {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-certificatearn)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-databasename)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-dynamodbsettings)": DynamoDbSettings,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-endpointidentifier)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-endpointtype)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-enginename)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-extraconnectionattributes)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-kmskeyid)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings)": MongoDbSettings,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-password)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-port)": Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings)": S3Settings,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-servername)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-sslmode)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-tags)": [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-username)": String
  }
}
```

### YAML<a name="aws-resource-dms-endpoint-syntax.yaml"></a>

```
Type: "AWS::DMS::Endpoint"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-certificatearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-databasename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-dynamodbsettings):
    DynamoDbSettings
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-endpointidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-endpointtype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-enginename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-extraconnectionattributes): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-kmskeyid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings): 
    MongoDbSettings
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-password): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-port): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-s3settings):
    S3Settings
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-servername): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-sslmode): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-tags):
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-username): String
```

## Properties<a name="aws-resource-dms-endpoint-properties"></a>

`CertificateArn`  
The Amazon Resource Number \(ARN\) for the certificate\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`DatabaseName`  
The name of the endpoint database\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`DynamoDbSettings`  
Settings in JSON format for the target DynamoDB endpoint\. For more information about the available settings, see the **Using Object Mapping to Migrate Data to DynamoDB** section at [ Using an Amazon DynamoDB Database as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html)\.  
*Required: *No  
*Type: *[AWS DMS Endpoint DynamoDBSettings](aws-properties-dms-endpoint-dynamodbsettings.md)  
*Update requires*: No interruption

`EndpointIdentifier`  
The database endpoint identifier\. Identifiers must begin with a letter; must contain only ASCII letters, digits, and hyphens; and must not end with a hyphen or contain two consecutive hyphens\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`EndpointType`  
The type of endpoint\. Valid values are `source` and `target`\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`EngineName`  
The type of engine for the endpoint\. Valid values depend on the `EndPointType` and include `MYSQL`, `ORACLE`, `POSTGRES`, `MARIADB`, `AURORA`, `REDSHIFT`, `S3`, `SYBASE`, `DYNAMODB`, `MONGODB`, and `SQLSERVER`\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`ExtraConnectionAttributes`  
Additional attributes associated with the connection\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`KmsKeyId`  
The KMS key identifier that will be used to encrypt the connection parameters\. If you do not specify a value for the `KmsKeyId` parameter, then AWS DMS will use your default encryption key\. AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS region\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`MongoDbSettings`  
Settings in JSON format for the source MongoDB endpoint\. For more information about the available settings, see the **Configuration Properties When Using MongoDB as a Source for AWS Database Migration Service** section at [ Using Amazon S3 as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html)\.  
*Required: *No  
*Type: *[AWS DMS Endpoint MongoDbSettings](aws-properties-dms-endpoint-mongodbsettings.md)  
*Update requires*: No interruption

`Password`  
The password to be used to login to the endpoint database\. Do not use this parameter directly\. Use `Password` as an input parameter with `noEcho` as shown in the [Parameters](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\. For best practices information, see [Do Not Embed Credentials in Your Templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds)\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Port`  
The port used by the endpoint database\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`S3Settings`  
Settings in JSON format for the target Amazon S3 endpoint\. For more information about the available settings, see the **Extra Connection Attributes** section at [ Using Amazon S3 as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html) in the *AWS Database Migration Service User Guide*\.  
*Required: *No  
*Type:* [AWS DMS Endpoint S3Settings](aws-properties-dms-endpoint-s3settings.md)  
*Update requires*: No interruption

`ServerName`  
The name of the server where the endpoint database resides\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`SslMode`  
The SSL mode to use for the SSL connection\.  
SSL mode can be one of four values: `none`, `require`, `verify-ca`, `verify-full`\. The default value is `none`\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Tags`  
The tags that you want to attach to the DMS endpoint\.  
*Required: *No  
*Type*: List of resource tags in key\-value format  
*Update requires*: Replacement 

`Username`  
The user name to be used to login to the endpoint database\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

## Return Value<a name="aws-resource-dms-endpoint-examples-returnvalues"></a>

### Ref<a name="w3ab2c21c10d315c11b3"></a>

When you pass the logical ID of an `AWS::DMS::Endpoint` resource to the intrinsic `Ref` function, the function returns the ARN of the endpoint\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="aws-resource-dms-endpoint-examples"></a>

### JSON<a name="aws-resource-dms-endpoint-example1.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "myBasicEndpoint": {
      "Type": "AWS::DMS::Endpoint",
      "Properties": {
        "EngineName": "mysql",
        "EndpointType": "source",
        "Username": "username",
        "Password": {
          "Ref": "PasswordParameter"
        },
        "ServerName": "source.db.amazon.com",
        "Port": 1234,
        "DatabaseName": "source-db"
      }
    }
  }
}
```

### YAML<a name="aws-resource-dms-endpoint-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: "Endpoint test"
Resources:
  BasicEndpoint:
    Type: "AWS::DMS::Endpoint"
    Properties:
      EngineName: "mysql"
      EndpointType: "target"
      Username: "username"
      Password: !Ref PasswordParameter
      ServerName: "server.db.amazon.com"
      Port: 1234
      DatabaseName: "my-db"
      Tags:
        - Key: "type"
          Value: "new"
```

## See Also<a name="w3ab2c21c10d315c15"></a>

+ [CreateEndpoint](http://docs.aws.amazon.com/dms/latest/APIReference/API_CreateEndpoint.html) in the *AWS Database Migration Service API Reference*\.

+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)