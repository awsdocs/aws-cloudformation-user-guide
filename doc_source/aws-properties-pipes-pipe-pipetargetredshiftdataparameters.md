# AWS::Pipes::Pipe PipeTargetRedshiftDataParameters<a name="aws-properties-pipes-pipe-pipetargetredshiftdataparameters"></a>

These are custom parameters to be used when the target is a Amazon Redshift cluster to invoke the Amazon Redshift Data API BatchExecuteStatement\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetredshiftdataparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetredshiftdataparameters-syntax.json"></a>

```
{
  "[Database](#cfn-pipes-pipe-pipetargetredshiftdataparameters-database)" : String,
  "[DbUser](#cfn-pipes-pipe-pipetargetredshiftdataparameters-dbuser)" : String,
  "[SecretManagerArn](#cfn-pipes-pipe-pipetargetredshiftdataparameters-secretmanagerarn)" : String,
  "[Sqls](#cfn-pipes-pipe-pipetargetredshiftdataparameters-sqls)" : [ String, ... ],
  "[StatementName](#cfn-pipes-pipe-pipetargetredshiftdataparameters-statementname)" : String,
  "[WithEvent](#cfn-pipes-pipe-pipetargetredshiftdataparameters-withevent)" : Boolean
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetredshiftdataparameters-syntax.yaml"></a>

```
  [Database](#cfn-pipes-pipe-pipetargetredshiftdataparameters-database): String
  [DbUser](#cfn-pipes-pipe-pipetargetredshiftdataparameters-dbuser): String
  [SecretManagerArn](#cfn-pipes-pipe-pipetargetredshiftdataparameters-secretmanagerarn): String
  [Sqls](#cfn-pipes-pipe-pipetargetredshiftdataparameters-sqls): 
    - String
  [StatementName](#cfn-pipes-pipe-pipetargetredshiftdataparameters-statementname): String
  [WithEvent](#cfn-pipes-pipe-pipetargetredshiftdataparameters-withevent): Boolean
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetredshiftdataparameters-properties"></a>

`Database`  <a name="cfn-pipes-pipe-pipetargetredshiftdataparameters-database"></a>
The name of the database\. Required when authenticating using temporary credentials\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DbUser`  <a name="cfn-pipes-pipe-pipetargetredshiftdataparameters-dbuser"></a>
The database user name\. Required when authenticating using temporary credentials\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretManagerArn`  <a name="cfn-pipes-pipe-pipetargetredshiftdataparameters-secretmanagerarn"></a>
The name or ARN of the secret that enables access to the database\. Required when authenticating using Secrets Manager\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sqls`  <a name="cfn-pipes-pipe-pipetargetredshiftdataparameters-sqls"></a>
The SQL statement text to run\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatementName`  <a name="cfn-pipes-pipe-pipetargetredshiftdataparameters-statementname"></a>
The name of the SQL statement\. You can name the SQL statement when you create it to identify the query\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WithEvent`  <a name="cfn-pipes-pipe-pipetargetredshiftdataparameters-withevent"></a>
Indicates whether to send an event back to EventBridge after the SQL statement runs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)