# AWS::Events::Rule RedshiftDataParameters<a name="aws-properties-events-rule-redshiftdataparameters"></a>

These are custom parameters to be used when the target is a Redshift cluster to invoke the Redshift Data API ExecuteStatement based on EventBridge events\.

## Syntax<a name="aws-properties-events-rule-redshiftdataparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-redshiftdataparameters-syntax.json"></a>

```
{
  "[Database](#cfn-events-rule-redshiftdataparameters-database)" : String,
  "[DbUser](#cfn-events-rule-redshiftdataparameters-dbuser)" : String,
  "[SecretManagerArn](#cfn-events-rule-redshiftdataparameters-secretmanagerarn)" : String,
  "[Sql](#cfn-events-rule-redshiftdataparameters-sql)" : String,
  "[StatementName](#cfn-events-rule-redshiftdataparameters-statementname)" : String,
  "[WithEvent](#cfn-events-rule-redshiftdataparameters-withevent)" : Boolean
}
```

### YAML<a name="aws-properties-events-rule-redshiftdataparameters-syntax.yaml"></a>

```
  [Database](#cfn-events-rule-redshiftdataparameters-database): String
  [DbUser](#cfn-events-rule-redshiftdataparameters-dbuser): String
  [SecretManagerArn](#cfn-events-rule-redshiftdataparameters-secretmanagerarn): String
  [Sql](#cfn-events-rule-redshiftdataparameters-sql): String
  [StatementName](#cfn-events-rule-redshiftdataparameters-statementname): String
  [WithEvent](#cfn-events-rule-redshiftdataparameters-withevent): Boolean
```

## Properties<a name="aws-properties-events-rule-redshiftdataparameters-properties"></a>

`Database`  <a name="cfn-events-rule-redshiftdataparameters-database"></a>
The name of the database\. Required when authenticating using temporary credentials\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `([a-zA-Z0-9]+)|(\$(\.[\w_-]+(\[(\d+|\*)\])*)*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DbUser`  <a name="cfn-events-rule-redshiftdataparameters-dbuser"></a>
The database user name\. Required when authenticating using temporary credentials\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `([a-zA-Z0-9]+)|(\$(\.[\w_-]+(\[(\d+|\*)\])*)*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretManagerArn`  <a name="cfn-events-rule-redshiftdataparameters-secretmanagerarn"></a>
The name or ARN of the secret that enables access to the database\. Required when authenticating using AWS Secrets Manager\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Pattern*: `(^arn:aws([a-z]|\-)*:secretsmanager:[a-z0-9-.]+:.*)|(\$(\.[\w_-]+(\[(\d+|\*)\])*)*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sql`  <a name="cfn-events-rule-redshiftdataparameters-sql"></a>
The SQL statement text to run\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatementName`  <a name="cfn-events-rule-redshiftdataparameters-statementname"></a>
The name of the SQL statement\. You can name the SQL statement when you create it to identify the query\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WithEvent`  <a name="cfn-events-rule-redshiftdataparameters-withevent"></a>
Indicates whether to send an event back to EventBridge after the SQL statement runs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)