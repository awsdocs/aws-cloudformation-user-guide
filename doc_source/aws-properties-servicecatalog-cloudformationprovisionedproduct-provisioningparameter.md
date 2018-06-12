# AWS Service Catalog CloudFormationProvisionedProduct ProvisioningParameter<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter"></a>

<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-description"></a>The `ProvisioningParameter` property type specifies a parameter for an AWS Service Catalog provisioned product\.

<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-inheritance"></a> `ProvisioningParameter` is a property of the [AWS::ServiceCatalog::CloudFormationProvisionedProduct](aws-resource-servicecatalog-cloudformationprovisionedproduct.md) resource\.

## Syntax<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-syntax.json"></a>

```
{
  "[Value](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-value)" : String,
  "[Key](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-key)" : String
}
```

### YAML<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-syntax.yaml"></a>

```
[Value](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-value): String
[Key](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-key): String
```

## Properties<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-properties"></a>

`Key`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-key"></a>
The parameter key\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameter-value"></a>
The parameter value\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 