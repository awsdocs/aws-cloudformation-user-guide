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
      "[ServiceCatalogProvisioningDetails](#cfn-sagemaker-project-servicecatalogprovisioningdetails)" : Json,
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
  [ServiceCatalogProvisioningDetails](#cfn-sagemaker-project-servicecatalogprovisioningdetails): Json
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
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-project-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-project-return-values"></a>

### Ref<a name="aws-resource-sagemaker-project-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-project-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-project-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`ProjectArn`  <a name="ProjectArn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`ProjectId`  <a name="ProjectId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`ProjectStatus`  <a name="ProjectStatus-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`ServiceCatalogProvisionedProductDetails`  <a name="ServiceCatalogProvisionedProductDetails-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.