# AWS::RDS::DBCluster Endpoint<a name="aws-properties-rds-dbcluster-endpoint"></a>

Specifies the connection endpoint for the primary instance of the DB cluster\.

## Syntax<a name="aws-properties-rds-dbcluster-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbcluster-endpoint-syntax.json"></a>

```
{
  "[Address](#cfn-rds-dbcluster-endpoint-address)" : String,
  "[Port](#cfn-rds-dbcluster-endpoint-port)" : String
}
```

### YAML<a name="aws-properties-rds-dbcluster-endpoint-syntax.yaml"></a>

```
  [Address](#cfn-rds-dbcluster-endpoint-address): String
  [Port](#cfn-rds-dbcluster-endpoint-port): String
```

## Properties<a name="aws-properties-rds-dbcluster-endpoint-properties"></a>

`Address`  <a name="cfn-rds-dbcluster-endpoint-address"></a>
Specifies the connection endpoint for the primary instance of the DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-rds-dbcluster-endpoint-port"></a>
Specifies the port that the database engine is listening on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)