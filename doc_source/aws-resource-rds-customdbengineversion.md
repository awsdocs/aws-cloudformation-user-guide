# AWS::RDS::CustomDBEngineVersion<a name="aws-resource-rds-customdbengineversion"></a>

Creates a custom DB engine version \(CEV\)\.

## Syntax<a name="aws-resource-rds-customdbengineversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-customdbengineversion-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::CustomDBEngineVersion",
  "Properties" : {
      "[DatabaseInstallationFilesS3BucketName](#cfn-rds-customdbengineversion-databaseinstallationfiless3bucketname)" : String,
      "[DatabaseInstallationFilesS3Prefix](#cfn-rds-customdbengineversion-databaseinstallationfiless3prefix)" : String,
      "[Description](#cfn-rds-customdbengineversion-description)" : String,
      "[Engine](#cfn-rds-customdbengineversion-engine)" : String,
      "[EngineVersion](#cfn-rds-customdbengineversion-engineversion)" : String,
      "[KMSKeyId](#cfn-rds-customdbengineversion-kmskeyid)" : String,
      "[Manifest](#cfn-rds-customdbengineversion-manifest)" : String,
      "[Status](#cfn-rds-customdbengineversion-status)" : String,
      "[Tags](#cfn-rds-customdbengineversion-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rds-customdbengineversion-syntax.yaml"></a>

```
Type: AWS::RDS::CustomDBEngineVersion
Properties: 
  [DatabaseInstallationFilesS3BucketName](#cfn-rds-customdbengineversion-databaseinstallationfiless3bucketname): String
  [DatabaseInstallationFilesS3Prefix](#cfn-rds-customdbengineversion-databaseinstallationfiless3prefix): String
  [Description](#cfn-rds-customdbengineversion-description): String
  [Engine](#cfn-rds-customdbengineversion-engine): String
  [EngineVersion](#cfn-rds-customdbengineversion-engineversion): String
  [KMSKeyId](#cfn-rds-customdbengineversion-kmskeyid): String
  [Manifest](#cfn-rds-customdbengineversion-manifest): String
  [Status](#cfn-rds-customdbengineversion-status): String
  [Tags](#cfn-rds-customdbengineversion-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rds-customdbengineversion-properties"></a>

`DatabaseInstallationFilesS3BucketName`  <a name="cfn-rds-customdbengineversion-databaseinstallationfiless3bucketname"></a>
The name of an Amazon S3 bucket that contains database installation files for your CEV\. For example, a valid bucket name is `my-custom-installation-files`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseInstallationFilesS3Prefix`  <a name="cfn-rds-customdbengineversion-databaseinstallationfiless3prefix"></a>
The Amazon S3 directory that contains the database installation files for your CEV\. For example, a valid bucket name is `123456789012/cev1`\. If this setting isn't specified, no prefix is assumed\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-rds-customdbengineversion-description"></a>
An optional description of your CEV\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-rds-customdbengineversion-engine"></a>
The database engine to use for your custom engine version \(CEV\)\.  
Valid values:  
+ `custom-oracle-ee`
+ `custom-oracle-ee-cdb`
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-rds-customdbengineversion-engineversion"></a>
The name of your CEV\. The name format is `major version.customized_string`\. For example, a valid CEV name is `19.my_cev1`\. This setting is required for RDS Custom for Oracle, but optional for Amazon RDS\. The combination of `Engine` and `EngineVersion` is unique per customer per Region\.  
*Constraints:* Minimum length is 1\. Maximum length is 60\.  
*Pattern:* `^[a-z0-9_.-]{1,60$`\}  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KMSKeyId`  <a name="cfn-rds-customdbengineversion-kmskeyid"></a>
The AWS KMS key identifier for an encrypted CEV\. A symmetric encryption KMS key is required for RDS Custom, but optional for Amazon RDS\.  
If you have an existing symmetric encryption KMS key in your account, you can use it with RDS Custom\. No further action is necessary\. If you don't already have a symmetric encryption KMS key in your account, follow the instructions in [ Creating a symmetric encryption KMS key](https://docs.aws.amazon.com/kms/latest/developerguide/create-keys.html#create-symmetric-cmk) in the * AWS Key Management Service Developer Guide*\.  
You can choose the same symmetric encryption key when you create a CEV and a DB instance, or choose different keys\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Manifest`  <a name="cfn-rds-customdbengineversion-manifest"></a>
The CEV manifest, which is a JSON document that describes the installation \.zip files stored in Amazon S3\. Specify the name/value pairs in a file or a quoted string\. RDS Custom applies the patches in the order in which they are listed\.  
The following JSON fields are valid:    
MediaImportTemplateVersion  
Version of the CEV manifest\. The date is in the format `YYYY-MM-DD`\.  
databaseInstallationFileNames  
Ordered list of installation files for the CEV\.  
opatchFileNames  
Ordered list of OPatch installers used for the Oracle DB engine\.  
psuRuPatchFileNames  
The PSU and RU patches for this CEV\.  
OtherPatchFileNames  
The patches that are not in the list of PSU and RU patches\. Amazon RDS applies these patches after applying the PSU and RU patches\.
For more information, see [ Creating the CEV manifest](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/custom-cev.html#custom-cev.preparing.manifest) in the *Amazon RDS User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-rds-customdbengineversion-status"></a>
A value that indicates the status of a custom engine version \(CEV\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rds-customdbengineversion-tags"></a>
A list of tags\. For more information, see [Tagging Amazon RDS Resources](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Tagging.html) in the *Amazon RDS User Guide\.*  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-customdbengineversion-return-values"></a>

### Ref<a name="aws-resource-rds-customdbengineversion-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-rds-customdbengineversion-return-values-fn--getatt"></a>

#### <a name="aws-resource-rds-customdbengineversion-return-values-fn--getatt-fn--getatt"></a>

`DBEngineVersionArn`  <a name="DBEngineVersionArn-fn::getatt"></a>
The ARN of the custom engine version\.