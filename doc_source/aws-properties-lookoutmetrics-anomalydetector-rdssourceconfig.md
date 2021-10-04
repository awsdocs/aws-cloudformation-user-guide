# AWS::LookoutMetrics::AnomalyDetector RDSSourceConfig<a name="aws-properties-lookoutmetrics-anomalydetector-rdssourceconfig"></a>

Contains information about the Amazon Relational Database Service \(RDS\) configuration\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-rdssourceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-rdssourceconfig-syntax.json"></a>

```
{
  "[DatabaseHost](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databasehost)" : String,
  "[DatabaseName](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databasename)" : String,
  "[DatabasePort](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databaseport)" : Integer,
  "[DBInstanceIdentifier](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-dbinstanceidentifier)" : String,
  "[RoleArn](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-rolearn)" : String,
  "[SecretManagerArn](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-secretmanagerarn)" : String,
  "[TableName](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-tablename)" : String,
  "[VpcConfiguration](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-vpcconfiguration)" : VpcConfiguration
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-rdssourceconfig-syntax.yaml"></a>

```
  [DatabaseHost](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databasehost): String
  [DatabaseName](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databasename): String
  [DatabasePort](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databaseport): Integer
  [DBInstanceIdentifier](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-dbinstanceidentifier): String
  [RoleArn](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-rolearn): String
  [SecretManagerArn](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-secretmanagerarn): String
  [TableName](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-tablename): String
  [VpcConfiguration](#cfn-lookoutmetrics-anomalydetector-rdssourceconfig-vpcconfiguration): 
    VpcConfiguration
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-rdssourceconfig-properties"></a>

`DatabaseHost`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databasehost"></a>
The host name of the database\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databasename"></a>
The name of the RDS database\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabasePort`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-databaseport"></a>
The port number where the database can be accessed\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBInstanceIdentifier`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-dbinstanceidentifier"></a>
A string identifying the database instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretManagerArn`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-secretmanagerarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Secrets Manager role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-tablename"></a>
The name of the table in the database\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-lookoutmetrics-anomalydetector-rdssourceconfig-vpcconfiguration"></a>
An object containing information about the Amazon Virtual Private Cloud \(VPC\) configuration\.  
*Required*: Yes  
*Type*: [VpcConfiguration](aws-properties-lookoutmetrics-anomalydetector-vpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)