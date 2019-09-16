# AWS::DMS::Endpoint MongoDbSettings<a name="aws-properties-dms-endpoint-mongodbsettings"></a>

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
  [ServerName](#cfn-dms-endpoint-mongodbsettings-servername): String
  [Username](#cfn-dms-endpoint-mongodbsettings-username): String
```

## Properties<a name="aws-properties-dms-endpoint-mongodbsettings-properties"></a>

`AuthMechanism`  <a name="cfn-dms-endpoint-mongodbsettings-authmechanism"></a>
 The authentication mechanism you use to access the MongoDB source endpoint\.  
Valid values: DEFAULT, MONGODB\_CR, SCRAM\_SHA\_1   
DEFAULT – For MongoDB version 2\.x, use MONGODB\_CR\. For MongoDB version 3\.x, use SCRAM\_SHA\_1\. This attribute is not used when authType=No\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `default | mongodb_cr | scram_sha_1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthSource`  <a name="cfn-dms-endpoint-mongodbsettings-authsource"></a>
 The MongoDB database name\. This attribute is not used when `authType=NO`\.   
The default is admin\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthType`  <a name="cfn-dms-endpoint-mongodbsettings-authtype"></a>
 The authentication type you use to access the MongoDB source endpoint\.  
Valid values: NO, PASSWORD   
When NO is selected, user name and password parameters are not used and can be empty\.   
*Required*: No  
*Type*: String  
*Allowed Values*: `no | password`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-dms-endpoint-mongodbsettings-databasename"></a>
 The database name on the MongoDB source endpoint\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocsToInvestigate`  <a name="cfn-dms-endpoint-mongodbsettings-docstoinvestigate"></a>
 Indicates the number of documents to preview to determine the document organization\. Use this attribute when `NestingLevel` is set to ONE\.   
Must be a positive value greater than 0\. Default value is 1000\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtractDocId`  <a name="cfn-dms-endpoint-mongodbsettings-extractdocid"></a>
 Specifies the document ID\. Use this attribute when `NestingLevel` is set to NONE\.   
Default value is false\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NestingLevel`  <a name="cfn-dms-endpoint-mongodbsettings-nestinglevel"></a>
 Specifies either document or table mode\.   
Valid values: NONE, ONE  
Default value is NONE\. Specify NONE to use document mode\. Specify ONE to use table mode\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `none | one`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-dms-endpoint-mongodbsettings-password"></a>
 The password for the user account you use to access the MongoDB source endpoint\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-dms-endpoint-mongodbsettings-port"></a>
 The port value for the MongoDB source endpoint\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerName`  <a name="cfn-dms-endpoint-mongodbsettings-servername"></a>
 The name of the server on the MongoDB source endpoint\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-dms-endpoint-mongodbsettings-username"></a>
The user name you use to access the MongoDB source endpoint\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)