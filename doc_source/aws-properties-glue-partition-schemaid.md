# AWS::Glue::Partition SchemaId<a name="aws-properties-glue-partition-schemaid"></a>

The unique ID of the schema in the AWS Glue schema registry\.

## Syntax<a name="aws-properties-glue-partition-schemaid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-schemaid-syntax.json"></a>

```
{
  "[RegistryName](#cfn-glue-partition-schemaid-registryname)" : String,
  "[SchemaArn](#cfn-glue-partition-schemaid-schemaarn)" : String,
  "[SchemaName](#cfn-glue-partition-schemaid-schemaname)" : String
}
```

### YAML<a name="aws-properties-glue-partition-schemaid-syntax.yaml"></a>

```
  [RegistryName](#cfn-glue-partition-schemaid-registryname): String
  [SchemaArn](#cfn-glue-partition-schemaid-schemaarn): String
  [SchemaName](#cfn-glue-partition-schemaid-schemaname): String
```

## Properties<a name="aws-properties-glue-partition-schemaid-properties"></a>

`RegistryName`  <a name="cfn-glue-partition-schemaid-registryname"></a>
The name of the schema registry that contains the schema\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaArn`  <a name="cfn-glue-partition-schemaid-schemaarn"></a>
The Amazon Resource Name \(ARN\) of the schema\. One of `SchemaArn` or `SchemaName` has to be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaName`  <a name="cfn-glue-partition-schemaid-schemaname"></a>
The name of the schema\. One of `SchemaArn` or `SchemaName` has to be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)