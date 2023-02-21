# AWS::AppFlow::Flow MetadataCatalogConfig<a name="aws-properties-appflow-flow-metadatacatalogconfig"></a>

Specifies the configuration that Amazon AppFlow uses when it catalogs your data\. When Amazon AppFlow catalogs your data, it stores metadata in a data catalog\.

## Syntax<a name="aws-properties-appflow-flow-metadatacatalogconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-metadatacatalogconfig-syntax.json"></a>

```
{
  "[GlueDataCatalog](#cfn-appflow-flow-metadatacatalogconfig-gluedatacatalog)" : GlueDataCatalog
}
```

### YAML<a name="aws-properties-appflow-flow-metadatacatalogconfig-syntax.yaml"></a>

```
  [GlueDataCatalog](#cfn-appflow-flow-metadatacatalogconfig-gluedatacatalog): 
    GlueDataCatalog
```

## Properties<a name="aws-properties-appflow-flow-metadatacatalogconfig-properties"></a>

`GlueDataCatalog`  <a name="cfn-appflow-flow-metadatacatalogconfig-gluedatacatalog"></a>
Specifies the configuration that Amazon AppFlow uses when it catalogs your data with the AWS Glue Data Catalog\.  
*Required*: No  
*Type*: [GlueDataCatalog](aws-properties-appflow-flow-gluedatacatalog.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)