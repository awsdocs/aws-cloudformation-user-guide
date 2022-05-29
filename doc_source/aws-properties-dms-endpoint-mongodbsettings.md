# AWS::DMS::Endpoint MongoDbSettings<a name="aws-properties-dms-endpoint-mongodbsettings"></a>

Not currently supported by AWS CloudFormation\.

## Syntax<a name="aws-properties-dms-endpoint-mongodbsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-mongodbsettings-syntax.json"></a>

```
{
  "[AuthMechanism](#cfn-dms-endpoint-mongodbsettings-authmechanism)" : String,
  "[AuthSource](#cfn-dms-endpoint-mongodbsettings-authsource)" : String,
  "[AuthType](#cfn-dms-endpoint-mongodbsettings-authtype)" : String,
  "[DatabaseName](#cfn-dms-endpoint-mongodbsettings-databasename)" : String,
  "[DocsToInvestigate](#cfn-dms-endpoint-mongodbsettings-docstoinvestigate)" : String,
  "[ExtractDocId](#cfn-dms-endpoint-mongodbsettings-extractdocid)" : String,
  "[NestingLevel](#cfn-dms-endpoint-mongodbsettings-nestinglevel)" : String,
  "[Password](#cfn-dms-endpoint-mongodbsettings-password)" : String,
  "[Port](#cfn-dms-endpoint-mongodbsettings-port)" : Integer,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-mongodbsettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-mongodbsettings-secretsmanagersecretid)" : String,
  "[ServerName](#cfn-dms-endpoint-mongodbsettings-servername)" : String,
  "[Username](#cfn-dms-endpoint-mongodbsettings-username)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-mongodbsettings-syntax.yaml"></a>

```
  [AuthMechanism](#cfn-dms-endpoint-mongodbsettings-authmechanism): String
  [AuthSource](#cfn-dms-endpoint-mongodbsettings-authsource): String
  [AuthType](#cfn-dms-endpoint-mongodbsettings-authtype): String
  [DatabaseName](#cfn-dms-endpoint-mongodbsettings-databasename): String
  [DocsToInvestigate](#cfn-dms-endpoint-mongodbsettings-docstoinvestigate): String
  [ExtractDocId](#cfn-dms-endpoint-mongodbsettings-extractdocid): String
  [NestingLevel](#cfn-dms-endpoint-mongodbsettings-nestinglevel): String
  [Password](#cfn-dms-endpoint-mongodbsettings-password): String
  [Port](#cfn-dms-endpoint-mongodbsettings-port): Integer
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-mongodbsettings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-mongodbsettings-secretsmanagersecretid): String
  [ServerName](#cfn-dms-endpoint-mongodbsettings-servername): String
  [Username](#cfn-dms-endpoint-mongodbsettings-username): String
```

## Properties<a name="aws-properties-dms-endpoint-mongodbsettings-properties"></a>

`AuthMechanism`  <a name="cfn-dms-endpoint-mongodbsettings-authmechanism"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Allowed values*: `default | mongodb_cr | scram_sha_1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthSource`  <a name="cfn-dms-endpoint-mongodbsettings-authsource"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthType`  <a name="cfn-dms-endpoint-mongodbsettings-authtype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Allowed values*: `no | password`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-dms-endpoint-mongodbsettings-databasename"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocsToInvestigate`  <a name="cfn-dms-endpoint-mongodbsettings-docstoinvestigate"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtractDocId`  <a name="cfn-dms-endpoint-mongodbsettings-extractdocid"></a>
Not currently supported by AWS CloudFormation\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NestingLevel`  <a name="cfn-dms-endpoint-mongodbsettings-nestinglevel"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Allowed values*: `none | one`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-dms-endpoint-mongodbsettings-password"></a>
Not currently supported by AWS CloudFormation\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-dms-endpoint-mongodbsettings-port"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-mongodbsettings-secretsmanageraccessrolearn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-mongodbsettings-secretsmanagersecretid"></a>
Not currently supported by AWS CloudFormation\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerName`  <a name="cfn-dms-endpoint-mongodbsettings-servername"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-dms-endpoint-mongodbsettings-username"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)