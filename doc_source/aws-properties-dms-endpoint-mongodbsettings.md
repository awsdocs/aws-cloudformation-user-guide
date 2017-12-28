# AWS DMS Endpoint MongoDbSettings<a name="aws-properties-dms-endpoint-mongodbsettings"></a>

Use the `MongoDbSettings` property to specify settings for a MongoDB endpoint for a  resource\.

## Syntax<a name="w3ab2c21c14d500b5"></a>

### JSON<a name="aws-properties-dms-endpoint-mongodbsettings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-authmechanism)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-authsource)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-databasename)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-docstoinvestigate)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-extractdocid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-kmskeyid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-nestinglevel)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-password)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-port)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-servername)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-username)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-mongodbsettings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-authmechanism): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-authsource): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-databasename): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-docstoinvestigate): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-extractdocid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-kmskeyid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-nestinglevel): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-password): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-port): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-servername): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-endpoint-mongodbsettings-username): String
```

## Properties<a name="w3ab2c21c14d500b7"></a>

For more information about option settings, see [Using a MongoDB Database as a Source for AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html) in the *AWS Database Migration Service User Guide*

`AuthMechanism`  
 The authentication mechanism you use to access the MongoDB source endpoint\.   
Valid values: DEFAULT, MONGODB\_CR, SCRAM\_SHA\_1   
For MongoDB version 2\.x, use MONGODB\_CR\. For MongoDB version 3\.x, use SCRAM\_SHA\_1\. This attribute is not used when `authType=No`\.   
*Required: *No  
*Type*: String

`AuthSource`  
 The authentication type you use to access the MongoDB source endpoint\.   
Valid values: NO, PASSWORD   
When NO is selected, user name and password parameters are not used and can be empty\.   
*Required: *No  
*Type*: String

`DatabaseName`  
The database name on the MongoDB source endpoint\.  
*Required: *No  
*Type*: String

`DocsToInvestigate`  
 Indicates the number of documents to preview to determine the document organization\. Use this attribute when `NestingLevel` is set to ONE\.  
Must be a positive value greater than 0\. Default value is 1000\.  
*Required: *No  
*Type*: String

`ExtractDocId`  
 Specifies the document ID\. Use this attribute when `NestingLevel` is set to NONE\. Default value is false\.   
*Required: *No  
*Type*: String

`KmsKeyId`  
The ID of the KMS key to be used\.  
*Required: *No  
*Type*: String

`NestingLevel`  
 Specifies either document or table mode\.   
Valid values: NONE, ONE  
Default value is NONE\. Specify NONE to use document mode\. Specify ONE to use table mode\.   
*Required: *No  
*Type*: String

`Password`  
 The password for the user account you use to access the MongoDB source endpoint\.  
*Required: *No  
*Type*: String

`Port`  
The port value for the MongoDB source endpoint\.  
*Required: *No  
*Type*: Integer

`ServerName`  
The name of the server on the MongoDB source endpoint\.   
*Required: *No  
*Type*: String

`Username`  
The user name you use to access the MongoDB source endpoint\.  
*Required: *No  
*Type*: String