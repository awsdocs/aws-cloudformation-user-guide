# AWS::Glue::DataCatalogEncryptionSettings<a name="aws-resource-glue-datacatalogencryptionsettings"></a>

Sets the security configuration for a specified catalog\. After the configuration has been set, the specified encryption is applied to every catalog write thereafter\.

## Syntax<a name="aws-resource-glue-datacatalogencryptionsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-datacatalogencryptionsettings-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::DataCatalogEncryptionSettings",
  "Properties" : {
      "[CatalogId](#cfn-glue-datacatalogencryptionsettings-catalogid)" : String,
      "[DataCatalogEncryptionSettings](#cfn-glue-datacatalogencryptionsettings-datacatalogencryptionsettings)" : DataCatalogEncryptionSettings
    }
}
```

### YAML<a name="aws-resource-glue-datacatalogencryptionsettings-syntax.yaml"></a>

```
Type: AWS::Glue::DataCatalogEncryptionSettings
Properties: 
  [CatalogId](#cfn-glue-datacatalogencryptionsettings-catalogid): String
  [DataCatalogEncryptionSettings](#cfn-glue-datacatalogencryptionsettings-datacatalogencryptionsettings): 
    DataCatalogEncryptionSettings
```

## Properties<a name="aws-resource-glue-datacatalogencryptionsettings-properties"></a>

`CatalogId`  <a name="cfn-glue-datacatalogencryptionsettings-catalogid"></a>
The ID of the Data Catalog in which the settings are created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataCatalogEncryptionSettings`  <a name="cfn-glue-datacatalogencryptionsettings-datacatalogencryptionsettings"></a>
Contains configuration information for maintaining Data Catalog security\.  
*Required*: Yes  
*Type*: [DataCatalogEncryptionSettings](aws-properties-glue-datacatalogencryptionsettings-datacatalogencryptionsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-datacatalogencryptionsettings-return-values"></a>

### Ref<a name="aws-resource-glue-datacatalogencryptionsettings-return-values-ref"></a>