# AWS::LakeFormation::Permissions Resource<a name="aws-properties-lakeformation-permissions-resource"></a>

A structure for the resource\.

## Syntax<a name="aws-properties-lakeformation-permissions-resource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-permissions-resource-syntax.json"></a>

```
{
  "[DatabaseResource](#cfn-lakeformation-permissions-resource-databaseresource)" : DatabaseResource,
  "[DataLocationResource](#cfn-lakeformation-permissions-resource-datalocationresource)" : DataLocationResource,
  "[TableResource](#cfn-lakeformation-permissions-resource-tableresource)" : TableResource,
  "[TableWithColumnsResource](#cfn-lakeformation-permissions-resource-tablewithcolumnsresource)" : TableWithColumnsResource
}
```

### YAML<a name="aws-properties-lakeformation-permissions-resource-syntax.yaml"></a>

```
  [DatabaseResource](#cfn-lakeformation-permissions-resource-databaseresource): 
    DatabaseResource
  [DataLocationResource](#cfn-lakeformation-permissions-resource-datalocationresource): 
    DataLocationResource
  [TableResource](#cfn-lakeformation-permissions-resource-tableresource): 
    TableResource
  [TableWithColumnsResource](#cfn-lakeformation-permissions-resource-tablewithcolumnsresource): 
    TableWithColumnsResource
```

## Properties<a name="aws-properties-lakeformation-permissions-resource-properties"></a>

`DatabaseResource`  <a name="cfn-lakeformation-permissions-resource-databaseresource"></a>
A structure for the database object\.  
*Required*: No  
*Type*: [DatabaseResource](aws-properties-lakeformation-permissions-databaseresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLocationResource`  <a name="cfn-lakeformation-permissions-resource-datalocationresource"></a>
Currently not supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [DataLocationResource](aws-properties-lakeformation-permissions-datalocationresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableResource`  <a name="cfn-lakeformation-permissions-resource-tableresource"></a>
A structure for the table object\. A table is a metadata definition that represents your data\. You can Grant and Revoke table privileges to a principal\.  
*Required*: No  
*Type*: [TableResource](aws-properties-lakeformation-permissions-tableresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableWithColumnsResource`  <a name="cfn-lakeformation-permissions-resource-tablewithcolumnsresource"></a>
Currently not supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [TableWithColumnsResource](aws-properties-lakeformation-permissions-tablewithcolumnsresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)