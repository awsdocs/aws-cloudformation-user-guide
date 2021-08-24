# AWS::Glue::Database DataLakePrincipal<a name="aws-properties-glue-database-datalakeprincipal"></a>

The AWS Lake Formation principal\.

## Syntax<a name="aws-properties-glue-database-datalakeprincipal-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-database-datalakeprincipal-syntax.json"></a>

```
{
  "[DataLakePrincipalIdentifier](#cfn-glue-database-datalakeprincipal-datalakeprincipalidentifier)" : String
}
```

### YAML<a name="aws-properties-glue-database-datalakeprincipal-syntax.yaml"></a>

```
  [DataLakePrincipalIdentifier](#cfn-glue-database-datalakeprincipal-datalakeprincipalidentifier): String
```

## Properties<a name="aws-properties-glue-database-datalakeprincipal-properties"></a>

`DataLakePrincipalIdentifier`  <a name="cfn-glue-database-datalakeprincipal-datalakeprincipalidentifier"></a>
An identifier for the AWS Lake Formation principal\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)