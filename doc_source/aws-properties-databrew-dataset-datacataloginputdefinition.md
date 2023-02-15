# AWS::DataBrew::Dataset DataCatalogInputDefinition<a name="aws-properties-databrew-dataset-datacataloginputdefinition"></a>

Represents how metadata stored in the AWS Glue Data Catalog is defined in a DataBrew dataset\. 

## Syntax<a name="aws-properties-databrew-dataset-datacataloginputdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-datacataloginputdefinition-syntax.json"></a>

```
{
  "[CatalogId](#cfn-databrew-dataset-datacataloginputdefinition-catalogid)" : String,
  "[DatabaseName](#cfn-databrew-dataset-datacataloginputdefinition-databasename)" : String,
  "[TableName](#cfn-databrew-dataset-datacataloginputdefinition-tablename)" : String,
  "[TempDirectory](#cfn-databrew-dataset-datacataloginputdefinition-tempdirectory)" : S3Location
}
```

### YAML<a name="aws-properties-databrew-dataset-datacataloginputdefinition-syntax.yaml"></a>

```
  [CatalogId](#cfn-databrew-dataset-datacataloginputdefinition-catalogid): String
  [DatabaseName](#cfn-databrew-dataset-datacataloginputdefinition-databasename): String
  [TableName](#cfn-databrew-dataset-datacataloginputdefinition-tablename): String
  [TempDirectory](#cfn-databrew-dataset-datacataloginputdefinition-tempdirectory): 
    S3Location
```

## Properties<a name="aws-properties-databrew-dataset-datacataloginputdefinition-properties"></a>

`CatalogId`  <a name="cfn-databrew-dataset-datacataloginputdefinition-catalogid"></a>
The unique identifier of the AWS account that holds the Data Catalog that stores the data\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-databrew-dataset-datacataloginputdefinition-databasename"></a>
The name of a database in the Data Catalog\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-databrew-dataset-datacataloginputdefinition-tablename"></a>
The name of a database table in the Data Catalog\. This table corresponds to a DataBrew dataset\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TempDirectory`  <a name="cfn-databrew-dataset-datacataloginputdefinition-tempdirectory"></a>
An Amazon location that AWS Glue Data Catalog can use as a temporary directory\.  
*Required*: No  
*Type*: [S3Location](aws-properties-databrew-dataset-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)