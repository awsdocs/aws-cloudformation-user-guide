# AWS::Glue::Database FederatedDatabase<a name="aws-properties-glue-database-databaseinput-federateddatabase"></a>

A `FederatedDatabase` structure that references an entity outside the AWS Glue Data Catalog\.

## Syntax<a name="aws-properties-glue-database-databaseinput-federateddatabase-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-database-databaseinput-federateddatabase-syntax.json"></a>

```
{
  "[ConnectionName](#cfn-glue-database-databaseinput-federateddatabase-connectionname)" : String,
  "[Identifier](#cfn-glue-database-databaseinput-federateddatabase-identifier)" : String
}
```

### YAML<a name="aws-properties-glue-database-databaseinput-federateddatabase-syntax.yaml"></a>

```
  [ConnectionName](#cfn-glue-database-databaseinput-federateddatabase-connectionname): String
  [Identifier](#cfn-glue-database-databaseinput-federateddatabase-identifier): String
```

## Properties<a name="aws-properties-glue-database-databaseinput-federateddatabase-properties"></a>

`ConnectionName`  <a name="cfn-glue-database-databaseinput-federateddatabase-connectionname"></a>
The name of the connection to the external metastore\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Identifier`  <a name="cfn-glue-database-databaseinput-federateddatabase-identifier"></a>
A unique identifier for the federated database\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)