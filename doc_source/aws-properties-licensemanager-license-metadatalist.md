# AWS::LicenseManager::License MetadataList<a name="aws-properties-licensemanager-license-metadatalist"></a>

The `MetadataList` property type defines the list of metadata\.

## Syntax<a name="aws-properties-licensemanager-license-metadatalist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-metadatalist-syntax.json"></a>

```
{
  "[MetadataList](#cfn-licensemanager-license-metadatalist-metadatalist)" : [ Metadata, ... ]
}
```

### YAML<a name="aws-properties-licensemanager-license-metadatalist-syntax.yaml"></a>

```
  [MetadataList](#cfn-licensemanager-license-metadatalist-metadatalist): 
    - Metadata
```

## Properties<a name="aws-properties-licensemanager-license-metadatalist-properties"></a>

`MetadataList`  <a name="cfn-licensemanager-license-metadatalist-metadatalist"></a>
The list of metadata\.  
*Required*: No  
*Type*: [List](#aws-properties-licensemanager-license-metadatalist) of [Metadata](aws-properties-licensemanager-license-metadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)