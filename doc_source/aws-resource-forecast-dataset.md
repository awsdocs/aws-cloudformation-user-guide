# AWS::Forecast::Dataset<a name="aws-resource-forecast-dataset"></a>

Creates an Amazon Forecast dataset\. The information about the dataset that you provide helps Forecast understand how to consume the data for model training\. This includes the following:
+  * `DataFrequency` * \- How frequently your historical time\-series data is collected\.
+  * `Domain` * and * `DatasetType` * \- Each dataset has an associated dataset domain and a type within the domain\. Amazon Forecast provides a list of predefined domains and types within each domain\. For each unique dataset domain and type within the domain, Amazon Forecast requires your data to include a minimum set of predefined fields\.
+  * `Schema` * \- A schema specifies the fields in the dataset, including the field name and data type\.

After creating a dataset, you import your training data into it and add the dataset to a dataset group\. You use the dataset group to create a predictor\. For more information, see [Importing datasets](https://docs.aws.amazon.com/forecast/latest/dg/howitworks-datasets-groups.html)\.

To get a list of all your datasets, use the [ListDatasets](https://docs.aws.amazon.com/forecast/latest/dg/API_ListDatasets.html) operation\.

For example Forecast datasets, see the [Amazon Forecast Sample GitHub repository](https://github.com/aws-samples/amazon-forecast-samples)\.

**Note**  
The `Status` of a dataset must be `ACTIVE` before you can import training data\. Use the [DescribeDataset](https://docs.aws.amazon.com/forecast/latest/dg/API_DescribeDataset.html) operation to get the status\.

## Syntax<a name="aws-resource-forecast-dataset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-forecast-dataset-syntax.json"></a>

```
{
  "Type" : "AWS::Forecast::Dataset",
  "Properties" : {
      "[DataFrequency](#cfn-forecast-dataset-datafrequency)" : String,
      "[DatasetName](#cfn-forecast-dataset-datasetname)" : String,
      "[DatasetType](#cfn-forecast-dataset-datasettype)" : String,
      "[Domain](#cfn-forecast-dataset-domain)" : String,
      "[EncryptionConfig](#cfn-forecast-dataset-encryptionconfig)" : Json,
      "[Schema](#cfn-forecast-dataset-schema)" : Json,
      "[Tags](#cfn-forecast-dataset-tags)" : [ Json, ... ]
    }
}
```

### YAML<a name="aws-resource-forecast-dataset-syntax.yaml"></a>

```
Type: AWS::Forecast::Dataset
Properties: 
  [DataFrequency](#cfn-forecast-dataset-datafrequency): String
  [DatasetName](#cfn-forecast-dataset-datasetname): String
  [DatasetType](#cfn-forecast-dataset-datasettype): String
  [Domain](#cfn-forecast-dataset-domain): String
  [EncryptionConfig](#cfn-forecast-dataset-encryptionconfig): Json
  [Schema](#cfn-forecast-dataset-schema): Json
  [Tags](#cfn-forecast-dataset-tags): 
    - Json
```

## Properties<a name="aws-resource-forecast-dataset-properties"></a>

`DataFrequency`  <a name="cfn-forecast-dataset-datafrequency"></a>
The frequency of data collection\. This parameter is required for RELATED\_TIME\_SERIES datasets\.  
Valid intervals are Y \(Year\), M \(Month\), W \(Week\), D \(Day\), H \(Hour\), 30min \(30 minutes\), 15min \(15 minutes\), 10min \(10 minutes\), 5min \(5 minutes\), and 1min \(1 minute\)\. For example, "D" indicates every day and "15min" indicates every 15 minutes\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `5`  
*Pattern*: `^Y|M|W|D|H|30min|15min|10min|5min|1min$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetName`  <a name="cfn-forecast-dataset-datasetname"></a>
The name of the dataset\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatasetType`  <a name="cfn-forecast-dataset-datasettype"></a>
The dataset type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ITEM_METADATA | RELATED_TIME_SERIES | TARGET_TIME_SERIES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-forecast-dataset-domain"></a>
The domain associated with the dataset\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CUSTOM | EC2_CAPACITY | INVENTORY_PLANNING | METRICS | RETAIL | WEB_TRAFFIC | WORK_FORCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionConfig`  <a name="cfn-forecast-dataset-encryptionconfig"></a>
A Key Management Service \(KMS\) key and the Identity and Access Management \(IAM\) role that Amazon Forecast can assume to access the key\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schema`  <a name="cfn-forecast-dataset-schema"></a>
The schema for the dataset\. The schema attributes and their order must match the fields in your data\. The dataset `Domain` and `DatasetType` that you choose determine the minimum required fields in your training data\. For information about the required fields for a specific dataset domain and type, see [Dataset Domains and Dataset Types](https://docs.aws.amazon.com/forecast/latest/dg/howitworks-domains-ds-types.html)\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-forecast-dataset-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-forecast-dataset-return-values"></a>

### Ref<a name="aws-resource-forecast-dataset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-forecast-dataset-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-forecast-dataset-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the dataset\.