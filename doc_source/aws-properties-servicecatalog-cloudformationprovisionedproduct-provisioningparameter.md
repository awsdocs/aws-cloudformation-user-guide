# AWS::ServiceCatalog::CloudFormationProvisionedProduct ProvisioningParameter<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter"></a>

Information about a parameter used to provision a product\.

## Syntax<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-syntax.json"></a>

```
{
  "[Key](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-key)" : String,
  "[Value](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-value)" : String
}
```

### YAML<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-syntax.yaml"></a>

```
  [Key](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-key): String
  [Value](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-value): String
```

## Properties<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-properties"></a>

`Key`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-key"></a>
The parameter key\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-value"></a>
The parameter value\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter--seealso"></a>
+ [ProvisioningParameter](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_ProvisioningParameter.html) in the *AWS Service Catalog API Reference*

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
