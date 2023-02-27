# AWS::DataBrew::Job<a name="aws-resource-databrew-job"></a>

Specifies a new DataBrew job\.

## Syntax<a name="aws-resource-databrew-job-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-databrew-job-syntax.json"></a>

```
{
  "Type" : "AWS::DataBrew::Job",
  "Properties" : {
      "[DatabaseOutputs](#cfn-databrew-job-databaseoutputs)" : [ DatabaseOutput, ... ],
      "[DataCatalogOutputs](#cfn-databrew-job-datacatalogoutputs)" : [ DataCatalogOutput, ... ],
      "[DatasetName](#cfn-databrew-job-datasetname)" : String,
      "[EncryptionKeyArn](#cfn-databrew-job-encryptionkeyarn)" : String,
      "[EncryptionMode](#cfn-databrew-job-encryptionmode)" : String,
      "[JobSample](#cfn-databrew-job-jobsample)" : JobSample,
      "[LogSubscription](#cfn-databrew-job-logsubscription)" : String,
      "[MaxCapacity](#cfn-databrew-job-maxcapacity)" : Integer,
      "[MaxRetries](#cfn-databrew-job-maxretries)" : Integer,
      "[Name](#cfn-databrew-job-name)" : String,
      "[OutputLocation](#cfn-databrew-job-outputlocation)" : OutputLocation,
      "[Outputs](#cfn-databrew-job-outputs)" : [ Output, ... ],
      "[ProfileConfiguration](#cfn-databrew-job-profileconfiguration)" : ProfileConfiguration,
      "[ProjectName](#cfn-databrew-job-projectname)" : String,
      "[Recipe](#cfn-databrew-job-recipe)" : Recipe,
      "[RoleArn](#cfn-databrew-job-rolearn)" : String,
      "[Tags](#cfn-databrew-job-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Timeout](#cfn-databrew-job-timeout)" : Integer,
      "[Type](#cfn-databrew-job-type)" : String,
      "[ValidationConfigurations](#cfn-databrew-job-validationconfigurations)" : [ ValidationConfiguration, ... ]
    }
}
```

### YAML<a name="aws-resource-databrew-job-syntax.yaml"></a>

```
Type: AWS::DataBrew::Job
Properties: 
  [DatabaseOutputs](#cfn-databrew-job-databaseoutputs): 
    - DatabaseOutput
  [DataCatalogOutputs](#cfn-databrew-job-datacatalogoutputs): 
    - DataCatalogOutput
  [DatasetName](#cfn-databrew-job-datasetname): String
  [EncryptionKeyArn](#cfn-databrew-job-encryptionkeyarn): String
  [EncryptionMode](#cfn-databrew-job-encryptionmode): String
  [JobSample](#cfn-databrew-job-jobsample): 
    JobSample
  [LogSubscription](#cfn-databrew-job-logsubscription): String
  [MaxCapacity](#cfn-databrew-job-maxcapacity): Integer
  [MaxRetries](#cfn-databrew-job-maxretries): Integer
  [Name](#cfn-databrew-job-name): String
  [OutputLocation](#cfn-databrew-job-outputlocation): 
    OutputLocation
  [Outputs](#cfn-databrew-job-outputs): 
    - Output
  [ProfileConfiguration](#cfn-databrew-job-profileconfiguration): 
    ProfileConfiguration
  [ProjectName](#cfn-databrew-job-projectname): String
  [Recipe](#cfn-databrew-job-recipe): 
    Recipe
  [RoleArn](#cfn-databrew-job-rolearn): String
  [Tags](#cfn-databrew-job-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Timeout](#cfn-databrew-job-timeout): Integer
  [Type](#cfn-databrew-job-type): String
  [ValidationConfigurations](#cfn-databrew-job-validationconfigurations): 
    - ValidationConfiguration
```

## Properties<a name="aws-resource-databrew-job-properties"></a>

