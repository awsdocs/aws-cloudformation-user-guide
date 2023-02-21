# AWS::DMS::Endpoint DocDbSettings<a name="aws-properties-dms-endpoint-docdbsettings"></a>

Provides information that defines a DocumentDB endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For more information about other available settings, see [ Using extra connections attributes with Amazon DocumentDB as a source](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.DocumentDB.html#CHAP_Source.DocumentDB.ECAs) and [ Using Amazon DocumentDB as a target for AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DocumentDB.html) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-docdbsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-docdbsettings-syntax.json"></a>

```
{
  "[DocsToInvestigate](#cfn-dms-endpoint-docdbsettings-docstoinvestigate)" : Integer,
  "[ExtractDocId](#cfn-dms-endpoint-docdbsettings-extractdocid)" : Boolean,
  "[NestingLevel](#cfn-dms-endpoint-docdbsettings-nestinglevel)" : String,
  "[SecretsManagerAccessRoleArn](#cfn-dms-endpoint-docdbsettings-secretsmanageraccessrolearn)" : String,
  "[SecretsManagerSecretId](#cfn-dms-endpoint-docdbsettings-secretsmanagersecretid)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-docdbsettings-syntax.yaml"></a>

```
  [DocsToInvestigate](#cfn-dms-endpoint-docdbsettings-docstoinvestigate): Integer
  [ExtractDocId](#cfn-dms-endpoint-docdbsettings-extractdocid): Boolean
  [NestingLevel](#cfn-dms-endpoint-docdbsettings-nestinglevel): String
  [SecretsManagerAccessRoleArn](#cfn-dms-endpoint-docdbsettings-secretsmanageraccessrolearn): String
  [SecretsManagerSecretId](#cfn-dms-endpoint-docdbsettings-secretsmanagersecretid): String
```

## Properties<a name="aws-properties-dms-endpoint-docdbsettings-properties"></a>

`DocsToInvestigate`  <a name="cfn-dms-endpoint-docdbsettings-docstoinvestigate"></a>
 Indicates the number of documents to preview to determine the document organization\. Use this setting when `NestingLevel` is set to `"one"`\.   
Must be a positive value greater than `0`\. Default value is `1000`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtractDocId`  <a name="cfn-dms-endpoint-docdbsettings-extractdocid"></a>
 Specifies the document ID\. Use this setting when `NestingLevel` is set to `"none"`\.   
Default value is `"false"`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NestingLevel`  <a name="cfn-dms-endpoint-docdbsettings-nestinglevel"></a>
 Specifies either document or table mode\.   
Default value is `"none"`\. Specify `"none"` to use document mode\. Specify `"one"` to use table mode\.  
*Required*: No  
*Type*: String  
*Allowed values*: `none | one`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerAccessRoleArn`  <a name="cfn-dms-endpoint-docdbsettings-secretsmanageraccessrolearn"></a>
The full Amazon Resource Name \(ARN\) of the IAM role that specifies AWS DMS as the trusted entity and grants the required permissions to access the value in `SecretsManagerSecret`\. The role must allow the `iam:PassRole` action\. `SecretsManagerSecret` has the value of the AWS Secrets Manager secret that allows access to the DocumentDB endpoint\.  
You can specify one of two sets of values for these permissions\. You can specify the values for this setting and `SecretsManagerSecretId`\. Or you can specify clear\-text values for `UserName`, `Password`, `ServerName`, and `Port`\. You can't specify both\.  
For more information on creating this `SecretsManagerSecret`, the corresponding `SecretsManagerAccessRoleArn`, and the `SecretsManagerSecretId` that is required to access it, see [ Using secrets to access AWS Database Migration Service resources](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.html#security-iam-secretsmanager) in the *AWS Database Migration Service User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsManagerSecretId`  <a name="cfn-dms-endpoint-docdbsettings-secretsmanagersecretid"></a>
The full ARN, partial ARN, or display name of the `SecretsManagerSecret` that contains the DocumentDB endpoint connection details\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)