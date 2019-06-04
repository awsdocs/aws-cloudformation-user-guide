# AWS::RDS::DBClusterParameterGroup<a name="aws-resource-rds-dbclusterparametergroup"></a>

The `AWS::RDS::DBClusterParameterGroup` resource creates a new Amazon RDS DB cluster parameter group\. For more information, see [Managing an Amazon Aurora DB Cluster](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_Aurora.html) in the *Amazon Aurora User Guide*\.

**Note**  
If you apply a parameter group to a DB cluster, then its DB instances might need to reboot\. This can result in an outage while the instances are rebooting\.

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
Provides the name of the DB parameter group family that this DB cluster parameter group is compatible with\.  
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

## Return Values<a name="aws-resource-rds-dbclusterparametergroup-return-values"></a>

### Ref<a name="aws-resource-rds-dbclusterparametergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB cluster parameter group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-rds-dbclusterparametergroup--examples"></a>

### <a name="aws-resource-rds-dbclusterparametergroup--examples--"></a>

The following snippet creates a parameter group that sets the character set database to `UTF32`: 

#### JSON<a name="aws-resource-rds-dbclusterparametergroup--examples----json"></a>

```
{
    "RDSDBClusterParameterGroup": {
        "Type": "AWS: : RDS: : DBClusterParameterGroup",
        "Properties": {
            "Parameters": {
                "character_set_database": "utf32"
            },
            "Family": "aurora5.6",
            "Description": "Asampleparametergroup"
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbclusterparametergroup--examples----yaml"></a>

```
--- 
RDSDBClusterParameterGroup: 
  Properties: 
    Description: "A sample parameter group"
    Family: aurora5.6
    Parameters: 
      character_set_database: utf32
  Type: "AWS::RDS::DBClusterParameterGroup"
```