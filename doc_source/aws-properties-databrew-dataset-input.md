# AWS::DataBrew::Dataset Input<a name="aws-properties-databrew-dataset-input"></a>

Represents information on how DataBrew can find data, in either the AWS Glue Data Catalog or Amazon S3\.

## Syntax<a name="aws-properties-databrew-dataset-input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-input-syntax.json"></a>

```
{
  "[DatabaseInputDefinition](#cfn-databrew-dataset-input-databaseinputdefinition)" : DatabaseInputDefinition,
  "[DataCatalogInputDefinition](#cfn-databrew-dataset-input-datacataloginputdefinition)" : DataCatalogInputDefinition,
  "[Metadata](#cfn-databrew-dataset-input-metadata)" : Metadata,
  "[S3InputDefinition](#cfn-databrew-dataset-input-s3inputdefinition)" : S3Location
}
```

### YAML<a name="aws-properties-databrew-dataset-input-syntax.yaml"></a>

```
  [DatabaseInputDefinition](#cfn-databrew-dataset-input-databaseinputdefinition): 
    DatabaseInputDefinition
  [DataCatalogInputDefinition](#cfn-databrew-dataset-input-datacataloginputdefinition): 
    DataCatalogInputDefinition
  [Metadata](#cfn-databrew-dataset-input-metadata): 
    Metadata
  [S3InputDefinition](#cfn-databrew-dataset-input-s3inputdefinition): 
    S3Location
```

## Properties<a name="aws-properties-databrew-dataset-input-properties"></a>

`DatabaseInputDefinition`  <a name="cfn-databrew-dataset-input-databaseinputdefinition"></a>
Connection information for dataset input files stored in a database\.  
*Required*: No  
*Type*: [DatabaseInputDefinition](aws-properties-databrew-dataset-databaseinputdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataCatalogInputDefinition`  <a name="cfn-databrew-dataset-input-datacataloginputdefinition"></a>
The AWS Glue Data Catalog parameters for the data\.  
*Required*: No  
*Type*: [DataCatalogInputDefinition](aws-properties-databrew-dataset-datacataloginputdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metadata`  <a name="cfn-databrew-dataset-input-metadata"></a>
Contains additional resource information needed for specific datasets\.  
*Required*: No  
*Type*: [Metadata](aws-properties-databrew-dataset-metadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3InputDefinition`  <a name="cfn-databrew-dataset-input-s3inputdefinition"></a>
The Amazon S3 location where the data is stored\.  
*Required*: No  
*Type*: [S3Location](aws-properties-databrew-dataset-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)