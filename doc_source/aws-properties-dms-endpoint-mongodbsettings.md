# AWS DMS Endpoint MongoDbSettings<a name="aws-properties-dms-endpoint-mongodbsettings"></a>

Use the `MongoDbSettings` property to specify settings for a MongoDB endpoint for a [AWS::DMS::Endpoint](aws-resource-dms-endpoint.md) resource\.

## Syntax<a name="w3ab2c21c14d582b5"></a>

### JSON<a name="aws-properties-dms-endpoint-mongodbsettings-syntax.json"></a>

```
{
  "[AuthMechanism](#cfn-dms-endpoint-mongodbsettings-authmechanism)" : String,
  "[AuthSource](#cfn-dms-endpoint-mongodbsettings-authsource)" : String,
  "[DatabaseName](#cfn-dms-endpoint-mongodbsettings-databasename)" : String,
  "[DocsToInvestigate](#cfn-dms-endpoint-mongodbsettings-docstoinvestigate)" : String,
  "[ExtractDocId](#cfn-dms-endpoint-mongodbsettings-extractdocid)" : String,
  "[KmsKeyId](#cfn-dms-endpoint-mongodbsettings-kmskeyid)" : String,
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
[DatabaseName](#cfn-dms-endpoint-mongodbsettings-databasename): String
[DocsToInvestigate](#cfn-dms-endpoint-mongodbsettings-docstoinvestigate): String
[ExtractDocId](#cfn-dms-endpoint-mongodbsettings-extractdocid): String
[KmsKeyId](#cfn-dms-endpoint-mongodbsettings-kmskeyid): String
[NestingLevel](#cfn-dms-endpoint-mongodbsettings-nestinglevel): String
[Password](#cfn-dms-endpoint-mongodbsettings-password): String
[Port](#cfn-dms-endpoint-mongodbsettings-port): String
[ServerName](#cfn-dms-endpoint-mongodbsettings-servername): String
[Username](#cfn-dms-endpoint-mongodbsettings-username): String
```

## Properties<a name="w3ab2c21c14d582b7"></a>

For more information about option settings, see [Using a MongoDB Database as a Source for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html) in the *AWS Database Migration Service User Guide*

`AuthMechanism`  <a name="cfn-dms-endpoint-mongodbsettings-authmechanism"></a>
 The authentication mechanism you use to access the MongoDB source endpoint\.   
Valid values: DEFAULT, MONGODB\_CR, SCRAM\_SHA\_1   
For MongoDB version 2\.x, use MONGODB\_CR\. For MongoDB version 3\.x, use SCRAM\_SHA\_1\. This attribute is not used when `authType=No`\.   
*Required*: No  
*Type*: String

`AuthSource`  <a name="cfn-dms-endpoint-mongodbsettings-authsource"></a>
 The authentication type you use to access the MongoDB source endpoint\.   
Valid values: NO, PASSWORD   
When NO is selected, user name and password parameters are not used and can be empty\.   
*Required*: No  
*Type*: String

`DatabaseName`  <a name="cfn-dms-endpoint-mongodbsettings-databasename"></a>
The database name on the MongoDB source endpoint\.  
*Required*: No  
*Type*: String

`DocsToInvestigate`  <a name="cfn-dms-endpoint-mongodbsettings-docstoinvestigate"></a>
 Indicates the number of documents to preview to determine the document organization\. Use this attribute when `NestingLevel` is set to ONE\.  
Must be a positive value greater than 0\. Default value is 1000\.  
*Required*: No  
*Type*: String

`ExtractDocId`  <a name="cfn-dms-endpoint-mongodbsettings-extractdocid"></a>
 Specifies the document ID\. Use this attribute when `NestingLevel` is set to NONE\. Default value is false\.   
*Required*: No  
*Type*: String

`KmsKeyId`  <a name="cfn-dms-endpoint-mongodbsettings-kmskeyid"></a>
The ID of the KMS key to be used\.  
*Required*: No  
*Type*: String

`NestingLevel`  <a name="cfn-dms-endpoint-mongodbsettings-nestinglevel"></a>
 Specifies either document or table mode\.   
Valid values: NONE, ONE  
Default value is NONE\. Specify NONE to use document mode\. Specify ONE to use table mode\.   
*Required*: No  
*Type*: String

`Password`  <a name="cfn-dms-endpoint-mongodbsettings-password"></a>
 The password for the user account you use to access the MongoDB source endpoint\.  
*Required*: No  
*Type*: String

`Port`  <a name="cfn-dms-endpoint-mongodbsettings-port"></a>
The port value for the MongoDB source endpoint\.  
*Required*: No  
*Type*: Integer

`ServerName`  <a name="cfn-dms-endpoint-mongodbsettings-servername"></a>
The name of the server on the MongoDB source endpoint\.   
*Required*: No  
*Type*: String

`Username`  <a name="cfn-dms-endpoint-mongodbsettings-username"></a>
The user name you use to access the MongoDB source endpoint\.  
*Required*: No  
*Type*: String