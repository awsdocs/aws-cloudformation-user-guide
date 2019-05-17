# AWS::RDS::DBParameterGroup<a name="aws-properties-rds-dbparametergroup"></a>

The `AWS::RDS::DBParameterGroup` resource creates a custom parameter group for an RDS database family\.

This type can be declared in a template and referenced in the `DBParameterGroupName` property of an ` [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)` resource\.

**Note**  
Applying a parameter group to a DB instance may require the instance to reboot, resulting in a database outage for the duration of the reboot\.

## Syntax<a name="aws-properties-rds-dbparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBParameterGroup",
  "Properties" : {
      "[Description](#cfn-rds-dbparametergroup-description)" : String,
      "[Family](#cfn-rds-dbparametergroup-family)" : String,
      "[Parameters](#cfn-rds-dbparametergroup-parameters)" : {Key : Value, ...},
      "[Tags](#cfn-rds-dbparametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-properties-rds-dbparametergroup-syntax.yaml"></a>

```
Type: AWS::RDS::DBParameterGroup
Properties: 
  [Description](#cfn-rds-dbparametergroup-description): String
  [Family](#cfn-rds-dbparametergroup-family): String
  [Parameters](#cfn-rds-dbparametergroup-parameters): 
    Key : Value
  [Tags](#cfn-rds-dbparametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-rds-dbparametergroup-properties"></a>

`Description`  <a name="cfn-rds-dbparametergroup-description"></a>
Provides the customer\-specified description for this DB Parameter Group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Family`  <a name="cfn-rds-dbparametergroup-family"></a>
Provides the name of the DB Parameter Group Family that this DB Parameter Group is compatible with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-rds-dbparametergroup-parameters"></a>
An array of parameter names, values, and the apply method for the parameter update\. At least one parameter name, value, and apply method must be supplied; subsequent arguments are optional\. A maximum of 20 parameters may be modified in a single request\.  
 **MySQL**   
Valid Values \(for Apply method\): `immediate` \| `pending-reboot`   
You can use the immediate value with dynamic parameters only\. You can use the `pending-reboot` value for both dynamic and static parameters, and changes are applied when DB Instance reboots\.  
 **Oracle**   
Valid Values \(for Apply method\): `pending-reboot`   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rds-dbparametergroup-tags"></a>
Tags to assign to the DB parameter group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-properties-rds-dbparametergroup-return-values"></a>

### Ref<a name="aws-properties-rds-dbparametergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB parameter group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-rds-dbparametergroup--examples"></a>

### <a name="aws-properties-rds-dbparametergroup--examples--"></a>

The following example creates a parameter group for an Aurora DB cluster that applies the `IGNORE_SPACE` SQL mode\. 

#### JSON<a name="aws-properties-rds-dbparametergroup--examples----json"></a>

```
{
    "RDSDBParameterGroup": {
        "Type": "AWS::RDS::DBParameterGroup",
        "Properties": {
            "Description": "CloudFormation Sample Parameter Group",
            "Family": "aurora5.6",
            "Parameters": {
                "sql_mode": "IGNORE_SPACE"
            }
        }
    }
}
```

#### YAML<a name="aws-properties-rds-dbparametergroup--examples----yaml"></a>

```
--- 
RDSDBParameterGroup: 
  Properties: 
    Description: "CloudFormation Sample Parameter Group"
    Family: aurora5.6
    Parameters: 
      sql_mode: IGNORE_SPACE
  Type: "AWS::RDS::DBParameterGroup"
```