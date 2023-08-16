# AWS::RDS::DBParameterGroup<a name="aws-resource-rds-dbparametergroup"></a>

The `AWS::RDS::DBParameterGroup` resource creates a custom parameter group for an RDS database family\.

This type can be declared in a template and referenced in the `DBParameterGroupName` property of an ` [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)` resource\.

For information about configuring parameters for Amazon RDS DB instances, see [Working with parameter groups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithParamGroups.html) in the *Amazon RDS User Guide*\.

For information about configuring parameters for Amazon Aurora DB instances, see [Working with parameter groups](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_WorkingWithParamGroups.html) in the *Amazon Aurora User Guide*\.

**Note**  
Applying a parameter group to a DB instance may require the DB instance to reboot, resulting in a database outage for the duration of the reboot\.

## Syntax<a name="aws-resource-rds-dbparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBParameterGroup",
  "Properties" : {
      "[DBParameterGroupName](#cfn-rds-dbparametergroup-dbparametergroupname)" : String,
      "[Description](#cfn-rds-dbparametergroup-description)" : String,
      "[Family](#cfn-rds-dbparametergroup-family)" : String,
      "[Parameters](#cfn-rds-dbparametergroup-parameters)" : Json,
      "[Tags](#cfn-rds-dbparametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rds-dbparametergroup-syntax.yaml"></a>

```
Type: AWS::RDS::DBParameterGroup
Properties: 
  [DBParameterGroupName](#cfn-rds-dbparametergroup-dbparametergroupname): String
  [Description](#cfn-rds-dbparametergroup-description): String
  [Family](#cfn-rds-dbparametergroup-family): String
  [Parameters](#cfn-rds-dbparametergroup-parameters): Json
  [Tags](#cfn-rds-dbparametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rds-dbparametergroup-properties"></a>

`DBParameterGroupName`  <a name="cfn-rds-dbparametergroup-dbparametergroupname"></a>
The name of the DB parameter group\.  
Constraints:  
+ Must be 1 to 255 letters, numbers, or hyphens\.
+ First character must be a letter
+ Can't end with a hyphen or contain two consecutive hyphens
If you don't specify a value for `DBParameterGroupName` property, a name is automatically created for the DB parameter group\.  
This value is stored as a lowercase string\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-rds-dbparametergroup-description"></a>
Provides the customer\-specified description for this DB parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Family`  <a name="cfn-rds-dbparametergroup-family"></a>
The DB parameter group family name\. A DB parameter group can be associated with one and only one DB parameter group family, and can be applied only to a DB instance running a DB engine and engine version compatible with that DB parameter group family\.  
The DB parameter group family can't be changed when updating a DB parameter group\.
To list all of the available parameter group families, use the following command:  
`aws rds describe-db-engine-versions --query "DBEngineVersions[].DBParameterGroupFamily"`  
The output contains duplicates\.  
For more information, see `[CreateDBParameterGroup](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBParameterGroup.html)`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-rds-dbparametergroup-parameters"></a>
An array of parameter names and values for the parameter update\. At least one parameter name and value must be supplied\. Subsequent arguments are optional\.  
For more information about DB parameters and DB parameter groups for Amazon RDS DB engines, see [Working with DB Parameter Groups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithParamGroups.html) in the *Amazon RDS User Guide*\.  
For more information about DB cluster and DB instance parameters and parameter groups for Amazon Aurora DB engines, see [ Working with DB Parameter Groups and DB Cluster Parameter Groups](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_WorkingWithParamGroups.html) in the *Amazon Aurora User Guide*\.  
AWS CloudFormation doesn't support specifying an apply method for each individual parameter\. The default apply method for each parameter is used\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rds-dbparametergroup-tags"></a>
An optional array of key\-value pairs to apply to this DB parameter group\.  
Currently, this is the only property that supports drift detection\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-dbparametergroup-return-values"></a>

### Ref<a name="aws-resource-rds-dbparametergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the name of the DB parameter group\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rds-dbparametergroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-rds-dbparametergroup-return-values-fn--getatt-fn--getatt"></a>

`DBParameterGroupName`  <a name="DBParameterGroupName-fn::getatt"></a>
The name of the DB parameter group\.

## Examples<a name="aws-resource-rds-dbparametergroup--examples"></a>



### <a name="aws-resource-rds-dbparametergroup--examples--"></a>

The following example creates a parameter group for a MySQL DB instance and sets the `sql_mode`, `max_allowed_packet`, and `innodb_buffer_pool_size` parameters\. 

#### JSON<a name="aws-resource-rds-dbparametergroup--examples----json"></a>

```
"RDSDBParameterGroup": {
        "Type": "AWS::RDS::DBParameterGroup",
        "Properties": {
            "Description": "CloudFormation Sample MySQL Parameter Group",
            "Family": "mysql8.0",
            "Parameters": {
                "sql_mode": "IGNORE_SPACE",
                "max_allowed_packet": 1024,
                "innodb_buffer_pool_size": "{DBInstanceClassMemory*3/4}"
            }
        }
    }
```

#### YAML<a name="aws-resource-rds-dbparametergroup--examples----yaml"></a>

```
RDSDBParameterGroup:
  Type: 'AWS::RDS::DBParameterGroup'
  Properties:
    Description: CloudFormation Sample MySQL Parameter Group
    Family: mysql8.0
    Parameters:
      sql_mode: IGNORE_SPACE
      max_allowed_packet: 1024
      innodb_buffer_pool_size: '{DBInstanceClassMemory*3/4}'
```