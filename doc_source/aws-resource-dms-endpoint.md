# AWS::DMS::Endpoint<a name="aws-resource-dms-endpoint"></a>

The `AWS::DMS::Endpoint` resource creates an AWS DMS endpoint\.

Currently, the only endpoint setting types that AWS CloudFormation supports are **DynamoDBSettings**, **ElasticSearchSettings**, and **NeptuneSettings**\.

## Syntax<a name="aws-resource-dms-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-endpoint-syntax.json"></a>

```
{
  "Type" : "AWS::DMS::Endpoint",
  "Properties" : {
      "[CertificateArn](#cfn-dms-endpoint-certificatearn)" : String,
      "[DatabaseName](#cfn-dms-endpoint-databasename)" : String,
      "[DocDbSettings](#cfn-dms-endpoint-docdbsettings)" : DocDbSettings,
      "[DynamoDbSettings](#cfn-dms-endpoint-dynamodbsettings)" : DynamoDbSettings,
      "[ElasticsearchSettings](#cfn-dms-endpoint-elasticsearchsettings)" : ElasticsearchSettings,
      "[EndpointIdentifier](#cfn-dms-endpoint-endpointidentifier)" : String,
      "[EndpointType](#cfn-dms-endpoint-endpointtype)" : String,
      "[EngineName](#cfn-dms-endpoint-enginename)" : String,
      "[ExtraConnectionAttributes](#cfn-dms-endpoint-extraconnectionattributes)" : String,
      "[IbmDb2Settings](#cfn-dms-endpoint-ibmdb2settings)" : IbmDb2Settings,
      "[KafkaSettings](#cfn-dms-endpoint-kafkasettings)" : KafkaSettings,
      "[KinesisSettings](#cfn-dms-endpoint-kinesissettings)" : KinesisSettings,
      "[KmsKeyId](#cfn-dms-endpoint-kmskeyid)" : String,
      "[MicrosoftSqlServerSettings](#cfn-dms-endpoint-microsoftsqlserversettings)" : MicrosoftSqlServerSettings,
      "[MongoDbSettings](#cfn-dms-endpoint-mongodbsettings)" : MongoDbSettings,
      "[MySqlSettings](#cfn-dms-endpoint-mysqlsettings)" : MySqlSettings,
      "[NeptuneSettings](#cfn-dms-endpoint-neptunesettings)" : NeptuneSettings,
      "[OracleSettings](#cfn-dms-endpoint-oraclesettings)" : OracleSettings,
      "[Password](#cfn-dms-endpoint-password)" : String,
      "[Port](#cfn-dms-endpoint-port)" : Integer,
      "[PostgreSqlSettings](#cfn-dms-endpoint-postgresqlsettings)" : PostgreSqlSettings,
      "[RedshiftSettings](#cfn-dms-endpoint-redshiftsettings)" : RedshiftSettings,
      "[S3Settings](#cfn-dms-endpoint-s3settings)" : S3Settings,
      "[ServerName](#cfn-dms-endpoint-servername)" : String,
      "[SslMode](#cfn-dms-endpoint-sslmode)" : String,
      "[SybaseSettings](#cfn-dms-endpoint-sybasesettings)" : SybaseSettings,
      "[Tags](#cfn-dms-endpoint-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Username](#cfn-dms-endpoint-username)" : String
    }
}
```

### YAML<a name="aws-resource-dms-endpoint-syntax.yaml"></a>

```
Type: AWS::DMS::Endpoint
Properties: 
  [CertificateArn](#cfn-dms-endpoint-certificatearn): String
  [DatabaseName](#cfn-dms-endpoint-databasename): String
  [DocDbSettings](#cfn-dms-endpoint-docdbsettings): 
    DocDbSettings
  [DynamoDbSettings](#cfn-dms-endpoint-dynamodbsettings): 
    DynamoDbSettings
  [ElasticsearchSettings](#cfn-dms-endpoint-elasticsearchsettings): 
    ElasticsearchSettings
  [EndpointIdentifier](#cfn-dms-endpoint-endpointidentifier): String
  [EndpointType](#cfn-dms-endpoint-endpointtype): String
  [EngineName](#cfn-dms-endpoint-enginename): String
  [ExtraConnectionAttributes](#cfn-dms-endpoint-extraconnectionattributes): String
  [IbmDb2Settings](#cfn-dms-endpoint-ibmdb2settings): 
    IbmDb2Settings
  [KafkaSettings](#cfn-dms-endpoint-kafkasettings): 
    KafkaSettings
  [KinesisSettings](#cfn-dms-endpoint-kinesissettings): 
    KinesisSettings
  [KmsKeyId](#cfn-dms-endpoint-kmskeyid): String
  [MicrosoftSqlServerSettings](#cfn-dms-endpoint-microsoftsqlserversettings): 
    MicrosoftSqlServerSettings
  [MongoDbSettings](#cfn-dms-endpoint-mongodbsettings): 
    MongoDbSettings
  [MySqlSettings](#cfn-dms-endpoint-mysqlsettings): 
    MySqlSettings
  [NeptuneSettings](#cfn-dms-endpoint-neptunesettings): 
    NeptuneSettings
  [OracleSettings](#cfn-dms-endpoint-oraclesettings): 
    OracleSettings
  [Password](#cfn-dms-endpoint-password): String
  [Port](#cfn-dms-endpoint-port): Integer
  [PostgreSqlSettings](#cfn-dms-endpoint-postgresqlsettings): 
    PostgreSqlSettings
  [RedshiftSettings](#cfn-dms-endpoint-redshiftsettings): 
    RedshiftSettings
  [S3Settings](#cfn-dms-endpoint-s3settings): 
    S3Settings
  [ServerName](#cfn-dms-endpoint-servername): String
  [SslMode](#cfn-dms-endpoint-sslmode): String
  [SybaseSettings](#cfn-dms-endpoint-sybasesettings): 
    SybaseSettings
  [Tags](#cfn-dms-endpoint-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Username](#cfn-dms-endpoint-username): String
```

