# AWS::Forecast::DatasetGroup<a name="aws-resource-forecast-datasetgroup"></a>

Creates a dataset group, which holds a collection of related datasets\. You can add datasets to the dataset group when you create the dataset group, or later by using the [UpdateDatasetGroup](https://docs.aws.amazon.com/forecast/latest/dg/API_UpdateDatasetGroup.html) operation\.

After creating a dataset group and adding datasets, you use the dataset group when you create a predictor\. For more information, see [Dataset groups](https://docs.aws.amazon.com/forecast/latest/dg/howitworks-datasets-groups.html)\.

To get a list of all your datasets groups, use the [ListDatasetGroups](https://docs.aws.amazon.com/forecast/latest/dg/API_ListDatasetGroups.html) operation\.

**Note**  
The `Status` of a dataset group must be `ACTIVE` before you can use the dataset group to create a predictor\. To get the status, use the [DescribeDatasetGroup](https://docs.aws.amazon.com/forecast/latest/dg/API_DescribeDatasetGroup.html) operation\.

## Syntax<a name="aws-resource-forecast-datasetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-forecast-datasetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::Forecast::DatasetGroup",
  "Properties" : {
      "[DatasetArns](#cfn-forecast-datasetgroup-datasetarns)" : [ String, ... ],
      "[DatasetGroupName](#cfn-forecast-datasetgroup-datasetgroupname)" : String,
      "[Domain](#cfn-forecast-datasetgroup-domain)" : String,
      "[Tags](#cfn-forecast-datasetgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-forecast-datasetgroup-syntax.yaml"></a>

```
Type: AWS::Forecast::DatasetGroup
Properties: 
  [DatasetArns](#cfn-forecast-datasetgroup-datasetarns): 
    - String
  [DatasetGroupName](#cfn-forecast-datasetgroup-datasetgroupname): String
  [Domain](#cfn-forecast-datasetgroup-domain): String
  [Tags](#cfn-forecast-datasetgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-forecast-datasetgroup-properties"></a>

`DatasetArns`  <a name="cfn-forecast-datasetgroup-datasetarns"></a>
An array of Amazon Resource Names \(ARNs\) of the datasets that you want to include in the dataset group\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetGroupName`  <a name="cfn-forecast-datasetgroup-datasetgroupname"></a>
The name of the dataset group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Domain`  <a name="cfn-forecast-datasetgroup-domain"></a>
The domain associated with the dataset group\. When you add a dataset to a dataset group, this value and the value specified for the `Domain` parameter of the [CreateDataset](https://docs.aws.amazon.com/forecast/latest/dg/API_CreateDataset.html) operation must match\.  
The `Domain` and `DatasetType` that you choose determine the fields that must be present in training data that you import to a dataset\. For example, if you choose the `RETAIL` domain and `TARGET_TIME_SERIES` as the `DatasetType`, Amazon Forecast requires that `item_id`, `timestamp`, and `demand` fields are present in your data\. For more information, see [Dataset groups](https://docs.aws.amazon.com/forecast/latest/dg/howitworks-datasets-groups.html)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CUSTOM | EC2_CAPACITY | INVENTORY_PLANNING | METRICS | RETAIL | WEB_TRAFFIC | WORK_FORCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-forecast-datasetgroup-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-forecast-datasetgroup-return-values"></a>

### Fn::GetAtt<a name="aws-resource-forecast-datasetgroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-forecast-datasetgroup-return-values-fn--getatt-fn--getatt"></a>

`DatasetGroupArn`  <a name="DatasetGroupArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the dataset group\.