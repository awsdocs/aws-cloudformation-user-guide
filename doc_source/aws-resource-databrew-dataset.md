# AWS::DataBrew::Dataset<a name="aws-resource-databrew-dataset"></a>

Represents a dataset that can be processed by DataBrew\.

## Syntax<a name="aws-resource-databrew-dataset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-databrew-dataset-syntax.json"></a>

```
{
  "Type" : "AWS::DataBrew::Dataset",
  "Properties" : {
      "[FormatOptions](#cfn-databrew-dataset-formatoptions)" : Json,
      "[Input](#cfn-databrew-dataset-input)" : Json,
      "[Name](#cfn-databrew-dataset-name)" : String,
      "[Tags](#cfn-databrew-dataset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-databrew-dataset-syntax.yaml"></a>

```
Type: AWS::DataBrew::Dataset
Properties: 
  [FormatOptions](#cfn-databrew-dataset-formatoptions): Json
  [Input](#cfn-databrew-dataset-input): Json
  [Name](#cfn-databrew-dataset-name): String
  [Tags](#cfn-databrew-dataset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-databrew-dataset-properties"></a>

`FormatOptions`  <a name="cfn-databrew-dataset-formatoptions"></a>
Options that define how DataBrew interprets the data in the dataset\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Input`  <a name="cfn-databrew-dataset-input"></a>
Information on how DataBrew can find the dataset, in either the AWS Glue Data Catalog or Amazon S3\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-databrew-dataset-name"></a>
The unique name of the dataset\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-databrew-dataset-tags"></a>
Metadata tags that have been applied to the dataset\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-databrew-dataset-return-values"></a>

### Ref<a name="aws-resource-databrew-dataset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myDataset" }` 

For the AWS Glue DataBrew dataset `myDataset`, `Ref` returns the name of the dataset\.