## Properties<a name="aws-resource-dms-endpoint-properties"></a>

`CertificateArn`  <a name="cfn-dms-endpoint-certificatearn"></a>
The Amazon Resource Name \(ARN\) for the certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-dms-endpoint-databasename"></a>
The name of the endpoint database\. For a MySQL source or target endpoint, do not specify DatabaseName\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocDbSettings`  <a name="cfn-dms-endpoint-docdbsettings"></a>
Settings in JSON format for the source DocumentDB endpoint\. For more information about the available settings, see the configuration properties section in [ Using DocumentDB as a Target for AWS Database Migration Service ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.DocumentDB.html) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [DocDbSettings](aws-properties-dms-endpoint-docdbsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDbSettings`  <a name="cfn-dms-endpoint-dynamodbsettings"></a>
Settings in JSON format for the target Amazon DynamoDB endpoint\. For information about other available settings, see [Using Object Mapping to Migrate Data to DynamoDB](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html#CHAP_Target.DynamoDB.ObjectMapping) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [DynamoDbSettings](aws-properties-dms-endpoint-dynamodbsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticsearchSettings`  <a name="cfn-dms-endpoint-elasticsearchsettings"></a>
Settings in JSON format for the target Elasticsearch endpoint\. For more information about the available settings, see [Extra Connection Attributes When Using Elasticsearch as a Target for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Elasticsearch.html#CHAP_Target.Elasticsearch.Configuration) in the * AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [ElasticsearchSettings](aws-properties-dms-endpoint-elasticsearchsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointIdentifier`  <a name="cfn-dms-endpoint-endpointidentifier"></a>
The database endpoint identifier\. Identifiers must begin with a letter and must contain only ASCII letters, digits, and hyphens\. They can't end with a hyphen, or contain two consecutive hyphens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointType`  <a name="cfn-dms-endpoint-endpointtype"></a>
The type of endpoint\. Valid values are `source` and `target`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `source | target`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineName`  <a name="cfn-dms-endpoint-enginename"></a>
The type of engine for the endpoint\. Valid values, depending on the `EndpointType` value, include `"mysql"`, `"oracle"`, `"postgres"`, `"mariadb"`, `"aurora"`, `"aurora-postgresql"`, `"redshift"`, `"s3"`, `"db2"`, `"azuredb"`, `"sybase"`, `"dynamodb"`, `"mongodb"`, `"kinesis"`, `"kafka"`, `"elasticsearch"`, `"docdb"`, `"sqlserver"`, and `"neptune"`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtraConnectionAttributes`  <a name="cfn-dms-endpoint-extraconnectionattributes"></a>
Additional attributes associated with the connection\. Each attribute is specified as a name\-value pair associated by an equal sign \(=\)\. Multiple attributes are separated by a semicolon \(;\) with no additional white space\. For information on the attributes available for connecting your source or target endpoint, see [Working with AWS DMS Endpoints](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Endpoints.html) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IbmDb2Settings`  <a name="cfn-dms-endpoint-ibmdb2settings"></a>
Not currently supported by AWS CloudFormation\.   
*Required*: No  
*Type*: [IbmDb2Settings](aws-properties-dms-endpoint-ibmdb2settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KafkaSettings`  <a name="cfn-dms-endpoint-kafkasettings"></a>
Settings in JSON format for the target Apache Kafka endpoint\. For more information about the available settings, see [Using object mapping to migrate data to a Kafka topic](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kafka.html#CHAP_Target.Kafka.ObjectMapping) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [KafkaSettings](aws-properties-dms-endpoint-kafkasettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisSettings`  <a name="cfn-dms-endpoint-kinesissettings"></a>
Settings in JSON format for the target endpoint for Amazon Kinesis Data Streams\. For more information about the available settings, see [Using Amazon Kinesis Data Streams as a Target for AWS Database Migration Service ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kinesis.html) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [KinesisSettings](aws-properties-dms-endpoint-kinesissettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-dms-endpoint-kmskeyid"></a>
An AWS KMS key identifier that is used to encrypt the connection parameters for the endpoint\.  
If you don't specify a value for the `KmsKeyId` parameter, then AWS DMS uses your default encryption key\.  
 AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MicrosoftSqlServerSettings`  <a name="cfn-dms-endpoint-microsoftsqlserversettings"></a>
Not currently supported by AWS CloudFormation\.   
*Required*: No  
*Type*: [MicrosoftSqlServerSettings](aws-properties-dms-endpoint-microsoftsqlserversettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MongoDbSettings`  <a name="cfn-dms-endpoint-mongodbsettings"></a>
Not currently supported by AWS CloudFormation\.   
*Required*: No  
*Type*: [MongoDbSettings](aws-properties-dms-endpoint-mongodbsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MySqlSettings`  <a name="cfn-dms-endpoint-mysqlsettings"></a>
Settings in JSON format for the source and target MySQL endpoint\. For information about other available settings, see [Extra connection attributes when using MySQL as a source for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MySQL.html#CHAP_Source.MySQL.ConnectionAttrib) and [Extra connection attributes when using a MySQL\-compatible database as a target for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.MySQL.html#CHAP_Target.MySQL.ConnectionAttrib) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [MySqlSettings](aws-properties-dms-endpoint-mysqlsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NeptuneSettings`  <a name="cfn-dms-endpoint-neptunesettings"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [NeptuneSettings](aws-properties-dms-endpoint-neptunesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OracleSettings`  <a name="cfn-dms-endpoint-oraclesettings"></a>
Settings in JSON format for the source and target Oracle endpoint\. For information about other available settings, see [Extra connection attributes when using Oracle as a source for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.ConnectionAttrib) and [ Extra connection attributes when using Oracle as a target for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Oracle.html#CHAP_Target.Oracle.ConnectionAttrib) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [OracleSettings](aws-properties-dms-endpoint-oraclesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-dms-endpoint-password"></a>
The password to be used to log in to the endpoint database\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-dms-endpoint-port"></a>
The port used by the endpoint database\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostgreSqlSettings`  <a name="cfn-dms-endpoint-postgresqlsettings"></a>
Not currently supported by AWS CloudFormation\.   
*Required*: No  
*Type*: [PostgreSqlSettings](aws-properties-dms-endpoint-postgresqlsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedshiftSettings`  <a name="cfn-dms-endpoint-redshiftsettings"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [RedshiftSettings](aws-properties-dms-endpoint-redshiftsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Settings`  <a name="cfn-dms-endpoint-s3settings"></a>
Settings in JSON format for the target Amazon S3 endpoint\. For more information about the available settings, see [Extra Connection Attributes When Using Amazon S3 as a Target for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html#CHAP_Target.S3.Configuring) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [S3Settings](aws-properties-dms-endpoint-s3settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerName`  <a name="cfn-dms-endpoint-servername"></a>
The name of the server where the endpoint database resides\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslMode`  <a name="cfn-dms-endpoint-sslmode"></a>
The Secure Sockets Layer \(SSL\) mode to use for the SSL connection\. The default is `none`\.   
When `engine_name` is set to S3, then the only allowed value is `none`\.
*Required*: No  
*Type*: String  
*Allowed values*: `none | require | verify-ca | verify-full`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SybaseSettings`  <a name="cfn-dms-endpoint-sybasesettings"></a>
Settings in JSON format for the source and target SAP ASE endpoint\. For information about other available settings, see [Extra connection attributes when using SAP ASE as a source for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.SAP.html#CHAP_Source.SAP.ConnectionAttrib) and [Extra connection attributes when using SAP ASE as a target for AWS DMS ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.SAP.html#CHAP_Target.SAP.ConnectionAttrib) in the * AWS Database Migration Service User Guide\.*   
*Required*: No  
*Type*: [SybaseSettings](aws-properties-dms-endpoint-sybasesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-dms-endpoint-tags"></a>
One or more tags to be assigned to the endpoint\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Username`  <a name="cfn-dms-endpoint-username"></a>
The user name to be used to log in to the endpoint database\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dms-endpoint-return-values"></a>

### Ref<a name="aws-resource-dms-endpoint-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the endpoint\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-dms-endpoint-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-dms-endpoint-return-values-fn--getatt-fn--getatt"></a>

`ExternalId`  <a name="ExternalId-fn::getatt"></a>
A value that can be used for cross\-account validation\.

## Examples<a name="aws-resource-dms-endpoint--examples"></a>



### <a name="aws-resource-dms-endpoint--examples--"></a>

#### JSON<a name="aws-resource-dms-endpoint--examples----json"></a>

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

#### YAML<a name="aws-resource-dms-endpoint--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: "Endpoint test"
Resources: 
  BasicEndpoint: 
    Properties: 
      DatabaseName: my-db
      EndpointType: target
      EngineName: mysql
      Password: PasswordParameter
      Port: 1234
      ServerName: server.db.amazon.com
      Tags: 
        - 
          Key: type
          Value: new
      Username: username
    Type: "AWS::DMS::Endpoint"
```

## See also<a name="aws-resource-dms-endpoint--seealso"></a>
+  [CreateEndpoint](https://docs.aws.amazon.com/dms/latest/APIReference/API_CreateEndpoint.html) in the *AWS Database Migration Service API Reference* 
+  [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) 

