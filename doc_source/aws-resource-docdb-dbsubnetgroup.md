# AWS::DocDB::DBSubnetGroup<a name="aws-resource-docdb-dbsubnetgroup"></a>

The `AWS::DocDB::DBSubnetGroup` Amazon DocumentDB resource describes a DBSubnetGroup\. For more information, see [DBSubnetGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBSubnetGroup.html) in the *Amazon DocumentDB Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-docdb-dbsubnetgroup-syntax)
+ [Properties](#aws-resource-docdb-dbsubnetgroup-properties)
+ [Return Values](#aws-resource-docdb-dbsubnetgroup-returnvalues)
+ [Example](#aws-resource-docdb-dbsubnetgroup-examples)
+ [See Also](#aws-resource-docdb-dbsubnetgroup-seealso)

## Syntax<a name="aws-resource-docdb-dbsubnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-docdb-dbsubnetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::DocDB::DBSubnetGroup",
  "Properties" : {
    "[DBSubnetGroupDescription](#cfn-docdb-dbsubnetgroup-dbsubnetgroupdescription)" : String,
    "[DBSubnetGroupName](#cfn-docdb-dbsubnetgroup-dbsubnetgroupname)" : String,
    "[SubnetIds](#cfn-docdb-dbsubnetgroup-subnetids)" : [ String, ... ],
    "[Tags](#cfn-docdb-dbsubnetgroup-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-docdb-dbsubnetgroup-syntax.yaml"></a>

```
Type: "AWS::DocDB::DBSubnetGroup"
Properties:
  [DBSubnetGroupDescription](#cfn-docdb-dbsubnetgroup-dbsubnetgroupdescription): String
  [DBSubnetGroupName](#cfn-docdb-dbsubnetgroup-dbsubnetgroupname): String
  [SubnetIds](#cfn-docdb-dbsubnetgroup-subnetids): 
    - String
  [Tags](#cfn-docdb-dbsubnetgroup-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-docdb-dbsubnetgroup-properties"></a>

`DBSubnetGroupDescription`  <a name="cfn-docdb-dbsubnetgroup-dbsubnetgroupdescription"></a>
The description of the DB subnet group\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DBSubnetGroupName`  <a name="cfn-docdb-dbsubnetgroup-dbsubnetgroupname"></a>
The name of the DB subnet group\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SubnetIds`  <a name="cfn-docdb-dbsubnetgroup-subnetids"></a>
List of subnet identifiers\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-docdb-dbsubnetgroup-tags"></a>
A list of up to 50 tags\. A tag is metadata assigned to an Amazon DocumentDB \(with MongoDB compatibility\) resource consisting of a key\-value pair\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-docdb-dbsubnetgroup-returnvalues"></a>

### Ref<a name="aws-resource-docdb-dbsubnetgroup-ref"></a>

When you pass the logical ID of an `AWS::DocDB::DBSubnetGroup` to the intrinsic `Ref` function, the function returns the name of the DBSubnetGroup, such as `default`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Example<a name="aws-resource-docdb-dbsubnetgroup-examples"></a>

### JSON<a name="aws-resource-docdb-dbsubnetgroup-example1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDBSubnetGroup" : {
         "Type" : "AWS::DocDB::DBSubnetGroup",
         "Properties" : {
            "DBSubnetGroupDescription" : "description",
            "SubnetIds" : [ "subnet-7b5b4112", "subnet-7b5b4115" ],
            "Tags" : [ {"Key" : "String", "Value" : "String"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-docdb-dbsubnetgroup-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDBSubnetGroup: 
    Type: "AWS::DocDB::DBSubnetGroup"
    Properties: 
      DBSubnetGroupDescription: "description"
      SubnetIds: 
        - "subnet-7b5b4112"
        - "subnet-7b5b4115"
      Tags: 
        - 
          Key: "String"
          Value: "String"
```

## See Also<a name="aws-resource-docdb-dbsubnetgroup-seealso"></a>

For more information, see the following topics in the *Amazon DocumentDB \(with MongoDB compatibility\) Developer Guide*\.****
+ [DBSubnetGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBSubnetGroup.html)
+ [Subnet](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_Subnet.html)
+ [CreateDBSubnetGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_CreateDBSubnetGroup.html)
+ [DeleteDBSubnetGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DeleteDBSubnetGroup.html)
+ [DescribeDBSubnetGroups](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DescribeDBSubnetGroups.html)
+ [ModifyDBSubnetGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_ModifyDBSubnetGroup.html)