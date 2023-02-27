# AWS::SageMaker::ModelPackage ModelPackageStatusDetails<a name="aws-properties-sagemaker-modelpackage-modelpackagestatusdetails"></a>

Specifies the validation and image scan statuses of the model package\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-modelpackagestatusdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-modelpackagestatusdetails-syntax.json"></a>

```
{
  "[ImageScanStatuses](#cfn-sagemaker-modelpackage-modelpackagestatusdetails-imagescanstatuses)" : [ ModelPackageStatusItem, ... ],
  "[ValidationStatuses](#cfn-sagemaker-modelpackage-modelpackagestatusdetails-validationstatuses)" : [ ModelPackageStatusItem, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-modelpackagestatusdetails-syntax.yaml"></a>

```
  [ImageScanStatuses](#cfn-sagemaker-modelpackage-modelpackagestatusdetails-imagescanstatuses): 
    - ModelPackageStatusItem
  [ValidationStatuses](#cfn-sagemaker-modelpackage-modelpackagestatusdetails-validationstatuses): 
    - ModelPackageStatusItem
```

## Properties<a name="aws-properties-sagemaker-modelpackage-modelpackagestatusdetails-properties"></a>

`ImageScanStatuses`  <a name="cfn-sagemaker-modelpackage-modelpackagestatusdetails-imagescanstatuses"></a>
The status of the scan of the Docker image container for the model package\.  
*Required*: No  
*Type*: List of [ModelPackageStatusItem](aws-properties-sagemaker-modelpackage-modelpackagestatusitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidationStatuses`  <a name="cfn-sagemaker-modelpackage-modelpackagestatusdetails-validationstatuses"></a>
The validation status of the model package\.  
*Required*: Yes  
*Type*: List of [ModelPackageStatusItem](aws-properties-sagemaker-modelpackage-modelpackagestatusitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)