# AWS::DocDB::DBClusterParameterGroup<a name="aws-resource-docdb-dbclusterparametergroup"></a>

The `AWS::DocDB::DBClusterParameterGroup` Amazon DocumentDB \(with MongoDB compatibility\) resource describes a DBClusterParameterGroup\. For more information, see [DBClusterParameterGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBClusterParameterGroup) in the *Amazon DocumentDB Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-docdb-dbclusterparametergroup-syntax)
+ [Properties](#aws-resource-docdb-dbclusterparametergroup-properties)
+ [Return Values](#aws-resource-docdb-dbclusterparametergroup-returnvalues)
+ [Example](#aws-resource-docdb-dbclusterparametergroup-examples)
+ [See Also](#aws-resource-docdb-dbclusterparametergroup-seealso)

## Syntax<a name="aws-resource-docdb-dbclusterparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-docdb-dbclusterparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::DocDB::DBClusterParameterGroup",
  "Properties" : {
    "[Description](#cfn-docdb-dbclusterparametergroup-description)" : String,
    "[Family](#cfn-docdb-dbclusterparametergroup-family)" : String,
    "[Name](#cfn-docdb-dbclusterparametergroup-name)" : String,
    "[Parameters](#cfn-docdb-dbclusterparametergroup-parameters)" : Json,
    "[Tags](#cfn-docdb-dbclusterparametergroup-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-docdb-dbclusterparametergroup-syntax.yaml"></a>

```
Type: "AWS::DocDB::DBClusterParameterGroup"
Properties:
  [Description](#cfn-docdb-dbclusterparametergroup-description): String
  [Family](#cfn-docdb-dbclusterparametergroup-family): String
  [Name](#cfn-docdb-dbclusterparametergroup-name): String
  [Parameters](#cfn-docdb-dbclusterparametergroup-parameters): Json
  [Tags](#cfn-docdb-dbclusterparametergroup-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-docdb-dbclusterparametergroup-properties"></a>

`Description`  <a name="cfn-docdb-dbclusterparametergroup-description"></a>
Provides the customer\-specified description for this DB cluster parameter group\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Family`  <a name="cfn-docdb-dbclusterparametergroup-family"></a>
The DB cluster parameter group from which user created DB cluster parameter groups are created\. For example, `default.docdb3.6`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-docdb-dbclusterparametergroup-name"></a>
Provides the name of the DB parameter group family that this DB cluster parameter group is compatible with\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Parameters`  <a name="cfn-docdb-dbclusterparametergroup-parameters"></a>
Provides the name of the DB cluster parameter group\.  
 *Required*: Yes  
 *Type*: Json  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-docdb-dbclusterparametergroup-tags"></a>
A list of up to 50 tags\. A tag is metadata assigned to an Amazon DocumentDB resource consisting of a key\-value pair\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-docdb-dbclusterparametergroup-returnvalues"></a>

### Ref<a name="aws-resource-docdb-dbclusterparametergroup-ref"></a>

When you pass the logical ID of an `AWS::DocDB::DBClusterParameterGroup` resource to the intrinsic `Ref` function, the function returns the DBClusterParameterGroup's name, such as `sample-db-cluster-param-group`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Example<a name="aws-resource-docdb-dbclusterparametergroup-examples"></a>

### JSON<a name="aws-resource-docdb-dbclusterparametergroup-example1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDBInstance" : {
         "Type" : "AWS::DocDB::DBClusterParameterGroup",
         "Properties" : {
            "Description" : "description",
            "Family" : "docdb3.6",
            "Name" : "modified-docdb3.6",
            "Parameters" : [ {"Name" : "String", "Value" : "String"} ],
            "Tags" : [ {"Key" : "String", "Value" : "String"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-docdb-dbclusterparametergroup-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDBInstance: 
    Type: "AWS::DocDB::DBClusterParameterGroup"
    Properties: 
      Description : "description"
      Family : "docdb3.6"
      Name : "modified-docdb3.6"
      Parameters : 
        - 
          Name : "String"
          Value : "String"
      Tags: 
        - 
          Key: "String"
          Value: "String"
```

## See Also<a name="aws-resource-docdb-dbclusterparametergroup-seealso"></a>

For more information, see the following topics in the *Amazon DocumentDB Developers Guide*\.
+ [DBClusterParameterGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DBClusterParameterGroup)
+ [CreateDBClusterParameterGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_CreateDBClusterParameterGroup)
+ [DeleteDBClusterParameterGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DeleteDBClusterParameterGroup)
+ [DescribeDBClusterParameterGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_DescribeDBClusterParameterGroup)
+ [ModifyDBClusterParameterGroup](https://docs.aws.amazon.com/amazondocdb/latest/developerguide/API_ModifyDBClusterParameterGroup)