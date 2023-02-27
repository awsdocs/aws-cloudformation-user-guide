# AWS::SageMaker::FeatureGroup DataCatalogConfig<a name="aws-properties-sagemaker-featuregroup-datacatalogconfig"></a>

The meta data of the Glue table which serves as data catalog for the `OfflineStore`\. 

## Syntax<a name="aws-properties-sagemaker-featuregroup-datacatalogconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-featuregroup-datacatalogconfig-syntax.json"></a>

```
{
  "[Catalog](#cfn-sagemaker-featuregroup-datacatalogconfig-catalog)" : String,
  "[Database](#cfn-sagemaker-featuregroup-datacatalogconfig-database)" : String,
  "[TableName](#cfn-sagemaker-featuregroup-datacatalogconfig-tablename)" : String
}
```

### YAML<a name="aws-properties-sagemaker-featuregroup-datacatalogconfig-syntax.yaml"></a>

```
  [Catalog](#cfn-sagemaker-featuregroup-datacatalogconfig-catalog): String
  [Database](#cfn-sagemaker-featuregroup-datacatalogconfig-database): String
  [TableName](#cfn-sagemaker-featuregroup-datacatalogconfig-tablename): String
```

## Properties<a name="aws-properties-sagemaker-featuregroup-datacatalogconfig-properties"></a>

`Catalog`  <a name="cfn-sagemaker-featuregroup-datacatalogconfig-catalog"></a>
The name of the Glue table catalog\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Database`  <a name="cfn-sagemaker-featuregroup-datacatalogconfig-database"></a>
The name of the Glue table database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableName`  <a name="cfn-sagemaker-featuregroup-datacatalogconfig-tablename"></a>
The name of the Glue table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)