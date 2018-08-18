# AWS::DMS::Endpoint<a name="aws-resource-dms-endpoint"></a>

The `AWS::DMS::Endpoint` resource creates an AWS DMS endpoint\.

**Topics**
+ [Syntax](#aws-resource-dms-endpoint-syntax)
+ [Properties](#aws-resource-dms-endpoint-properties)
+ [Return Value](#aws-resource-dms-endpoint-examples-returnvalues)
+ [Example](#aws-resource-dms-endpoint-examples)
+ [See Also](#w3ab2c21c10d352c15)

## Syntax<a name="aws-resource-dms-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-endpoint-syntax.json"></a>

```
{
  "Type": "AWS::DMS::Endpoint",
  "Properties": {
    "[CertificateArn](#cfn-dms-endpoint-certificatearn)": String,
    "[DatabaseName](#cfn-dms-endpoint-databasename)": String,
    "[DynamoDbSettings](#cfn-dms-endpoint-dynamodbsettings)": DynamoDbSettings,
    "[EndpointIdentifier](#cfn-dms-endpoint-endpointidentifier)": String,
    "[EndpointType](#cfn-dms-endpoint-endpointtype)": String,
    "[EngineName](#cfn-dms-endpoint-enginename)": String,
    "[ExtraConnectionAttributes](#cfn-dms-endpoint-extraconnectionattributes)": String,
    "[KmsKeyId](#cfn-dms-endpoint-kmskeyid)": String,
    "[MongoDbSettings](#cfn-dms-endpoint-mongodbsettings)": MongoDbSettings,
    "[Password](#cfn-dms-endpoint-password)": String,
    "[Port](#cfn-dms-endpoint-port)": Integer,
    "[S3Settings](#cfn-dms-endpoint-s3settings)": S3Settings,
    "[ServerName](#cfn-dms-endpoint-servername)": String,
    "[SslMode](#cfn-dms-endpoint-sslmode)": String,
    "[Tags](#cfn-dms-endpoint-tags)": [ Resource Tag, ... ],
    "[Username](#cfn-dms-endpoint-username)": String
  }
}
```

### YAML<a name="aws-resource-dms-endpoint-syntax.yaml"></a>

```
Type: "AWS::DMS::Endpoint"
Properties:
  [CertificateArn](#cfn-dms-endpoint-certificatearn): String
  [DatabaseName](#cfn-dms-endpoint-databasename): String
  [DynamoDbSettings](#cfn-dms-endpoint-dynamodbsettings):
    DynamoDbSettings
  [EndpointIdentifier](#cfn-dms-endpoint-endpointidentifier): String
  [EndpointType](#cfn-dms-endpoint-endpointtype): String
  [EngineName](#cfn-dms-endpoint-enginename): String
  [ExtraConnectionAttributes](#cfn-dms-endpoint-extraconnectionattributes): String
  [KmsKeyId](#cfn-dms-endpoint-kmskeyid): String
  [MongoDbSettings](#cfn-dms-endpoint-mongodbsettings): 
    MongoDbSettings
  [Password](#cfn-dms-endpoint-password): String
  [Port](#cfn-dms-endpoint-port): Integer
  [S3Settings](#cfn-dms-endpoint-s3settings):
    S3Settings
  [ServerName](#cfn-dms-endpoint-servername): String
  [SslMode](#cfn-dms-endpoint-sslmode): String
  [Tags](#cfn-dms-endpoint-tags):
    - Resource Tag
  [Username](#cfn-dms-endpoint-username): String
```

## Properties<a name="aws-resource-dms-endpoint-properties"></a>

`CertificateArn`  <a name="cfn-dms-endpoint-certificatearn"></a>
The Amazon Resource Number \(ARN\) for the certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DatabaseName`  <a name="cfn-dms-endpoint-databasename"></a>
The name of the endpoint database\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DynamoDbSettings`  <a name="cfn-dms-endpoint-dynamodbsettings"></a>
Settings in JSON format for the target DynamoDB endpoint\. For more information about the available settings, see the **Using Object Mapping to Migrate Data to DynamoDB** section at [ Using an Amazon DynamoDB Database as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html)\.  
*Required*: No  
*Type: *[AWS DMS Endpoint DynamoDBSettings](aws-properties-dms-endpoint-dynamodbsettings.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EndpointIdentifier`  <a name="cfn-dms-endpoint-endpointidentifier"></a>
The database endpoint identifier\. Identifiers must begin with a letter; must contain only ASCII letters, digits, and hyphens; and must not end with a hyphen or contain two consecutive hyphens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EndpointType`  <a name="cfn-dms-endpoint-endpointtype"></a>
The type of endpoint\. Valid values are `source` and `target`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EngineName`  <a name="cfn-dms-endpoint-enginename"></a>
The type of engine for the endpoint\. Valid values depend on the `EndPointType` and include `MYSQL`, `ORACLE`, `POSTGRES`, `MARIADB`, `AURORA`, `REDSHIFT`, `S3`, `SYBASE`, `DYNAMODB`, `MONGODB`, and `SQLSERVER`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ExtraConnectionAttributes`  <a name="cfn-dms-endpoint-extraconnectionattributes"></a>
Additional attributes associated with the connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyId`  <a name="cfn-dms-endpoint-kmskeyid"></a>
The KMS key identifier that will be used to encrypt the connection parameters\. If you do not specify a value for the `KmsKeyId` parameter, then AWS DMS will use your default encryption key\. AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MongoDbSettings`  <a name="cfn-dms-endpoint-mongodbsettings"></a>
Settings in JSON format for the source MongoDB endpoint\. For more information about the available settings, see the **Configuration Properties When Using MongoDB as a Source for AWS Database Migration Service** section at [ Using Amazon S3 as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html)\.  
*Required*: No  
*Type: *[AWS DMS Endpoint MongoDbSettings](aws-properties-dms-endpoint-mongodbsettings.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Password`  <a name="cfn-dms-endpoint-password"></a>
The password to be used to login to the endpoint database\. Do not use this parameter directly\. Use `Password` as an input parameter with `noEcho` as shown in the [Parameters](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\. For best practices information, see [Do Not Embed Credentials in Your Templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Port`  <a name="cfn-dms-endpoint-port"></a>
The port used by the endpoint database\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`S3Settings`  <a name="cfn-dms-endpoint-s3settings"></a>
Settings in JSON format for the target Amazon S3 endpoint\. For more information about the available settings, see the **Extra Connection Attributes** section at [ Using Amazon S3 as a Target for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type:* [AWS DMS Endpoint S3Settings](aws-properties-dms-endpoint-s3settings.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ServerName`  <a name="cfn-dms-endpoint-servername"></a>
The name of the server where the endpoint database resides\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SslMode`  <a name="cfn-dms-endpoint-sslmode"></a>
The SSL mode to use for the SSL connection\.  
SSL mode can be one of four values: `none`, `require`, `verify-ca`, `verify-full`\. The default value is `none`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-dms-endpoint-tags"></a>
The tags that you want to attach to the DMS endpoint\.  
*Required*: No  
*Type*: List of [resource tags](aws-properties-resource-tags.md) in key\-value format  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Username`  <a name="cfn-dms-endpoint-username"></a>
The user name to be used to login to the endpoint database\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-dms-endpoint-examples-returnvalues"></a>

### Ref<a name="w3ab2c21c10d352c11b3"></a>

When you pass the logical ID of an `AWS::DMS::Endpoint` resource to the intrinsic `Ref` function, the function returns the ARN of the endpoint\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

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

## See Also<a name="w3ab2c21c10d352c15"></a>
+ [CreateEndpoint](http://docs.aws.amazon.com/dms/latest/APIReference/API_CreateEndpoint.html) in the *AWS Database Migration Service API Reference*\.
+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)