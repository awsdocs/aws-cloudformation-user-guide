# AWS::DocDB::DBInstance<a name="aws-resource-docdb-dbinstance"></a>

The `AWS::DocDB::DBInstance` Amazon DocumentDB \(with MongoDB compatibility\) resource describes a DBInstance\. For more information, see [DBInstance](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBInstance) in the *Amazon DocumentDB Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-docdb-dbinstance-syntax)
+ [Properties](#aws-resource-docdb-dbinstance-properties)
+ [Return Values](#aws-resource-docdb-dbinstance-returnvalues)
+ [Example](#aws-resource-docdb-dbinstance-examples)
+ [See Also](#aws-resource-docdb-dbinstance-seealso)

## Syntax<a name="aws-resource-docdb-dbinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-docdb-dbinstance-syntax.json"></a>

```
{
  "Type" : "AWS::DocDB::DBInstance",
  "Properties" : {
    "[AutoMinorVersionUpgrade](#cfn-docdb-dbinstance-autominorversionupgrade)" : Boolean,
    "[AvailabilityZone](#cfn-docdb-dbinstance-availabilityzone)" : String,
    "[DBClusterIdentifier](#cfn-docdb-dbinstance-dbclusteridentifier)" : String,
    "[DBInstanceClass](#cfn-docdb-dbinstance-dbinstanceclass)" : String,
    "[DBInstanceIdentifier](#cfn-docdb-dbinstance-dbinstanceidentifier)" : String,
    "[PreferredMaintenanceWindow](#cfn-docdb-dbinstance-preferredmaintenancewindow)" : String,
    "[Tags](#cfn-docdb-dbinstance-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-docdb-dbinstance-syntax.yaml"></a>

```
Type: "AWS::DocDB::DBInstance"
Properties:
  [AutoMinorVersionUpgrade](#cfn-docdb-dbinstance-autominorversionupgrade): Boolean
  [AvailabilityZone](#cfn-docdb-dbinstance-availabilityzone): String
  [DBClusterIdentifier](#cfn-docdb-dbinstance-dbclusteridentifier): String
  [DBInstanceClass](#cfn-docdb-dbinstance-dbinstanceclass): String
  [DBInstanceIdentifier](#cfn-docdb-dbinstance-dbinstanceidentifier): String
  [PreferredMaintenanceWindow](#cfn-docdb-dbinstance-preferredmaintenancewindow): String
  [Tags](#cfn-docdb-dbinstance-tags):
    - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-docdb-dbinstance-properties"></a>

`AutoMinorVersionUpgrade`  <a name="cfn-docdb-dbinstance-autominorversionupgrade"></a>
Indicates that minor version patches are applied automatically\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AvailabilityZone`  <a name="cfn-docdb-dbinstance-availabilityzone"></a>
Specifies the name of the Availability Zone the DB instance is located in\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DBClusterIdentifier`  <a name="cfn-docdb-dbinstance-dbclusteridentifier"></a>
Specifies the DB cluster this DB instance is a member of\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DBInstanceClass`  <a name="cfn-docdb-dbinstance-dbinstanceclass"></a>
Contains the name of the compute and memory capacity class of the DB instance\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Some interruption](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt) 

`DBInstanceIdentifier`  <a name="cfn-docdb-dbinstance-dbinstanceidentifier"></a>
The unique identifier for this DB instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`PreferredMaintenanceWindow`  <a name="cfn-docdb-dbinstance-preferredmaintenancewindow"></a>
Specifies the weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-docdb-dbinstance-tags"></a>
A list of up to 50 tags\. A tag is metadata assigned to an Amazon DocumentDB \(with MongoDB compatibility\) resource consisting of a key\-value pair\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-docdb-dbinstance-returnvalues"></a>

### Ref<a name="aws-resource-docdb-dbinstance-ref"></a>

When you pass the logical ID of an `AWS::DocDB::DBInstance` resource to the intrinsic `Ref` function, the function returns the DBInstanceIdentifier, such as `sample-db-instance`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-docdb-dbinstance-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Endpoint`  
The connection endpoint for the DB instance\. For example: `sample-cluster.cluster-abcdefghijkl.us-east-1.docdb.amazonaws.com`\.

`Port`  
The port number on which the database accepts connections, such as `27017`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Example<a name="aws-resource-docdb-dbinstance-examples"></a>

### JSON<a name="aws-resource-docdb-dbinstance-example1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDBInstance" : {
         "Type" : "AWS::DocDB::DBInstance",
         "Properties" : {
            "AutoMinorVersionUpgrade" : "true",
            "Availabilityzone" : "us-east-1a",
            "DBClusterIdentifier" : "sample-cluster",
            "DBInstanceClass" : "db.r4.large",
            "DBInstanceIdentifier" : "sample-instance",
            "PreferredMaintenanceWindow" : "sat:04:51-sat:05:21",
            "Tags" : [ {"Key" : "String", "Value" : "String"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-docdb-dbinstance-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDBInstance: 
    Type: "AWS::DocDB::DBInstance"
    Properties: 
      AutoMinorVersionUpgrade: true
      AvailabilityZone: "us-east-1a"
      DBClusterIdentifier: "sample-cluster"
      DBInstanceClass: "db.r4.large"
      DBInstanceIdentifier: "sample-instance"
      PreferredMaintenanceWindow: "sat:04:51-sat:05:21"
      Tags: 
        - 
          Key: "String"
          Value: "String"
```

## See Also<a name="aws-resource-docdb-dbinstance-seealso"></a>

For more information, see the following topics in the *Amazon DocumentDB Developers Guide*\.
+ [DBInstance](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBInstance)
+ [CreateDBInstance](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_CreateDBInstance)
+ [DeleteDBInstance](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DeleteDBInstance)
+ [DescribeDBInstances](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DescribeDBInstances)
+ [ModifyDBInstance](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_ModifyDBInstance)