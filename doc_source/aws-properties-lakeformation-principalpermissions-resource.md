# AWS::LakeFormation::PrincipalPermissions Resource<a name="aws-properties-lakeformation-principalpermissions-resource"></a>

A structure for the resource\.

## Syntax<a name="aws-properties-lakeformation-principalpermissions-resource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-principalpermissions-resource-syntax.json"></a>

```
{
  "[Catalog](#cfn-lakeformation-principalpermissions-resource-catalog)" : Json,
  "[Database](#cfn-lakeformation-principalpermissions-resource-database)" : DatabaseResource,
  "[DataCellsFilter](#cfn-lakeformation-principalpermissions-resource-datacellsfilter)" : DataCellsFilterResource,
  "[DataLocation](#cfn-lakeformation-principalpermissions-resource-datalocation)" : DataLocationResource,
  "[LFTag](#cfn-lakeformation-principalpermissions-resource-lftag)" : LFTagKeyResource,
  "[LFTagPolicy](#cfn-lakeformation-principalpermissions-resource-lftagpolicy)" : LFTagPolicyResource,
  "[Table](#cfn-lakeformation-principalpermissions-resource-table)" : TableResource,
  "[TableWithColumns](#cfn-lakeformation-principalpermissions-resource-tablewithcolumns)" : TableWithColumnsResource
}
```

### YAML<a name="aws-properties-lakeformation-principalpermissions-resource-syntax.yaml"></a>

```
  [Catalog](#cfn-lakeformation-principalpermissions-resource-catalog): Json
  [Database](#cfn-lakeformation-principalpermissions-resource-database): 
    DatabaseResource
  [DataCellsFilter](#cfn-lakeformation-principalpermissions-resource-datacellsfilter): 
    DataCellsFilterResource
  [DataLocation](#cfn-lakeformation-principalpermissions-resource-datalocation): 
    DataLocationResource
  [LFTag](#cfn-lakeformation-principalpermissions-resource-lftag): 
    LFTagKeyResource
  [LFTagPolicy](#cfn-lakeformation-principalpermissions-resource-lftagpolicy): 
    LFTagPolicyResource
  [Table](#cfn-lakeformation-principalpermissions-resource-table): 
    TableResource
  [TableWithColumns](#cfn-lakeformation-principalpermissions-resource-tablewithcolumns): 
    TableWithColumnsResource
```

## Properties<a name="aws-properties-lakeformation-principalpermissions-resource-properties"></a>

`Catalog`  <a name="cfn-lakeformation-principalpermissions-resource-catalog"></a>
The identifier for the Data Catalog\. By default, the account ID\. The Data Catalog is the persistent metadata store\. It contains database definitions, table definitions, and other control information to manage your AWS Lake Formation environment\.   
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Database`  <a name="cfn-lakeformation-principalpermissions-resource-database"></a>
The database for the resource\. Unique to the Data Catalog\. A database is a set of associated table definitions organized into a logical group\. You can Grant and Revoke database permissions to a principal\.   
*Required*: No  
*Type*: [DatabaseResource](aws-properties-lakeformation-principalpermissions-databaseresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataCellsFilter`  <a name="cfn-lakeformation-principalpermissions-resource-datacellsfilter"></a>
A data cell filter\.  
*Required*: No  
*Type*: [DataCellsFilterResource](aws-properties-lakeformation-principalpermissions-datacellsfilterresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataLocation`  <a name="cfn-lakeformation-principalpermissions-resource-datalocation"></a>
The location of an Amazon S3 path where permissions are granted or revoked\.   
*Required*: No  
*Type*: [DataLocationResource](aws-properties-lakeformation-principalpermissions-datalocationresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LFTag`  <a name="cfn-lakeformation-principalpermissions-resource-lftag"></a>
The LF\-tag key and values attached to a resource\.  
*Required*: No  
*Type*: [LFTagKeyResource](aws-properties-lakeformation-principalpermissions-lftagkeyresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LFTagPolicy`  <a name="cfn-lakeformation-principalpermissions-resource-lftagpolicy"></a>
A list of LF\-tag conditions that define a resource's LF\-tag policy\.  
*Required*: No  
*Type*: [LFTagPolicyResource](aws-properties-lakeformation-principalpermissions-lftagpolicyresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Table`  <a name="cfn-lakeformation-principalpermissions-resource-table"></a>
The table for the resource\. A table is a metadata definition that represents your data\. You can Grant and Revoke table privileges to a principal\.   
*Required*: No  
*Type*: [TableResource](aws-properties-lakeformation-principalpermissions-tableresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableWithColumns`  <a name="cfn-lakeformation-principalpermissions-resource-tablewithcolumns"></a>
The table with columns for the resource\. A principal with permissions to this resource can select metadata from the columns of a table in the Data Catalog and the underlying data in Amazon S3\.  
*Required*: No  
*Type*: [TableWithColumnsResource](aws-properties-lakeformation-principalpermissions-tablewithcolumnsresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-properties-lakeformation-principalpermissions-resource--examples"></a>

### Permissions on a catalog<a name="aws-properties-lakeformation-principalpermissions-resource--examples--Permissions_on_a_catalog"></a>

The following example shows how to grant permissions on a Catalog\.

#### JSON<a name="aws-properties-lakeformation-principalpermissions-resource--examples--Permissions_on_a_catalog--json"></a>

```
{
    "SamplePermission": {
        "Type": "AWS::LakeFormation::PrincipalPermissions",
        "Properties": {
            "Resource": {
                "Catalog": {}
            },
            "Permissions": ["CREATE_DATABASE"],
            "PermissionsWithGrantOption": []
        }
    }

}
```

#### YAML<a name="aws-properties-lakeformation-principalpermissions-resource--examples--Permissions_on_a_catalog--yaml"></a>

```
SamplePermission:
    Type: AWS::LakeFormation::PrincipalPermissions
    Properties:
      Principal:
        DataLakePrincipalIdentifier: "arn:sample_principal"
      Resource:
        Catalog: {}
      Permissions:
        - "CREATE_DATABASE"

      PermissionsWithGrantOption: []
```