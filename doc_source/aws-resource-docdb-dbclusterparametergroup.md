# AWS::DocDB::DBClusterParameterGroup<a name="aws-resource-docdb-dbclusterparametergroup"></a>

The `AWS::DocDB::DBClusterParameterGroup` Amazon DocumentDB \(with MongoDB compatibility\) resource describes a DBClusterParameterGroup\. For more information, see [DBClusterParameterGroup](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DBClusterParameterGroup.html) in the *Amazon DocumentDB Developer Guide*\.

Parameters in a DB cluster parameter group apply to all of the instances in a DB cluster\.

A DB cluster parameter group is initially created with the default parameters for the database engine used by instances in the DB cluster\. To provide custom values for any of the parameters, you must modify the group after you create it\. After you create a DB cluster parameter group, you must associate it with your DB cluster\. For the new DB cluster parameter group and associated settings to take effect, you must then reboot the DB instances in the DB cluster without failover\.

**Important**  
After you create a DB cluster parameter group, you should wait at least 5 minutes before creating your first DB cluster that uses that DB cluster parameter group as the default parameter group\. This allows Amazon DocumentDB to fully complete the create action before the DB cluster parameter group is used as the default for a new DB cluster\. This step is especially important for parameters that are critical when creating the default database for a DB cluster, such as the character set for the default database defined by the `character_set_database` parameter\.

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
      "[Tags](#cfn-docdb-dbclusterparametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-docdb-dbclusterparametergroup-syntax.yaml"></a>

```
Type: AWS::DocDB::DBClusterParameterGroup
Properties: 
  [Description](#cfn-docdb-dbclusterparametergroup-description): String
  [Family](#cfn-docdb-dbclusterparametergroup-family): String
  [Name](#cfn-docdb-dbclusterparametergroup-name): String
  [Parameters](#cfn-docdb-dbclusterparametergroup-parameters): Json
  [Tags](#cfn-docdb-dbclusterparametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-docdb-dbclusterparametergroup-properties"></a>

`Description`  <a name="cfn-docdb-dbclusterparametergroup-description"></a>
The description for the DB cluster parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Family`  <a name="cfn-docdb-dbclusterparametergroup-family"></a>
The DB cluster parameter group family name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-docdb-dbclusterparametergroup-name"></a>
The name of the DB cluster parameter group\.  
Constraints:  
+ Must match the name of an existing `DBClusterParameterGroup`\.
This value is stored as a lowercase string\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-docdb-dbclusterparametergroup-parameters"></a>
Provides a list of parameters for the DB cluster parameter group\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-docdb-dbclusterparametergroup-tags"></a>
The tags to be assigned to the DB cluster parameter group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-docdb-dbclusterparametergroup-return-values"></a>

### Ref<a name="aws-resource-docdb-dbclusterparametergroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DBClusterParameterGroup's name, such as `sample-db-cluster-param-group`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-docdb-dbclusterparametergroup--examples"></a>

### <a name="aws-resource-docdb-dbclusterparametergroup--examples--"></a>

#### JSON<a name="aws-resource-docdb-dbclusterparametergroup--examples----json"></a>

```
{
   "Type" : "AWS::DocDB::DBClusterParameterGroup",
   "Properties" : {
      "Description" : String,
      "Family" : String,
      "Name" : String,
      "Parameters" : Json,
      "Tags" : [ Tag, ... ]
   }
}
```

#### YAML<a name="aws-resource-docdb-dbclusterparametergroup--examples----yaml"></a>

```
Type: "AWS::DocDB::DBClusterParameterGroup"
Properties:
   Description: String
   Family: String
   Name: String
   Parameters: Json
   Tags: 
      - Tag
```

## See Also<a name="aws-resource-docdb-dbclusterparametergroup--seealso"></a>
+  [DBClusterParameterGroup](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DBClusterParameterGroup.html) 
+  [CreateDBClusterParameterGroup](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_CreateDBClusterParameterGroup.html) 
+  [DeleteDBClusterParameterGroup](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DeleteDBClusterParameterGroup.html) 
+  [DescribeDBClusterParameterGroups](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DescribeDBClusterParameterGroups.html) 
+  [ModifyDBClusterParameterGroup](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_ModifyDBClusterParameterGroup.html) 