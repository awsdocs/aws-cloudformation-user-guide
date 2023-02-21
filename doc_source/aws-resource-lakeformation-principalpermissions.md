# AWS::LakeFormation::PrincipalPermissions<a name="aws-resource-lakeformation-principalpermissions"></a>

 The `AWS::LakeFormation::PrincipalPermissions` resource represents the permissions that a principal has on a Data Catalog resource \(such as AWS Glue databases or AWS Glue tables\)\. When you create a `PrincipalPermissions` resource, the permissions are granted via the AWS Lake Formation `GrantPermissions` API operation\. When you delete a `PrincipalPermissions` resource, the permissions on principal\-resource pair are revoked via the AWS Lake Formation `RevokePermissions` API operation\. 

## Syntax<a name="aws-resource-lakeformation-principalpermissions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-principalpermissions-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::PrincipalPermissions",
  "Properties" : {
      "[Catalog](#cfn-lakeformation-principalpermissions-catalog)" : String,
      "[Permissions](#cfn-lakeformation-principalpermissions-permissions)" : [ String, ... ],
      "[PermissionsWithGrantOption](#cfn-lakeformation-principalpermissions-permissionswithgrantoption)" : [ String, ... ],
      "[Principal](#cfn-lakeformation-principalpermissions-principal)" : DataLakePrincipal,
      "[Resource](#cfn-lakeformation-principalpermissions-resource)" : Resource
    }
}
```

### YAML<a name="aws-resource-lakeformation-principalpermissions-syntax.yaml"></a>

```
Type: AWS::LakeFormation::PrincipalPermissions
Properties: 
  [Catalog](#cfn-lakeformation-principalpermissions-catalog): String
  [Permissions](#cfn-lakeformation-principalpermissions-permissions): 
    - String
  [PermissionsWithGrantOption](#cfn-lakeformation-principalpermissions-permissionswithgrantoption): 
    - String
  [Principal](#cfn-lakeformation-principalpermissions-principal): 
    DataLakePrincipal
  [Resource](#cfn-lakeformation-principalpermissions-resource): 
    Resource
```

## Properties<a name="aws-resource-lakeformation-principalpermissions-properties"></a>

`Catalog`  <a name="cfn-lakeformation-principalpermissions-catalog"></a>
 The identifier for the Data Catalog\. By default, the account ID\. The Data Catalog is the persistent metadata store\. It contains database definitions, table definitions, and other control information to manage your Lake Formation environment\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Permissions`  <a name="cfn-lakeformation-principalpermissions-permissions"></a>
The permissions granted or revoked\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PermissionsWithGrantOption`  <a name="cfn-lakeformation-principalpermissions-permissionswithgrantoption"></a>
Indicates the ability to grant permissions \(as a subset of permissions granted\)\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Principal`  <a name="cfn-lakeformation-principalpermissions-principal"></a>
The principal to be granted a permission\.  
*Required*: Yes  
*Type*: [DataLakePrincipal](aws-properties-lakeformation-principalpermissions-datalakeprincipal.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Resource`  <a name="cfn-lakeformation-principalpermissions-resource"></a>
The resource to be granted or revoked permissions\.  
*Required*: Yes  
*Type*: [Resource](aws-properties-lakeformation-principalpermissions-resource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lakeformation-principalpermissions-return-values"></a>

### Ref<a name="aws-resource-lakeformation-principalpermissions-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the primary identifier of the resource\. The primary identifier of the resource is a combination of `ResourceIdentifier` and `PrincipalIdentifier` separated by a pipe\.

For example: `{"DataLakePrincipalIdentifier":"arn:aws:iam::123456789012:role/ExampleRole"}|{"Catalog":null,"Database":null,"Table":null,"TableWithColumns":null,"DataLocation":null,"DataCellsFilter":{"TableCatalogId":"123456789012","DatabaseName":"ExampleDatabase","TableName":"ExampleTable","Name":"ExampleFilter"},"LFTag":null,"LFTagPolicy":null}` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lakeformation-principalpermissions-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lakeformation-principalpermissions-return-values-fn--getatt-fn--getatt"></a>

`PrincipalIdentifier`  <a name="PrincipalIdentifier-fn::getatt"></a>
Json encoding of the input principal\. For example: `{"DataLakePrincipalIdentifier":"arn:aws:iam::123456789012:role/ExampleRole"}` 

`ResourceIdentifier`  <a name="ResourceIdentifier-fn::getatt"></a>
Json encoding of the input resource\. For example: `{"Catalog":null,"Database":null,"Table":null,"TableWithColumns":null,"DataLocation":null,"DataCellsFilter":{"TableCatalogId":"123456789012","DatabaseName":"ExampleDatabase","TableName":"ExampleTable","Name":"ExampleFilter"},"LFTag":null,"LFTagPolicy":null}`

## Remarks<a name="aws-resource-lakeformation-principalpermissions--remarks"></a>

When you delete a `PrincipalPermissions` resource, AWS Lake Formation revokes all permissions \(even manually granted ones\) that the principal has on the resource\.

CloudFormation resources must have a one\-to\-one mapping between a defined resource \(an AWS Lake Formation permission\) and the primary identifier \(a combination of AWS Lake Formation resource and AWS Lake Formation principal for which this permission is being granted\)\. Due to this limitation, the current implementation of `PrincipalPermissions` has the following behavior for permissions on `TableWithColumns` resources:
+ When you create a `TableWithColumn` permissions resource, CloudFormation will first check whether the principal already has any permissions on the underlying resource\. CloudFormation will create the resource only if there is no previous permission associated to the specific principal for the same resource identifier\. If there exists a permission resource with the same combination, the request will fail with the `AlreadyExistsException` error\.
**Note**  
This limitation is also applicable to having a `SELECT` permission on the table since that is effectively a `SELECT` permission on a `ColumnWildcard` in a `TableWithColumns` resource\.

## Examples<a name="aws-resource-lakeformation-principalpermissions--examples"></a>

### Permissions on a database<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_a_database"></a>

The following example demonstrates how to grant permissions on a `Database` resource:

#### JSON<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_a_database--json"></a>

```
{
    "SamplePermission": {
    "Type": "AWS::LakeFormation::PrincipalPermissions",
        "Properties": {
            "Principal": {
                "DataLakePrincipalIdentifier": " "arn:sample_principal"
            },
            "Resource": {
                "Database": {
                    "CatalogId": "12345678910",
                    "Name": "sample_db"
                }
            },
            "Permissions": ["CREATE_TABLE", "ALTER", "DROP", "DESCRIBE"],
            "PermissionsWithGrantOption": ["CREATE_TABLE", "ALTER", "DROP", "DESCRIBE"]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_a_database--yaml"></a>

```
SamplePermission:
    Type: AWS::LakeFormation::PrincipalPermissions
    Properties:
      Principal:
        DataLakePrincipalIdentifier: "arn:sample_principal"
      Resource:
        Database:
          CatalogId: "12345678910"
          Name: "sample_db"
      Permissions:
        - "CREATE_TABLE" 
        - "ALTER" 
        - "DROP"
        - "DESCRIBE"
      PermissionsWithGrantOption:
        - "CREATE_TABLE" 
        - "ALTER" 
        - "DROP"
        - "DESCRIBE"
```

### Permissions on a table<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_a_table"></a>

The following example demonstrates how to grant permissions on a `Table` resource:

#### JSON<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_a_table--json"></a>

```
{
    "SamplePermission": {
    "Type": "AWS::LakeFormation::PrincipalPermissions",
        "Properties": {
            "Principal": {
                "DataLakePrincipalIdentifier": " "arn:sample_principal"
            },
            "Resource": {
                "Table": {
                    "CatalogId": "12345678910",
                    "DatabaseName": "sample_db",
                    "Name": "sample_tbl"
                }
            },
            "Permissions": ["SELECT", "INSERT", "DELETE", "ALTER", "DROP", "DESCRIBE"],
            "PermissionsWithGrantOption": ["SELECT", "INSERT", "DELETE", "ALTER", "DROP", "DESCRIBE"]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_a_table--yaml"></a>

```
SamplePermission:
    Type: AWS::LakeFormation::PrincipalPermissions
    Properties:
      Principal:
        DataLakePrincipalIdentifier: "arn:sample_principal"
      Resource:
        Table:
          CatalogId: "12345678910"
          DatabaseName: "sample_db"
          Name: "sample_tbl"
      Permissions:
        - "SELECT"
        - "INSERT"
        - "DELETE" 
        - "ALTER" 
        - "DROP"
        - "DESCRIBE"
      PermissionsWithGrantOption:
        - "SELECT"
        - "INSERT"
        - "DELETE" 
        - "ALTER" 
        - "DROP"
        - "DESCRIBE"
```

### Permissions on columns<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_columns"></a>

The following example demonstrates how to grant permissions on a `TableWithColumns` resource:

#### JSON<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_columns--json"></a>

```
{
    "SamplePermission": {
    "Type": "AWS::LakeFormation::PrincipalPermissions",
        "Properties": {
            "Principal": {
                "DataLakePrincipalIdentifier": " "arn:sample_principal"
            },
            "Resource": {
                "TableWithColumns": {
                    "CatalogId": "12345678910",
                    "DatabaseName": "sample_db",
                    "Name": "sample_tbl",
                    "ColumnNames": ["sample_col1", "sample_col2"]
                }
            },
            "Permissions": ["SELECT"],
            "PermissionsWithGrantOption": ["SELECT"]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-principalpermissions--examples--Permissions_on_columns--yaml"></a>

```
SamplePermission:
    Type: AWS::LakeFormation::PrincipalPermissions
    Properties:
      Principal:
        DataLakePrincipalIdentifier: "arn:sample_principal"
      Resource:
        TableWithColumns:
          CatalogId: "12345678910"
          DatabaseName: "sample_db"
          Name: "sample_tbl"
          ColumnNames:
            - "sample_col1"
      Permissions:
        - "SELECT"
      PermissionsWithGrantOption:
        - "SELECT"
```