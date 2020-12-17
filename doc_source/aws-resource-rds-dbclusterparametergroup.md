# AWS::RDS::DBClusterParameterGroup<a name="aws-resource-rds-dbclusterparametergroup"></a>

The `AWS::RDS::DBClusterParameterGroup` resource creates a new Amazon RDS DB cluster parameter group\.

For information about configuring parameters for Amazon Aurora DB instances, see [Working with DB parameter groups and DB cluster parameter groups](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/USER_WorkingWithParamGroups.html) in the *Amazon Aurora User Guide*\.

**Note**  
If you apply a parameter group to a DB cluster, then its DB instances might need to reboot\. This can result in an outage while the DB instances are rebooting\.  
If you apply a change to parameter group associated with a stopped DB cluster, then the update stack waits until the DB cluster is started\.

## Syntax<a name="aws-resource-rds-dbclusterparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbclusterparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBClusterParameterGroup",
  "Properties" : {
      "[Description](#cfn-rds-dbclusterparametergroup-description)" : String,
      "[Family](#cfn-rds-dbclusterparametergroup-family)" : String,
      "[Parameters](#cfn-rds-dbclusterparametergroup-parameters)" : Json,
      "[Tags](#cfn-rds-dbclusterparametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rds-dbclusterparametergroup-syntax.yaml"></a>

```
Type: AWS::RDS::DBClusterParameterGroup
Properties: 
  [Description](#cfn-rds-dbclusterparametergroup-description): String
  [Family](#cfn-rds-dbclusterparametergroup-family): String
  [Parameters](#cfn-rds-dbclusterparametergroup-parameters): Json
  [Tags](#cfn-rds-dbclusterparametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rds-dbclusterparametergroup-properties"></a>

`Description`  <a name="cfn-rds-dbclusterparametergroup-description"></a>
A friendly description for this DB cluster parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Family`  <a name="cfn-rds-dbclusterparametergroup-family"></a>
The DB cluster parameter group family name\. A DB cluster parameter group can be associated with one and only one DB cluster parameter group family, and can be applied only to a DB cluster running a DB engine and engine version compatible with that DB cluster parameter group family\.  
The DB cluster parameter group family can't be changed when updating a DB cluster parameter group\.
To list all of the available parameter group families, use the following command:  
`aws rds describe-db-engine-versions --query "DBEngineVersions[].DBParameterGroupFamily"`  
The output contains duplicates\.  
For more information, see `[CreateDBClusterParameterGroup](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBClusterParameterGroup.html)`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-rds-dbclusterparametergroup-parameters"></a>
Provides a list of parameters for the DB cluster parameter group\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rds-dbclusterparametergroup-tags"></a>
Tags to assign to the DB cluster parameter group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-dbclusterparametergroup-return-values"></a>

### Ref<a name="aws-resource-rds-dbclusterparametergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB cluster parameter group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-rds-dbclusterparametergroup--examples"></a>



### <a name="aws-resource-rds-dbclusterparametergroup--examples--"></a>

The following snippet creates a DB cluster parameter group for an Aurora MySQL DB cluster and sets the `time_zone` and `character_set_database` parameters: 

#### JSON<a name="aws-resource-rds-dbclusterparametergroup--examples----json"></a>

```
"RDSDBClusterParameterGroup": {
        "Type": "AWS::RDS::DBClusterParameterGroup",
        "Properties": {
            "Description": "CloudFormation Sample Aurora Cluster Parameter Group",
            "Family": "aurora5.6",
            "Parameters": {
                "time_zone": "US/Eastern",
                "character_set_database": "utf32"
            }
        }
    }
```

#### YAML<a name="aws-resource-rds-dbclusterparametergroup--examples----yaml"></a>

```
RDSDBClusterParameterGroup:
  Type: 'AWS::RDS::DBClusterParameterGroup'
  Properties:
    Description: CloudFormation Sample Aurora Cluster Parameter Group
    Family: aurora5.6
    Parameters:
      time_zone: US/Eastern
      character_set_database: utf32
```