# AWS::DataBrew::Recipe DataCatalogInputDefinition<a name="aws-properties-databrew-recipe-datacataloginputdefinition"></a>

Represents how metadata stored in the AWS Glue Data Catalog is defined in a DataBrew dataset\. 

## Syntax<a name="aws-properties-databrew-recipe-datacataloginputdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-recipe-datacataloginputdefinition-syntax.json"></a>

```
{
  "[CatalogId](#cfn-databrew-recipe-datacataloginputdefinition-catalogid)" : String,
  "[DatabaseName](#cfn-databrew-recipe-datacataloginputdefinition-databasename)" : String,
  "[TableName](#cfn-databrew-recipe-datacataloginputdefinition-tablename)" : String,
  "[TempDirectory](#cfn-databrew-recipe-datacataloginputdefinition-tempdirectory)" : S3Location
}
```

### YAML<a name="aws-properties-databrew-recipe-datacataloginputdefinition-syntax.yaml"></a>

```
  [CatalogId](#cfn-databrew-recipe-datacataloginputdefinition-catalogid): String
  [DatabaseName](#cfn-databrew-recipe-datacataloginputdefinition-databasename): String
  [TableName](#cfn-databrew-recipe-datacataloginputdefinition-tablename): String
  [TempDirectory](#cfn-databrew-recipe-datacataloginputdefinition-tempdirectory): 
    S3Location
```

## Properties<a name="aws-properties-databrew-recipe-datacataloginputdefinition-properties"></a>

`CatalogId`  <a name="cfn-databrew-recipe-datacataloginputdefinition-catalogid"></a>
The unique identifier of the AWS account that holds the Data Catalog that stores the data\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-databrew-recipe-datacataloginputdefinition-databasename"></a>
The name of a database in the Data Catalog\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-databrew-recipe-datacataloginputdefinition-tablename"></a>
The name of a database table in the Data Catalog\. This table corresponds to a DataBrew dataset\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TempDirectory`  <a name="cfn-databrew-recipe-datacataloginputdefinition-tempdirectory"></a>
An Amazon location that AWS Glue Data Catalog can use as a temporary directory\.  
*Required*: No  
*Type*: [S3Location](aws-properties-databrew-recipe-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)