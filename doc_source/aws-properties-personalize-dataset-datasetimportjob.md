# AWS::Personalize::Dataset DatasetImportJob<a name="aws-properties-personalize-dataset-datasetimportjob"></a>

Describes a job that imports training data from a data source \(Amazon S3 bucket\) to an Amazon Personalize dataset\. For more information, see [CreateDatasetImportJob](https://docs.aws.amazon.com/personalize/latest/dg/API_CreateDatasetImportJob.html)\.

A dataset import job can be in one of the following states:
+ CREATE PENDING > CREATE IN\_PROGRESS > ACTIVE \-or\- CREATE FAILED

## Syntax<a name="aws-properties-personalize-dataset-datasetimportjob-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-personalize-dataset-datasetimportjob-syntax.json"></a>

```
{
  "[DatasetArn](#cfn-personalize-dataset-datasetimportjob-datasetarn)" : String,
  "[DatasetImportJobArn](#cfn-personalize-dataset-datasetimportjob-datasetimportjobarn)" : String,
  "[DataSource](#cfn-personalize-dataset-datasetimportjob-datasource)" : DataSource,
  "[JobName](#cfn-personalize-dataset-datasetimportjob-jobname)" : String,
  "[RoleArn](#cfn-personalize-dataset-datasetimportjob-rolearn)" : String
}
```

### YAML<a name="aws-properties-personalize-dataset-datasetimportjob-syntax.yaml"></a>

```
  [DatasetArn](#cfn-personalize-dataset-datasetimportjob-datasetarn): String
  [DatasetImportJobArn](#cfn-personalize-dataset-datasetimportjob-datasetimportjobarn): String
  [DataSource](#cfn-personalize-dataset-datasetimportjob-datasource): 
    DataSource
  [JobName](#cfn-personalize-dataset-datasetimportjob-jobname): String
  [RoleArn](#cfn-personalize-dataset-datasetimportjob-rolearn): String
```

## Properties<a name="aws-properties-personalize-dataset-datasetimportjob-properties"></a>

`DatasetArn`  <a name="cfn-personalize-dataset-datasetimportjob-datasetarn"></a>
The Amazon Resource Name \(ARN\) of the dataset that receives the imported data\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `arn:([a-z\d-]+):personalize:.*:.*:.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetImportJobArn`  <a name="cfn-personalize-dataset-datasetimportjob-datasetimportjobarn"></a>
The ARN of the dataset import job\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `arn:([a-z\d-]+):personalize:.*:.*:.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSource`  <a name="cfn-personalize-dataset-datasetimportjob-datasource"></a>
The Amazon S3 bucket that contains the training data to import\.  
*Required*: No  
*Type*: [DataSource](aws-properties-personalize-dataset-datasource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobName`  <a name="cfn-personalize-dataset-datasetimportjob-jobname"></a>
The name of the import job\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\-_]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-personalize-dataset-datasetimportjob-rolearn"></a>
The ARN of the IAM role that has permissions to read from the Amazon S3 data source\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `arn:([a-z\d-]+):personalize:.*:.*:.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)