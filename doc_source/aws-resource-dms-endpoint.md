# AWS::DMS::Endpoint<a name="aws-resource-dms-endpoint"></a>

The `AWS::DMS::Endpoint` resource specifies an AWS DMS endpoint\.

Currently, AWS CloudFormation supports all AWS DMS endpoint types\.

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
      "[GcpMySQLSettings](#cfn-dms-endpoint-gcpmysqlsettings)" : GcpMySQLSettings,
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
      "[RedisSettings](#cfn-dms-endpoint-redissettings)" : RedisSettings,
      "[RedshiftSettings](#cfn-dms-endpoint-redshiftsettings)" : RedshiftSettings,
      "[ResourceIdentifier](#cfn-dms-endpoint-resourceidentifier)" : String,
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
  [GcpMySQLSettings](#cfn-dms-endpoint-gcpmysqlsettings): 
    GcpMySQLSettings
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
  [RedisSettings](#cfn-dms-endpoint-redissettings): 
    RedisSettings
  [RedshiftSettings](#cfn-dms-endpoint-redshiftsettings): 
    RedshiftSettings
  [ResourceIdentifier](#cfn-dms-endpoint-resourceidentifier): String
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
The name of the endpoint database\. For a MySQL source or target endpoint, don't specify `DatabaseName`\. To migrate to a specific database, use this setting and `targetDbType`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocDbSettings`  <a name="cfn-dms-endpoint-docdbsettings"></a>
Settings in JSON format for the source and target DocumentDB endpoint\. For more information about other available settings, see [ Using extra connections attributes with Amazon DocumentDB as a source](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.DocumentDB.html#CHAP_Source.DocumentDB.ECAs) and [ Using Amazon DocumentDB as a target for AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DocumentDB.html) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [DocDbSettings](aws-properties-dms-endpoint-docdbsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDbSettings`  <a name="cfn-dms-endpoint-dynamodbsettings"></a>
Settings in JSON format for the target Amazon DynamoDB endpoint\. For information about other available settings, see [ Using object mapping to migrate data to DynamoDB](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html#CHAP_Target.DynamoDB.ObjectMapping) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [DynamoDbSettings](aws-properties-dms-endpoint-dynamodbsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticsearchSettings`  <a name="cfn-dms-endpoint-elasticsearchsettings"></a>
Settings in JSON format for the target OpenSearch endpoint\. For more information about the available settings, see [ Extra connection attributes when using OpenSearch as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Elasticsearch.html#CHAP_Target.Elasticsearch.Configuration) in the *AWS Database Migration Service User Guide*\.  
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
The type of engine for the endpoint, depending on the `EndpointType` value\.  
*Valid values*: `mysql` \| `oracle` \| `postgres` \| `mariadb` \| `aurora` \| `aurora-postgresql` \| `opensearch` \| `redshift` \| `s3` \| `db2` \| `azuredb` \| `sybase` \| `dynamodb` \| `mongodb` \| `kinesis` \| `kafka` \| `elasticsearch` \| `docdb` \| `sqlserver` \| `neptune`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtraConnectionAttributes`  <a name="cfn-dms-endpoint-extraconnectionattributes"></a>
Additional attributes associated with the connection\. Each attribute is specified as a name\-value pair associated by an equal sign \(=\)\. Multiple attributes are separated by a semicolon \(;\) with no additional white space\. For information on the attributes available for connecting your source or target endpoint, see [ Working with AWS DMS Endpoints](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Endpoints.html) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GcpMySQLSettings`  <a name="cfn-dms-endpoint-gcpmysqlsettings"></a>
Settings in JSON format for the source GCP MySQL endpoint\. These settings are much the same as the settings for any MySQL\-compatible endpoint\. For more information, see [ Extra connection attributes when using MySQL as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MySQL.html#CHAP_Source.MySQL.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [GcpMySQLSettings](aws-properties-dms-endpoint-gcpmysqlsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IbmDb2Settings`  <a name="cfn-dms-endpoint-ibmdb2settings"></a>
Settings in JSON format for the source IBM Db2 LUW endpoint\. For information about other available settings, see [ Extra connection attributes when using Db2 LUW as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.DB2.html#CHAP_Source.DB2.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [IbmDb2Settings](aws-properties-dms-endpoint-ibmdb2settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KafkaSettings`  <a name="cfn-dms-endpoint-kafkasettings"></a>
Settings in JSON format for the target Apache Kafka endpoint\. For more information about other available settings, see [ Using object mapping to migrate data to a Kafka topic](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kafka.html#CHAP_Target.Kafka.ObjectMapping) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [KafkaSettings](aws-properties-dms-endpoint-kafkasettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisSettings`  <a name="cfn-dms-endpoint-kinesissettings"></a>
Settings in JSON format for the target endpoint for Amazon Kinesis Data Streams\. For more information about other available settings, see [ Using object mapping to migrate data to a Kinesis data stream](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kinesis.html#CHAP_Target.Kinesis.ObjectMapping) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [KinesisSettings](aws-properties-dms-endpoint-kinesissettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-dms-endpoint-kmskeyid"></a>
An AWS KMS key identifier that is used to encrypt the connection parameters for the endpoint\.  
If you don't specify a value for the `KmsKeyId` parameter, AWS DMS uses your default encryption key\.  
AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MicrosoftSqlServerSettings`  <a name="cfn-dms-endpoint-microsoftsqlserversettings"></a>
Settings in JSON format for the source and target Microsoft SQL Server endpoint\. For information about other available settings, see [ Extra connection attributes when using SQL Server as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.SQLServer.html#CHAP_Source.SQLServer.ConnectionAttrib) and [ Extra connection attributes when using SQL Server as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.SQLServer.html#CHAP_Target.SQLServer.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [MicrosoftSqlServerSettings](aws-properties-dms-endpoint-microsoftsqlserversettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MongoDbSettings`  <a name="cfn-dms-endpoint-mongodbsettings"></a>
Settings in JSON format for the source MongoDB endpoint\. For more information about the available settings, see [ Using MongoDB as a target for AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html#CHAP_Source.MongoDB.Configuration) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [MongoDbSettings](aws-properties-dms-endpoint-mongodbsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MySqlSettings`  <a name="cfn-dms-endpoint-mysqlsettings"></a>
Settings in JSON format for the source and target MySQL endpoint\. For information about other available settings, see [ Extra connection attributes when using MySQL as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MySQL.html#CHAP_Source.MySQL.ConnectionAttrib) and [ Extra connection attributes when using a MySQL\-compatible database as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.MySQL.html#CHAP_Target.MySQL.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [MySqlSettings](aws-properties-dms-endpoint-mysqlsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NeptuneSettings`  <a name="cfn-dms-endpoint-neptunesettings"></a>
Settings in JSON format for the target Amazon Neptune endpoint\. For more information about the available settings, see [ Specifying endpoint settings for Amazon Neptune as a target](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Neptune.html#CHAP_Target.Neptune.EndpointSettings) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [NeptuneSettings](aws-properties-dms-endpoint-neptunesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OracleSettings`  <a name="cfn-dms-endpoint-oraclesettings"></a>
Settings in JSON format for the source and target Oracle endpoint\. For information about other available settings, see [ Extra connection attributes when using Oracle as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.ConnectionAttrib) and [ Extra connection attributes when using Oracle as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Oracle.html#CHAP_Target.Oracle.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
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
Settings in JSON format for the source and target PostgreSQL endpoint\.  
For information about other available settings, see [ Extra connection attributes when using PostgreSQL as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.PostgreSQL.html#CHAP_Source.PostgreSQL.ConnectionAttrib) and [ Extra connection attributes when using PostgreSQL as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.PostgreSQL.html#CHAP_Target.PostgreSQL.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [PostgreSqlSettings](aws-properties-dms-endpoint-postgresqlsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedisSettings`  <a name="cfn-dms-endpoint-redissettings"></a>
Settings in JSON format for the target Redis endpoint\. For information about other available settings, see [ Specifying endpoint settings for Redis as a target](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Redis.html#CHAP_Target.Redis.EndpointSettings) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [RedisSettings](aws-properties-dms-endpoint-redissettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedshiftSettings`  <a name="cfn-dms-endpoint-redshiftsettings"></a>
Settings in JSON format for the Amazon Redshift endpoint\.  
For more information about other available settings, see [ Extra connection attributes when using Amazon Redshift as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Redshift.html#CHAP_Target.Redshift.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [RedshiftSettings](aws-properties-dms-endpoint-redshiftsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceIdentifier`  <a name="cfn-dms-endpoint-resourceidentifier"></a>
A display name for the resource identifier at the end of the `EndpointArn` response parameter that is returned in the created `Endpoint` object\. The value for this parameter can have up to 31 characters\. It can contain only ASCII letters, digits, and hyphen \('\-'\)\. Also, it can't end with a hyphen or contain two consecutive hyphens, and can only begin with a letter, such as `Example-App-ARN1`\.   
For example, this value might result in the `EndpointArn` value `arn:aws:dms:eu-west-1:012345678901:rep:Example-App-ARN1`\. If you don't specify a `ResourceIdentifier` value, AWS DMS generates a default identifier value for the end of `EndpointArn`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Settings`  <a name="cfn-dms-endpoint-s3settings"></a>
Settings in JSON format for the source and target Amazon S3 endpoint\. For more information about other available settings, see [ Extra connection attributes when using Amazon S3 as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.S3.html#CHAP_Source.S3.Configuring) and [ Extra connection attributes when using Amazon S3 as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html#CHAP_Target.S3.Configuring) in the*AWS Database Migration Service User Guide*\.  
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
When `engine_name` is set to S3, the only allowed value is `none`\.
*Required*: No  
*Type*: String  
*Allowed values*: `none | require | verify-ca | verify-full`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SybaseSettings`  <a name="cfn-dms-endpoint-sybasesettings"></a>
Settings in JSON format for the source and target SAP ASE endpoint\. For information about other available settings, see [ Extra connection attributes when using SAP ASE as a source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.SAP.html#CHAP_Source.SAP.ConnectionAttrib) and [ Extra connection attributes when using SAP ASE as a target for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.SAP.html#CHAP_Target.SAP.ConnectionAttrib) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: [SybaseSettings](aws-properties-dms-endpoint-sybasesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-dms-endpoint-tags"></a>
One or more tags to be assigned to the endpoint\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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
+  [ CreateEndpoint](https://docs.aws.amazon.com/dms/latest/APIReference/API_CreateEndpoint.html) in the *AWS Database Migration Service API Reference*
+  [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)

