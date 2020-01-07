# AWS::Glue::Crawler CatalogTarget<a name="aws-properties-glue-crawler-catalogtarget"></a>

Specifies an AWS Glue Data Catalog target\.

## Syntax<a name="aws-properties-glue-crawler-catalogtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-catalogtarget-syntax.json"></a>

```
{
  "[DatabaseName](#cfn-glue-crawler-catalogtarget-databasename)" : String,
  "[Tables](#cfn-glue-crawler-catalogtarget-tables)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-catalogtarget-syntax.yaml"></a>

```
  [DatabaseName](#cfn-glue-crawler-catalogtarget-databasename): String
  [Tables](#cfn-glue-crawler-catalogtarget-tables): 
    - String
```

## Properties<a name="aws-properties-glue-crawler-catalogtarget-properties"></a>

`DatabaseName`  <a name="cfn-glue-crawler-catalogtarget-databasename"></a>
The name of the database to be synchronized\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tables`  <a name="cfn-glue-crawler-catalogtarget-tables"></a>
A list of the tables to be synchronized\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)