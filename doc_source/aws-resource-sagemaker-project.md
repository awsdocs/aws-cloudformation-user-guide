# AWS::SageMaker::Project<a name="aws-resource-sagemaker-project"></a>

Creates a machine learning \(ML\) project that can contain one or more templates that set up an ML pipeline from training to deploying an approved model\.

## Syntax<a name="aws-resource-sagemaker-project-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-project-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::Project",
  "Properties" : {
      "[ProjectDescription](#cfn-sagemaker-project-projectdescription)" : String,
      "[ProjectName](#cfn-sagemaker-project-projectname)" : String,
      "[ServiceCatalogProvisioningDetails](#cfn-sagemaker-project-servicecatalogprovisioningdetails)" : ServiceCatalogProvisioningDetails,
      "[Tags](#cfn-sagemaker-project-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-project-syntax.yaml"></a>

```
Type: AWS::SageMaker::Project
Properties: 
  [ProjectDescription](#cfn-sagemaker-project-projectdescription): String
  [ProjectName](#cfn-sagemaker-project-projectname): String
  [ServiceCatalogProvisioningDetails](#cfn-sagemaker-project-servicecatalogprovisioningdetails): 
    ServiceCatalogProvisioningDetails
  [Tags](#cfn-sagemaker-project-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-project-properties"></a>

`ProjectDescription`  <a name="cfn-sagemaker-project-projectdescription"></a>
The description of the project\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProjectName`  <a name="cfn-sagemaker-project-projectname"></a>
The name of the project\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,31}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceCatalogProvisioningDetails`  <a name="cfn-sagemaker-project-servicecatalogprovisioningdetails"></a>
The product ID and provisioning artifact ID to provision a service catalog\. For information, see [What is AWS Service Catalog](https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html)\.  
*Required*: Yes  
*Type*: [ServiceCatalogProvisioningDetails](aws-properties-sagemaker-project-servicecatalogprovisioningdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-project-tags"></a>
A list of key\-value pairs to apply to this resource\.  
For more information, see [Resource Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) and [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html#allocation-what) in the * AWS Billing and Cost Management User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-project-return-values"></a>

### Ref<a name="aws-resource-sagemaker-project-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-project-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-project-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time that the project was created\.

`ProjectArn`  <a name="ProjectArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the project\.

`ProjectId`  <a name="ProjectId-fn::getatt"></a>
The ID of the project\. This ID is prepended to all entities associated with this project\.

`ProjectStatus`  <a name="ProjectStatus-fn::getatt"></a>
The status of the project\.

`ServiceCatalogProvisionedProductDetails`  <a name="ServiceCatalogProvisionedProductDetails-fn::getatt"></a>
The product ID and status message of the projet as a service catalog provisioned product\. For information, see [What is AWS Service Catalog](https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html)\.

`ServiceCatalogProvisionedProductDetails.ProvisionedProductId`  <a name="ServiceCatalogProvisionedProductDetails.ProvisionedProductId-fn::getatt"></a>
Property description not available\.

`ServiceCatalogProvisionedProductDetails.ProvisionedProductStatusMessage`  <a name="ServiceCatalogProvisionedProductDetails.ProvisionedProductStatusMessage-fn::getatt"></a>
Property description not available\.

## Examples<a name="aws-resource-sagemaker-project--examples"></a>

### SageMaker Project Example<a name="aws-resource-sagemaker-project--examples--SageMaker_Project_Example"></a>

The following example creates a SageMaker Project\.

#### JSON<a name="aws-resource-sagemaker-project--examples--SageMaker_Project_Example--json"></a>

```
{
   "Description": "AWS SageMaker Project basic template",
   "Resources": {
      "SampleProject": {
         "Type": "AWS::SageMaker::Project",
         "Properties": {
            "ProjectName": "project1",
            "ProjectDescription": "Project Description",
            "ServiceCatalogProvisioningDetails": {
               "ProductId": "prod-53ibyqbj2cgmo",
               "ProvisioningArtifactId": "pa-sm4pjfuzictpe"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-sagemaker-project--examples--SageMaker_Project_Example--yaml"></a>

```
---
Description: AWS SageMaker Project basic template

Resources:

  SampleProject:
    Type: AWS::SageMaker::Project
    Properties:
      ProjectName: "SampleProject"
      ProjectDescription: "Project Description"
      ServiceCatalogProvisioningDetails:
        ProductId: "prod-53ibyqbj2cgmo"
        ProvisioningArtifactId: "pa-sm4pjfuzictpe"
```