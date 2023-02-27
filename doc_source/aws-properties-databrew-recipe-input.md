# AWS::DataBrew::Recipe Input<a name="aws-properties-databrew-recipe-input"></a>

Represents information on how DataBrew can find data, in either the AWS Glue Data Catalog or Amazon S3\.

## Syntax<a name="aws-properties-databrew-recipe-input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-recipe-input-syntax.json"></a>

```
{
  "[DataCatalogInputDefinition](#cfn-databrew-recipe-input-datacataloginputdefinition)" : DataCatalogInputDefinition,
  "[S3InputDefinition](#cfn-databrew-recipe-input-s3inputdefinition)" : S3Location
}
```

### YAML<a name="aws-properties-databrew-recipe-input-syntax.yaml"></a>

```
  [DataCatalogInputDefinition](#cfn-databrew-recipe-input-datacataloginputdefinition): 
    DataCatalogInputDefinition
  [S3InputDefinition](#cfn-databrew-recipe-input-s3inputdefinition): 
    S3Location
```

## Properties<a name="aws-properties-databrew-recipe-input-properties"></a>

`DataCatalogInputDefinition`  <a name="cfn-databrew-recipe-input-datacataloginputdefinition"></a>
The AWS Glue Data Catalog parameters for the data\.  
*Required*: No  
*Type*: [DataCatalogInputDefinition](aws-properties-databrew-recipe-datacataloginputdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3InputDefinition`  <a name="cfn-databrew-recipe-input-s3inputdefinition"></a>
The Amazon S3 location where the data is stored\.  
*Required*: No  
*Type*: [S3Location](aws-properties-databrew-recipe-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)