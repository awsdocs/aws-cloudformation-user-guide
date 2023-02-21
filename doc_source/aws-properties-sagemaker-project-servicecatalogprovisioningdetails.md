# AWS::SageMaker::Project ServiceCatalogProvisioningDetails<a name="aws-properties-sagemaker-project-servicecatalogprovisioningdetails"></a>

Details that you specify to provision a service catalog product\. For information about service catalog, see [What is AWS Service Catalog](https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html)\.

## Syntax<a name="aws-properties-sagemaker-project-servicecatalogprovisioningdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-project-servicecatalogprovisioningdetails-syntax.json"></a>

```
{
  "[PathId](#cfn-sagemaker-project-servicecatalogprovisioningdetails-pathid)" : String,
  "[ProductId](#cfn-sagemaker-project-servicecatalogprovisioningdetails-productid)" : String,
  "[ProvisioningArtifactId](#cfn-sagemaker-project-servicecatalogprovisioningdetails-provisioningartifactid)" : String,
  "[ProvisioningParameters](#cfn-sagemaker-project-servicecatalogprovisioningdetails-provisioningparameters)" : [ ProvisioningParameter, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-project-servicecatalogprovisioningdetails-syntax.yaml"></a>

```
  [PathId](#cfn-sagemaker-project-servicecatalogprovisioningdetails-pathid): String
  [ProductId](#cfn-sagemaker-project-servicecatalogprovisioningdetails-productid): String
  [ProvisioningArtifactId](#cfn-sagemaker-project-servicecatalogprovisioningdetails-provisioningartifactid): String
  [ProvisioningParameters](#cfn-sagemaker-project-servicecatalogprovisioningdetails-provisioningparameters): 
    - ProvisioningParameter
```

## Properties<a name="aws-properties-sagemaker-project-servicecatalogprovisioningdetails-properties"></a>

`PathId`  <a name="cfn-sagemaker-project-servicecatalogprovisioningdetails-pathid"></a>
The path identifier of the product\. This value is optional if the product has a default path, and required if the product has more than one path\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProductId`  <a name="cfn-sagemaker-project-servicecatalogprovisioningdetails-productid"></a>
The ID of the product to provision\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisioningArtifactId`  <a name="cfn-sagemaker-project-servicecatalogprovisioningdetails-provisioningartifactid"></a>
The ID of the provisioning artifact\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisioningParameters`  <a name="cfn-sagemaker-project-servicecatalogprovisioningdetails-provisioningparameters"></a>
A list of key value pairs that you specify when you provision a product\.  
*Required*: No  
*Type*: List of [ProvisioningParameter](aws-properties-sagemaker-project-provisioningparameter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)