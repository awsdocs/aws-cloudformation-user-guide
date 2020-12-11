# AWS::DataBrew::Job<a name="aws-resource-databrew-job"></a>

Creates a new DataBrew job\.

## Syntax<a name="aws-resource-databrew-job-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-databrew-job-syntax.json"></a>

```
{
  "Type" : "AWS::DataBrew::Job",
  "Properties" : {
      "[DatasetName](#cfn-databrew-job-datasetname)" : String,
      "[EncryptionKeyArn](#cfn-databrew-job-encryptionkeyarn)" : String,
      "[EncryptionMode](#cfn-databrew-job-encryptionmode)" : String,
      "[LogSubscription](#cfn-databrew-job-logsubscription)" : String,
      "[MaxCapacity](#cfn-databrew-job-maxcapacity)" : Integer,
      "[MaxRetries](#cfn-databrew-job-maxretries)" : Integer,
      "[Name](#cfn-databrew-job-name)" : String,
      "[OutputLocation](#cfn-databrew-job-outputlocation)" : Json,
      "[Outputs](#cfn-databrew-job-outputs)" : [ Output, ... ],
      "[ProjectName](#cfn-databrew-job-projectname)" : String,
      "[Recipe](#cfn-databrew-job-recipe)" : Json,
      "[RoleArn](#cfn-databrew-job-rolearn)" : String,
      "[Tags](#cfn-databrew-job-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Timeout](#cfn-databrew-job-timeout)" : Integer,
      "[Type](#cfn-databrew-job-type)" : String
    }
}
```

### YAML<a name="aws-resource-databrew-job-syntax.yaml"></a>

```
Type: AWS::DataBrew::Job
Properties: 
  [DatasetName](#cfn-databrew-job-datasetname): String
  [EncryptionKeyArn](#cfn-databrew-job-encryptionkeyarn): String
  [EncryptionMode](#cfn-databrew-job-encryptionmode): String
  [LogSubscription](#cfn-databrew-job-logsubscription): String
  [MaxCapacity](#cfn-databrew-job-maxcapacity): Integer
  [MaxRetries](#cfn-databrew-job-maxretries): Integer
  [Name](#cfn-databrew-job-name): String
  [OutputLocation](#cfn-databrew-job-outputlocation): Json
  [Outputs](#cfn-databrew-job-outputs): 
    - Output
  [ProjectName](#cfn-databrew-job-projectname): String
  [Recipe](#cfn-databrew-job-recipe): Json
  [RoleArn](#cfn-databrew-job-rolearn): String
  [Tags](#cfn-databrew-job-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Timeout](#cfn-databrew-job-timeout): Integer
  [Type](#cfn-databrew-job-type): String
```

## Properties<a name="aws-resource-databrew-job-properties"></a>

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
+  `SSE-KMS` \- Server\-side encryption with AWS KMS\-managed keys\.
+  `SSE-S3` \- Server\-side encryption with keys managed by Amazon S3\.
*Required*: No  
*Type*: String  
*Allowed values*: `SSE-KMS | SSE-S3`  
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
The location in Amazon S3 where the job writes its output\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Outputs`  <a name="cfn-databrew-job-outputs"></a>
One or more artifacts that represent output from running the job\.  
*Required*: No  
*Type*: List of [Output](aws-properties-databrew-job-output.md)  
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
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-databrew-job-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that will be assumed for this job\.  
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

## Return values<a name="aws-resource-databrew-job-return-values"></a>

### Ref<a name="aws-resource-databrew-job-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myJob" }` 

For an AWS Glue DataBrew job named `myJob`, `Ref` returns the name of the job\. 

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
      OutputLocation:
        Bucket: !Join [ '', ['databrew-cfn-integration-tests-', !Ref 'AWS::Region', '-', !Ref 'AWS::AccountId' ] ]
      Tags: [{Key: key00AtCreate, Value: value001AtCreate}]
```

#### JSON<a name="aws-resource-databrew-job--examples--Creating_jobs--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "This CloudFormation template creates a DataBrew Profile Job",
    "Resources": {
        "MyDataBrewProfileJob": {
            "Type": "AWS::DataBrew::Job",
            "Properties": {
                "Type": "PROFILE",
                "Name": "job-test",
                "DatasetName": "dataset-test",
                "RoleArn": "arn:aws:iam::1234567891011:role/PassRoleAdmin",
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