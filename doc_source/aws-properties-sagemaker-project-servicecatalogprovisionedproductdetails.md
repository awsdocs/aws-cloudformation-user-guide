# AWS::SageMaker::Project ServiceCatalogProvisionedProductDetails<a name="aws-properties-sagemaker-project-servicecatalogprovisionedproductdetails"></a>

Details of a provisioned service catalog product\. For information about service catalog, see [What is AWS Service Catalog](https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html)\.

## Syntax<a name="aws-properties-sagemaker-project-servicecatalogprovisionedproductdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-project-servicecatalogprovisionedproductdetails-syntax.json"></a>

```
{
  "[ProvisionedProductId](#cfn-sagemaker-project-servicecatalogprovisionedproductdetails-provisionedproductid)" : String,
  "[ProvisionedProductStatusMessage](#cfn-sagemaker-project-servicecatalogprovisionedproductdetails-provisionedproductstatusmessage)" : String
}
```

### YAML<a name="aws-properties-sagemaker-project-servicecatalogprovisionedproductdetails-syntax.yaml"></a>

```
  [ProvisionedProductId](#cfn-sagemaker-project-servicecatalogprovisionedproductdetails-provisionedproductid): String
  [ProvisionedProductStatusMessage](#cfn-sagemaker-project-servicecatalogprovisionedproductdetails-provisionedproductstatusmessage): String
```

## Properties<a name="aws-properties-sagemaker-project-servicecatalogprovisionedproductdetails-properties"></a>

`ProvisionedProductId`  <a name="cfn-sagemaker-project-servicecatalogprovisionedproductdetails-provisionedproductid"></a>
The ID of the provisioned product\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisionedProductStatusMessage`  <a name="cfn-sagemaker-project-servicecatalogprovisionedproductdetails-provisionedproductstatusmessage"></a>
The current status of the product\.  
+  `AVAILABLE` \- Stable state, ready to perform any operation\. The most recent operation succeeded and completed\.
+  `UNDER_CHANGE` \- Transitive state\. Operations performed might not have valid results\. Wait for an AVAILABLE status before performing operations\.
+  `TAINTED` \- Stable state, ready to perform any operation\. The stack has completed the requested operation but is not exactly what was requested\. For example, a request to update to a new version failed and the stack rolled back to the current version\.
+  `ERROR` \- An unexpected error occurred\. The provisioned product exists but the stack is not running\. For example, CloudFormation received a parameter value that was not valid and could not launch the stack\.
+  `PLAN_IN_PROGRESS` \- Transitive state\. The plan operations were performed to provision a new product, but resources have not yet been created\. After reviewing the list of resources to be created, execute the plan\. Wait for an AVAILABLE status before performing operations\.
*Required*: No  
*Type*: String  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)