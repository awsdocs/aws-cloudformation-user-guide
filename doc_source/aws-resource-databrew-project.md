# AWS::DataBrew::Project<a name="aws-resource-databrew-project"></a>

Creates a new DataBrew project\.

## Syntax<a name="aws-resource-databrew-project-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-databrew-project-syntax.json"></a>

```
{
  "Type" : "AWS::DataBrew::Project",
  "Properties" : {
      "[DatasetName](#cfn-databrew-project-datasetname)" : String,
      "[Name](#cfn-databrew-project-name)" : String,
      "[RecipeName](#cfn-databrew-project-recipename)" : String,
      "[RoleArn](#cfn-databrew-project-rolearn)" : String,
      "[Sample](#cfn-databrew-project-sample)" : Json,
      "[Tags](#cfn-databrew-project-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-databrew-project-syntax.yaml"></a>

```
Type: AWS::DataBrew::Project
Properties: 
  [DatasetName](#cfn-databrew-project-datasetname): String
  [Name](#cfn-databrew-project-name): String
  [RecipeName](#cfn-databrew-project-recipename): String
  [RoleArn](#cfn-databrew-project-rolearn): String
  [Sample](#cfn-databrew-project-sample): Json
  [Tags](#cfn-databrew-project-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-databrew-project-properties"></a>

`DatasetName`  <a name="cfn-databrew-project-datasetname"></a>
The dataset that the project is to act upon\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-databrew-project-name"></a>
The unique name of a project\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecipeName`  <a name="cfn-databrew-project-recipename"></a>
The name of a recipe that will be developed during a project session\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-databrew-project-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that will be assumed for this project\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sample`  <a name="cfn-databrew-project-sample"></a>
The sample size and sampling type to apply to the data\. If this parameter isn't specified, then the sample will consiste of the first 500 rows from the dataset\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-databrew-project-tags"></a>
Metadata tags that have been applied to the project\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-databrew-project-return-values"></a>

### Ref<a name="aws-resource-databrew-project-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myProject" }` 

For an AWS Glue DataBrew project named `myProject`,  `Ref` returns the name of the project\. 

## Examples<a name="aws-resource-databrew-project--examples"></a>



### Creating projects<a name="aws-resource-databrew-project--examples--Creating_projects"></a>

The following examples create new DataBrew projects\.

#### YAML<a name="aws-resource-databrew-project--examples--Creating_projects--yaml"></a>

```
Resources:
  TestDataBrewProject:
    Type: AWS::DataBrew::Project
    Properties:
      Name: project-name
      RecipeName: recipe-name
      DatasetName: dataset-name
      RoleArn: arn:aws:iam::12345678910:role/PassRoleAdmin
      Sample:
        Size: 500
        Type: LAST_N
```

#### JSON<a name="aws-resource-databrew-project--examples--Creating_projects--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "This CloudFormation template creates a DataBrew Project",
    "Resources": {
        "MyDataBrewProject": {
            "Type": "AWS::DataBrew::Project",
            "Properties": {
                "Name": "test-project",
                "RecipeName": "test-project-recipe",
                "DatasetName": "test-dataset",
                "RoleArn": "arn:aws:iam::1234567891011:role/PassRoleAdmin",
                "Sample": {
                    "Size": 500,
                    "Type": "LAST_N"
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