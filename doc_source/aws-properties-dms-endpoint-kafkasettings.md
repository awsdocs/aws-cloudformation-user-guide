# AWS::DMS::Endpoint KafkaSettings<a name="aws-properties-dms-endpoint-kafkasettings"></a>

Provides information that describes an Apache Kafka endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For more information about other available settings, see [ Using object mapping to migrate data to a Kafka topic](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kafka.html#CHAP_Target.Kafka.ObjectMapping) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-kafkasettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-kafkasettings-syntax.json"></a>

```
{
  "[Broker](#cfn-dms-endpoint-kafkasettings-broker)" : String,
  "[IncludeControlDetails](#cfn-dms-endpoint-kafkasettings-includecontroldetails)" : Boolean,
  "[IncludeNullAndEmpty](#cfn-dms-endpoint-kafkasettings-includenullandempty)" : Boolean,
  "[IncludePartitionValue](#cfn-dms-endpoint-kafkasettings-includepartitionvalue)" : Boolean,
  "[IncludeTableAlterOperations](#cfn-dms-endpoint-kafkasettings-includetablealteroperations)" : Boolean,
  "[IncludeTransactionDetails](#cfn-dms-endpoint-kafkasettings-includetransactiondetails)" : Boolean,
  "[MessageFormat](#cfn-dms-endpoint-kafkasettings-messageformat)" : String,
  "[MessageMaxBytes](#cfn-dms-endpoint-kafkasettings-messagemaxbytes)" : Integer,
  "[NoHexPrefix](#cfn-dms-endpoint-kafkasettings-nohexprefix)" : Boolean,
  "[PartitionIncludeSchemaTable](#cfn-dms-endpoint-kafkasettings-partitionincludeschematable)" : Boolean,
  "[SaslPassword](#cfn-dms-endpoint-kafkasettings-saslpassword)" : String,
  "[SaslUserName](#cfn-dms-endpoint-kafkasettings-saslusername)" : String,
  "[SecurityProtocol](#cfn-dms-endpoint-kafkasettings-securityprotocol)" : String,
  "[SslCaCertificateArn](#cfn-dms-endpoint-kafkasettings-sslcacertificatearn)" : String,
  "[SslClientCertificateArn](#cfn-dms-endpoint-kafkasettings-sslclientcertificatearn)" : String,
  "[SslClientKeyArn](#cfn-dms-endpoint-kafkasettings-sslclientkeyarn)" : String,
  "[SslClientKeyPassword](#cfn-dms-endpoint-kafkasettings-sslclientkeypassword)" : String,
  "[Topic](#cfn-dms-endpoint-kafkasettings-topic)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-kafkasettings-syntax.yaml"></a>

```
  [Broker](#cfn-dms-endpoint-kafkasettings-broker): String
  [IncludeControlDetails](#cfn-dms-endpoint-kafkasettings-includecontroldetails): Boolean
  [IncludeNullAndEmpty](#cfn-dms-endpoint-kafkasettings-includenullandempty): Boolean
  [IncludePartitionValue](#cfn-dms-endpoint-kafkasettings-includepartitionvalue): Boolean
  [IncludeTableAlterOperations](#cfn-dms-endpoint-kafkasettings-includetablealteroperations): Boolean
  [IncludeTransactionDetails](#cfn-dms-endpoint-kafkasettings-includetransactiondetails): Boolean
  [MessageFormat](#cfn-dms-endpoint-kafkasettings-messageformat): String
  [MessageMaxBytes](#cfn-dms-endpoint-kafkasettings-messagemaxbytes): Integer
  [NoHexPrefix](#cfn-dms-endpoint-kafkasettings-nohexprefix): Boolean
  [PartitionIncludeSchemaTable](#cfn-dms-endpoint-kafkasettings-partitionincludeschematable): Boolean
  [SaslPassword](#cfn-dms-endpoint-kafkasettings-saslpassword): String
  [SaslUserName](#cfn-dms-endpoint-kafkasettings-saslusername): String
  [SecurityProtocol](#cfn-dms-endpoint-kafkasettings-securityprotocol): String
  [SslCaCertificateArn](#cfn-dms-endpoint-kafkasettings-sslcacertificatearn): String
  [SslClientCertificateArn](#cfn-dms-endpoint-kafkasettings-sslclientcertificatearn): String
  [SslClientKeyArn](#cfn-dms-endpoint-kafkasettings-sslclientkeyarn): String
  [SslClientKeyPassword](#cfn-dms-endpoint-kafkasettings-sslclientkeypassword): String
  [Topic](#cfn-dms-endpoint-kafkasettings-topic): String
```

## Properties<a name="aws-properties-dms-endpoint-kafkasettings-properties"></a>

`Broker`  <a name="cfn-dms-endpoint-kafkasettings-broker"></a>
A comma\-separated list of one or more broker locations in your Kafka cluster that host your Kafka instance\. Specify each broker location in the form `broker-hostname-or-ip:port`\. For example, `"ec2-12-345-678-901.compute-1.amazonaws.com:2345"`\. For more information and examples of specifying a list of broker locations, see [ Using Apache Kafka as a target for AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kafka.html) in the *AWS Database Migration Service User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeControlDetails`  <a name="cfn-dms-endpoint-kafkasettings-includecontroldetails"></a>
Shows detailed control information for table definition, column definition, and table and column changes in the Kafka message output\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeNullAndEmpty`  <a name="cfn-dms-endpoint-kafkasettings-includenullandempty"></a>
Include NULL and empty columns for records migrated to the endpoint\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludePartitionValue`  <a name="cfn-dms-endpoint-kafkasettings-includepartitionvalue"></a>
Shows the partition value within the Kafka message output unless the partition type is `schema-table-type`\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeTableAlterOperations`  <a name="cfn-dms-endpoint-kafkasettings-includetablealteroperations"></a>
Includes any data definition language \(DDL\) operations that change the table in the control data, such as `rename-table`, `drop-table`, `add-column`, `drop-column`, and `rename-column`\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeTransactionDetails`  <a name="cfn-dms-endpoint-kafkasettings-includetransactiondetails"></a>
Provides detailed transaction information from the source database\. This information includes a commit timestamp, a log position, and values for `transaction_id`, previous `transaction_id`, and `transaction_record_id` \(the record offset within a transaction\)\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageFormat`  <a name="cfn-dms-endpoint-kafkasettings-messageformat"></a>
The output format for the records created on the endpoint\. The message format is `JSON` \(default\) or `JSON_UNFORMATTED` \(a single line with no tab\)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `json | json-unformatted`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageMaxBytes`  <a name="cfn-dms-endpoint-kafkasettings-messagemaxbytes"></a>
The maximum size in bytes for records created on the endpoint The default is 1,000,000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoHexPrefix`  <a name="cfn-dms-endpoint-kafkasettings-nohexprefix"></a>
Set this optional parameter to `true` to avoid adding a '0x' prefix to raw data in hexadecimal format\. For example, by default, AWS DMS adds a '0x' prefix to the LOB column type in hexadecimal format moving from an Oracle source to a Kafka target\. Use the `NoHexPrefix` endpoint setting to enable migration of RAW data type columns without adding the '0x' prefix\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PartitionIncludeSchemaTable`  <a name="cfn-dms-endpoint-kafkasettings-partitionincludeschematable"></a>
Prefixes schema and table names to partition values, when the partition type is `primary-key-type`\. Doing this increases data distribution among Kafka partitions\. For example, suppose that a SysBench schema has thousands of tables and each table has only limited range for a primary key\. In this case, the same primary key is sent from thousands of tables to the same partition, which causes throttling\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SaslPassword`  <a name="cfn-dms-endpoint-kafkasettings-saslpassword"></a>
The secure password that you created when you first set up your Amazon MSK cluster to validate a client identity and make an encrypted connection between server and client using SASL\-SSL authentication\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SaslUserName`  <a name="cfn-dms-endpoint-kafkasettings-saslusername"></a>
 The secure user name you created when you first set up your Amazon MSK cluster to validate a client identity and make an encrypted connection between server and client using SASL\-SSL authentication\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityProtocol`  <a name="cfn-dms-endpoint-kafkasettings-securityprotocol"></a>
Set secure connection to a Kafka target endpoint using Transport Layer Security \(TLS\)\. Options include `ssl-encryption`, `ssl-authentication`, and `sasl-ssl`\. `sasl-ssl` requires `SaslUsername` and `SaslPassword`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `plaintext | sasl-ssl | ssl-authentication | ssl-encryption`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslCaCertificateArn`  <a name="cfn-dms-endpoint-kafkasettings-sslcacertificatearn"></a>
 The Amazon Resource Name \(ARN\) for the private certificate authority \(CA\) cert that AWS DMS uses to securely connect to your Kafka target endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslClientCertificateArn`  <a name="cfn-dms-endpoint-kafkasettings-sslclientcertificatearn"></a>
The Amazon Resource Name \(ARN\) of the client certificate used to securely connect to a Kafka target endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslClientKeyArn`  <a name="cfn-dms-endpoint-kafkasettings-sslclientkeyarn"></a>
The Amazon Resource Name \(ARN\) for the client private key used to securely connect to a Kafka target endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslClientKeyPassword`  <a name="cfn-dms-endpoint-kafkasettings-sslclientkeypassword"></a>
 The password for the client private key used to securely connect to a Kafka target endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Topic`  <a name="cfn-dms-endpoint-kafkasettings-topic"></a>
The topic to which you migrate the data\. If you don't specify a topic, AWS DMS specifies `"kafka-default-topic"` as the migration topic\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)