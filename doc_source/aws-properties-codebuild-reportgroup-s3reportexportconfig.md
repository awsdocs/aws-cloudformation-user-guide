# AWS::CodeBuild::ReportGroup S3ReportExportConfig<a name="aws-properties-codebuild-reportgroup-s3reportexportconfig"></a>

 Information about the S3 bucket where the raw data of a report are exported\. 

## Syntax<a name="aws-properties-codebuild-reportgroup-s3reportexportconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-reportgroup-s3reportexportconfig-syntax.json"></a>

```
{
  "[Bucket](#cfn-codebuild-reportgroup-s3reportexportconfig-bucket)" : String,
  "[EncryptionDisabled](#cfn-codebuild-reportgroup-s3reportexportconfig-encryptiondisabled)" : Boolean,
  "[EncryptionKey](#cfn-codebuild-reportgroup-s3reportexportconfig-encryptionkey)" : String,
  "[Packaging](#cfn-codebuild-reportgroup-s3reportexportconfig-packaging)" : String,
  "[Path](#cfn-codebuild-reportgroup-s3reportexportconfig-path)" : String
}
```

### YAML<a name="aws-properties-codebuild-reportgroup-s3reportexportconfig-syntax.yaml"></a>

```
  [Bucket](#cfn-codebuild-reportgroup-s3reportexportconfig-bucket): String
  [EncryptionDisabled](#cfn-codebuild-reportgroup-s3reportexportconfig-encryptiondisabled): Boolean
  [EncryptionKey](#cfn-codebuild-reportgroup-s3reportexportconfig-encryptionkey): String
  [Packaging](#cfn-codebuild-reportgroup-s3reportexportconfig-packaging): String
  [Path](#cfn-codebuild-reportgroup-s3reportexportconfig-path): String
```

## Properties<a name="aws-properties-codebuild-reportgroup-s3reportexportconfig-properties"></a>

`Bucket`  <a name="cfn-codebuild-reportgroup-s3reportexportconfig-bucket"></a>
 The name of the S3 bucket where the raw data of a report are exported\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionDisabled`  <a name="cfn-codebuild-reportgroup-s3reportexportconfig-encryptiondisabled"></a>
 A boolean value that specifies if the results of a report are encrypted\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionKey`  <a name="cfn-codebuild-reportgroup-s3reportexportconfig-encryptionkey"></a>
 The encryption key for the report's encrypted raw data\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Packaging`  <a name="cfn-codebuild-reportgroup-s3reportexportconfig-packaging"></a>
 The type of build output artifact to create\. Valid values include:   
+  `NONE`: AWS CodeBuild creates the raw data in the output bucket\. This is the default if packaging is not specified\. 
+  `ZIP`: AWS CodeBuild creates a ZIP file with the raw data in the output bucket\. 
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | ZIP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-codebuild-reportgroup-s3reportexportconfig-path"></a>
 The path to the exported report's raw data results\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)