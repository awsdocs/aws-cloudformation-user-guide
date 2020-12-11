# AWS::DataBrew::Dataset<a name="aws-resource-databrew-dataset"></a>

Creates a new DataBrew dataset\.

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

For an AWS Glue DataBrew dataset named `myDataset`, `Ref` returns the name of the dataset\. 

## Examples<a name="aws-resource-databrew-dataset--examples"></a>



### Creating datasets<a name="aws-resource-databrew-dataset--examples--Creating_datasets"></a>

The following examples create new DataBrew datasets\.

#### YAML<a name="aws-resource-databrew-dataset--examples--Creating_datasets--yaml"></a>

```
Resources:
  TestDataBrewDataset:
    Type: AWS::DataBrew::Dataset
    Properties:
      Name: dataset-name
      Input:
        S3InputDefinition:
          Bucket: !Join [ '', ['databrew-cfn-integration-tests-', !Ref 'AWS::Region', '-', !Ref 'AWS::AccountId' ] ]
          Key: cocktails.json
      FormatOptions:
        Json:
          MultiLine: True
```

#### JSON<a name="aws-resource-databrew-dataset--examples--Creating_datasets--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "This CloudFormation template creates a DataBrew Dataset",
    "Resources": {
    "TestDataBrewDataset": {
      "Type": "AWS::DataBrew::Dataset",
      "Properties": {
        "Name": "cf-test-dataset1",
        "Input": {
          "S3InputDefinition": {
            "Bucket": "test-location",
            "Key": "test.xlsx"
          }
        },
        "FormatOptions": {
          "Excel": {
            "SheetNames": ["test"]
          }
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