`DatabaseOutputs`  <a name="cfn-databrew-job-databaseoutputs"></a>
Represents a list of JDBC database output objects which defines the output destination for a DataBrew recipe job to write into\.  
*Required*: No  
*Type*: List of [DatabaseOutput](aws-properties-databrew-job-databaseoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataCatalogOutputs`  <a name="cfn-databrew-job-datacatalogoutputs"></a>
One or more artifacts that represent the AWS Glue Data Catalog output from running the job\.  
*Required*: No  
*Type*: List of [DataCatalogOutput](aws-properties-databrew-job-datacatalogoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetName`  <a name="cfn-databrew-job-datasetname"></a>
A dataset that the job is to process\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionKeyArn`  <a name="cfn-databrew-job-encryptionkeyarn"></a>
The Amazon Resource Name \(ARN\) of an encryption key that is used to protect the job output\. For more information, see [Encrypting data written by DataBrew jobs](https://docs.aws.amazon.com/databrew/latest/dg/encryption-security-configuration.html)   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionMode`  <a name="cfn-databrew-job-encryptionmode"></a>
The encryption mode for the job, which can be one of the following:  
+  `SSE-KMS` \- Server\-side encryption with keys managed by AWS KMS\.
+  `SSE-S3` \- Server\-side encryption with keys managed by Amazon S3\.
*Required*: No  
*Type*: String  
*Allowed values*: `SSE-KMS | SSE-S3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobSample`  <a name="cfn-databrew-job-jobsample"></a>
A sample configuration for profile jobs only, which determines the number of rows on which the profile job is run\. If a `JobSample` value isn't provided, the default value is used\. The default value is CUSTOM\_ROWS for the mode parameter and 20,000 for the size parameter\.  
*Required*: No  
*Type*: [JobSample](aws-properties-databrew-job-jobsample.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogSubscription`  <a name="cfn-databrew-job-logsubscription"></a>
The current status of Amazon CloudWatch logging for the job\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLE | ENABLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCapacity`  <a name="cfn-databrew-job-maxcapacity"></a>
The maximum number of nodes that can be consumed when the job processes data\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetries`  <a name="cfn-databrew-job-maxretries"></a>
The maximum number of times to retry the job after a job run fails\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-databrew-job-name"></a>
The unique name of the job\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `240`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutputLocation`  <a name="cfn-databrew-job-outputlocation"></a>
Property description not available\.  
*Required*: No  
*Type*: [OutputLocation](aws-properties-databrew-job-outputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Outputs`  <a name="cfn-databrew-job-outputs"></a>
One or more artifacts that represent output from running the job\.  
*Required*: No  
*Type*: List of [Output](aws-properties-databrew-job-output.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProfileConfiguration`  <a name="cfn-databrew-job-profileconfiguration"></a>
Configuration for profile jobs\. Configuration can be used to select columns, do evaluations, and override default parameters of evaluations\. When configuration is undefined, the profile job will apply default settings to all supported columns\.   
*Required*: No  
*Type*: [ProfileConfiguration](aws-properties-databrew-job-profileconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProjectName`  <a name="cfn-databrew-job-projectname"></a>
The name of the project that the job is associated with\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Recipe`  <a name="cfn-databrew-job-recipe"></a>
A series of data transformation steps that the job runs\.  
*Required*: No  
*Type*: [Recipe](aws-properties-databrew-job-recipe.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-databrew-job-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role to be assumed for this job\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-databrew-job-tags"></a>
Metadata tags that have been applied to the job\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Timeout`  <a name="cfn-databrew-job-timeout"></a>
The job's timeout in minutes\. A job that attempts to run longer than this timeout period ends with a status of `TIMEOUT`\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-databrew-job-type"></a>
The job type of the job, which must be one of the following:  
+  `PROFILE` \- A job to analyze a dataset, to determine its size, data types, data distribution, and more\.
+  `RECIPE` \- A job to apply one or more transformations to a dataset\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `PROFILE | RECIPE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidationConfigurations`  <a name="cfn-databrew-job-validationconfigurations"></a>
List of validation configurations that are applied to the profile job\.  
*Required*: No  
*Type*: List of [ValidationConfiguration](aws-properties-databrew-job-validationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-databrew-job-return-values"></a>

### Ref<a name="aws-resource-databrew-job-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myJob" }` 

For an AWS Glue DataBrew job named `myJob`, `Ref` returns the name of the job\. 

## Examples<a name="aws-resource-databrew-job--examples"></a>



### Creating jobs<a name="aws-resource-databrew-job--examples--Creating_jobs"></a>

The following examples create new DataBrew profile jobs\.

#### YAML<a name="aws-resource-databrew-job--examples--Creating_jobs--yaml"></a>

```
Resources:
  TestDataBrewJob:
    Type: AWS::DataBrew::Job
    Properties:
      Type: PROFILE
      Name: job-name
      DatasetName: dataset-name
      RoleArn: arn:aws:iam::12345678910:role/PassRoleAdmin
      JobSample:
        Mode: 'CUSTOM_ROWS'
        Size: 50000
      OutputLocation:
        Bucket: !Join [ '', ['databrew-cfn-integration-tests-', !Ref 'AWS::Region', '-', !Ref 'AWS::AccountId' ] ]
      Tags: [{Key: key00AtCreate, Value: value001AtCreate}]
```

#### JSON<a name="aws-resource-databrew-job--examples--Creating_jobs--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "This CloudFormation template specifies a DataBrew Profile Job",
    "Resources": {
        "MyDataBrewProfileJob": {
            "Type": "AWS::DataBrew::Job",
            "Properties": {
                "Type": "PROFILE",
                "Name": "job-test",
                "DatasetName": "dataset-test",
                "RoleArn": "arn:aws:iam::1234567891011:role/PassRoleAdmin",
                "JobSample": {
                    "Mode": "FULL_DATASET"
                },
                "OutputLocation": {
                    "Bucket": "test-output",
                    "Key": "job-output.json"
                },
                "Tags": [
                    {
                        "Key": "key00AtCreate",
                        "Value": "value001AtCreate"
                    }
                ]
            }
        }
    }
}
```