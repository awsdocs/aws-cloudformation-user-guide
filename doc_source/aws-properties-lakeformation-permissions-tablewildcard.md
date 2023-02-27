# AWS::LakeFormation::Permissions TableWildcard<a name="aws-properties-lakeformation-permissions-tablewildcard"></a>

A wildcard object representing every table under a database\.

## Syntax<a name="aws-properties-lakeformation-permissions-tablewildcard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-permissions-tablewildcard-syntax.json"></a>

```
{
}
```

### YAML<a name="aws-properties-lakeformation-permissions-tablewildcard-syntax.yaml"></a>

```
```

## Examples<a name="aws-properties-lakeformation-permissions-tablewildcard--examples"></a>

### Permissions on all tables in a database<a name="aws-properties-lakeformation-permissions-tablewildcard--examples--Permissions_on_all_tables_in_a_database"></a>

The following example demonstrates how to grant permissions on all tables in a database using the `TableWildcard` object\.

#### JSON<a name="aws-properties-lakeformation-permissions-tablewildcard--examples--Permissions_on_all_tables_in_a_database--json"></a>

```
"ExamplePermission": {
  "Type": "AWS::LakeFormation::Permissions",
  "Properties": {
    "DataLakePrincipal": {
      "DataLakePrincipalIdentifier": {
        "arn:sample_principal"
      }
    },
    "Resource": {
      "TableResource": {
        "DatabaseName": "example_database",
        "TableWildcard": {}
      }
    },
    "Permissions": [
      "SELECT"
    ],
    "PermissionsWithGrantOption": [
      "SELECT"
    ]
  }
}
```

#### YAML<a name="aws-properties-lakeformation-permissions-tablewildcard--examples--Permissions_on_all_tables_in_a_database--yaml"></a>

```
ExamplePermission:
  Type: AWS::LakeFormation::Permissions
  Properties:
    Principal:
      DataLakePrincipalIdentifier: "arn:sample_principal"
    Resource:
      Table:
        DatabaseName: "example_database"
        TableWildcard: { }
    Permissions: 
          - "SELECT"
    PermissionsWithGrantOption: 
          - "SELECT"
```