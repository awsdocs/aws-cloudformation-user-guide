# AWS::Kendra::DataSource ConnectionConfiguration<a name="aws-properties-kendra-datasource-connectionconfiguration"></a>

Provides the information necessary to connect to a database\.

## Syntax<a name="aws-properties-kendra-datasource-connectionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-connectionconfiguration-syntax.json"></a>

```
{
  "[DatabaseHost](#cfn-kendra-datasource-connectionconfiguration-databasehost)" : String,
  "[DatabaseName](#cfn-kendra-datasource-connectionconfiguration-databasename)" : String,
  "[DatabasePort](#cfn-kendra-datasource-connectionconfiguration-databaseport)" : Integer,
  "[SecretArn](#cfn-kendra-datasource-connectionconfiguration-secretarn)" : String,
  "[TableName](#cfn-kendra-datasource-connectionconfiguration-tablename)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-connectionconfiguration-syntax.yaml"></a>

```
  [DatabaseHost](#cfn-kendra-datasource-connectionconfiguration-databasehost): String
  [DatabaseName](#cfn-kendra-datasource-connectionconfiguration-databasename): String
  [DatabasePort](#cfn-kendra-datasource-connectionconfiguration-databaseport): Integer
  [SecretArn](#cfn-kendra-datasource-connectionconfiguration-secretarn): String
  [TableName](#cfn-kendra-datasource-connectionconfiguration-tablename): String
```

## Properties<a name="aws-properties-kendra-datasource-connectionconfiguration-properties"></a>

`DatabaseHost`  <a name="cfn-kendra-datasource-connectionconfiguration-databasehost"></a>
The name of the host for the database\. Can be either a string \(host\.subdomain\.domain\.tld\) or an IPv4 or IPv6 address\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-kendra-datasource-connectionconfiguration-databasename"></a>
The name of the database containing the document data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabasePort`  <a name="cfn-kendra-datasource-connectionconfiguration-databaseport"></a>
The port that the database uses for connections\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-connectionconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of credentials stored in AWS Secrets Manager\. The credentials should be a user/password pair\. For more information, see [Using a Database Data Source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-database.html)\. For more information about AWS Secrets Manager, see [ What Is AWS Secrets Manager ](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) in the *AWS Secrets Manager* user guide\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-kendra-datasource-connectionconfiguration-tablename"></a>
The name of the table that contains the document data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)