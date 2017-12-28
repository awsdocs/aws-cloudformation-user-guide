# AWS::RDS::DBClusterParameterGroup<a name="aws-resource-rds-dbclusterparametergroup"></a>

The `AWS::RDS::DBClusterParameterGroup` resource creates a new Amazon Relational Database Service \(Amazon RDS\) database \(DB\) cluster parameter group\. For more information about DB cluster parameter groups, see [Appendix: DB Cluster and DB Instance Parameters](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Aurora.Appendix.ParameterGroups.html) in the *Amazon Relational Database Service User Guide*\.

**Note**  
Applying a parameter group to a DB cluster might require instances to reboot, resulting in a database outage while the instances reboot\.


+ [Syntax](#aws-resource-rds-dbclusterparametergroup-syntax)
+ [Properties](#w3ab2c21c10d879c11)
+ [Return Values](#w3ab2c21c10d879c13)
+ [Example](#w3ab2c21c10d879c15)

## Syntax<a name="aws-resource-rds-dbclusterparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbclusterparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBClusterParameterGroup",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-family)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-parameters)" : DBParameters,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-rds-dbclusterparametergroup-syntax.yaml"></a>

```
Type: "AWS::RDS::DBClusterParameterGroup"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-family): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-parameters): DBParameters
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbclusterparametergroup-tags):
    Resource Tag
```

## Properties<a name="w3ab2c21c10d879c11"></a>

`Description`  
A friendly description for this DB cluster parameter group\.  
*Required: *Yes  
*Type:* String  
*Update requires*: Replacement

`Family`  
The database family of this DB cluster parameter group, such as `aurora5.6`\.  
*Required: *Yes  
*Type:* String  
*Update requires*: Replacement

`Parameters`  
The parameters to set for this DB cluster parameter group\. For a list of parameter keys, see [Appendix: DB Cluster and DB Instance Parameters](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Aurora.Appendix.ParameterGroups.html) in the *Amazon Relational Database Service User Guide*\.  
Changes to dynamic parameters are applied immediately\. Changes to static parameters require a reboot without failover to the DB instance that is associated with the parameter group before the change can take effect\.  
*Required: *Yes  
*Type:* A JSON object consisting of string key\-value pairs, as shown in the following example:  

```
"Parameters" : {
   "Key1" : "Value1",
   "Key2" : "Value2",
   "Key3" : "Value3"
}
```
*Update requires*: No interruption or some interruptions, depending on the parameters that you update\.

`Tags`  
The tags that you want to attach to this parameter group\.  
*Required: *No  
*Type*: A list of resource tags  
*Update requires*: Updates are not supported\.

## Return Values<a name="w3ab2c21c10d879c13"></a>

### Ref<a name="w3ab2c21c10d879c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d879c15"></a>

The following snippet creates a parameter group that sets the character set database to UTF32:

### JSON<a name="aws-resource-rds-dbclusterparametergroup-example.json"></a>

```
"RDSDBClusterParameterGroup" : {
  "Type" : "AWS::RDS::DBClusterParameterGroup",
  "Properties" : {
    "Parameters" : {
      "character_set_database" : "utf32"
    },
    "Family" : "aurora5.6",
    "Description" : "A sample parameter group"
  }
}
```

### YAML<a name="aws-resource-rds-dbclusterparametergroup-example.yaml"></a>

```
RDSDBClusterParameterGroup: 
  Type: "AWS::RDS::DBClusterParameterGroup"
  Properties: 
    Parameters: 
      character_set_database: "utf32"
    Family: "aurora5.6"
    Description: "A sample parameter group"
```