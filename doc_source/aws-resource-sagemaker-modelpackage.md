# AWS::SageMaker::ModelPackage<a name="aws-resource-sagemaker-modelpackage"></a>

A versioned model that can be deployed for SageMaker inference\.

## Syntax<a name="aws-resource-sagemaker-modelpackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-modelpackage-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::ModelPackage",
  "Properties" : {
      "[AdditionalInferenceSpecificationDefinition](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition)" : AdditionalInferenceSpecificationDefinition,
      "[AdditionalInferenceSpecifications](#cfn-sagemaker-modelpackage-additionalinferencespecifications)" : [ AdditionalInferenceSpecificationDefinition, ... ],
      "[AdditionalInferenceSpecificationsToAdd](#cfn-sagemaker-modelpackage-additionalinferencespecificationstoadd)" : [ AdditionalInferenceSpecificationDefinition, ... ],
      "[ApprovalDescription](#cfn-sagemaker-modelpackage-approvaldescription)" : String,
      "[CertifyForMarketplace](#cfn-sagemaker-modelpackage-certifyformarketplace)" : Boolean,
      "[ClientToken](#cfn-sagemaker-modelpackage-clienttoken)" : String,
      "[CreatedBy](#cfn-sagemaker-modelpackage-createdby)" : UserContext,
      "[CustomerMetadataProperties](#cfn-sagemaker-modelpackage-customermetadataproperties)" : {Key : Value, ...},
      "[Domain](#cfn-sagemaker-modelpackage-domain)" : String,
      "[DriftCheckBaselines](#cfn-sagemaker-modelpackage-driftcheckbaselines)" : DriftCheckBaselines,
      "[Environment](#cfn-sagemaker-modelpackage-environment)" : {Key : Value, ...},
      "[InferenceSpecification](#cfn-sagemaker-modelpackage-inferencespecification)" : InferenceSpecification,
      "[LastModifiedBy](#cfn-sagemaker-modelpackage-lastmodifiedby)" : UserContext,
      "[LastModifiedTime](#cfn-sagemaker-modelpackage-lastmodifiedtime)" : String,
      "[MetadataProperties](#cfn-sagemaker-modelpackage-metadataproperties)" : MetadataProperties,
      "[ModelApprovalStatus](#cfn-sagemaker-modelpackage-modelapprovalstatus)" : String,
      "[ModelMetrics](#cfn-sagemaker-modelpackage-modelmetrics)" : ModelMetrics,
      "[ModelPackageDescription](#cfn-sagemaker-modelpackage-modelpackagedescription)" : String,
      "[ModelPackageGroupName](#cfn-sagemaker-modelpackage-modelpackagegroupname)" : String,
      "[ModelPackageName](#cfn-sagemaker-modelpackage-modelpackagename)" : String,
      "[ModelPackageStatusDetails](#cfn-sagemaker-modelpackage-modelpackagestatusdetails)" : ModelPackageStatusDetails,
      "[ModelPackageStatusItem](#cfn-sagemaker-modelpackage-modelpackagestatusitem)" : ModelPackageStatusItem,
      "[ModelPackageVersion](#cfn-sagemaker-modelpackage-modelpackageversion)" : Integer,
      "[SamplePayloadUrl](#cfn-sagemaker-modelpackage-samplepayloadurl)" : String,
      "[SourceAlgorithmSpecification](#cfn-sagemaker-modelpackage-sourcealgorithmspecification)" : SourceAlgorithmSpecification,
      "[Tags](#cfn-sagemaker-modelpackage-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Task](#cfn-sagemaker-modelpackage-task)" : String,
      "[ValidationSpecification](#cfn-sagemaker-modelpackage-validationspecification)" : ValidationSpecification
    }
}
```

### YAML<a name="aws-resource-sagemaker-modelpackage-syntax.yaml"></a>

```
Type: AWS::SageMaker::ModelPackage
Properties: 
  [AdditionalInferenceSpecificationDefinition](#cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition): 
    AdditionalInferenceSpecificationDefinition
  [AdditionalInferenceSpecifications](#cfn-sagemaker-modelpackage-additionalinferencespecifications): 
    - AdditionalInferenceSpecificationDefinition
  [AdditionalInferenceSpecificationsToAdd](#cfn-sagemaker-modelpackage-additionalinferencespecificationstoadd): 
    - AdditionalInferenceSpecificationDefinition
  [ApprovalDescription](#cfn-sagemaker-modelpackage-approvaldescription): String
  [CertifyForMarketplace](#cfn-sagemaker-modelpackage-certifyformarketplace): Boolean
  [ClientToken](#cfn-sagemaker-modelpackage-clienttoken): String
  [CreatedBy](#cfn-sagemaker-modelpackage-createdby): 
    UserContext
  [CustomerMetadataProperties](#cfn-sagemaker-modelpackage-customermetadataproperties): 
    Key : Value
  [Domain](#cfn-sagemaker-modelpackage-domain): String
  [DriftCheckBaselines](#cfn-sagemaker-modelpackage-driftcheckbaselines): 
    DriftCheckBaselines
  [Environment](#cfn-sagemaker-modelpackage-environment): 
    Key : Value
  [InferenceSpecification](#cfn-sagemaker-modelpackage-inferencespecification): 
    InferenceSpecification
  [LastModifiedBy](#cfn-sagemaker-modelpackage-lastmodifiedby): 
    UserContext
  [LastModifiedTime](#cfn-sagemaker-modelpackage-lastmodifiedtime): String
  [MetadataProperties](#cfn-sagemaker-modelpackage-metadataproperties): 
    MetadataProperties
  [ModelApprovalStatus](#cfn-sagemaker-modelpackage-modelapprovalstatus): String
  [ModelMetrics](#cfn-sagemaker-modelpackage-modelmetrics): 
    ModelMetrics
  [ModelPackageDescription](#cfn-sagemaker-modelpackage-modelpackagedescription): String
  [ModelPackageGroupName](#cfn-sagemaker-modelpackage-modelpackagegroupname): String
  [ModelPackageName](#cfn-sagemaker-modelpackage-modelpackagename): String
  [ModelPackageStatusDetails](#cfn-sagemaker-modelpackage-modelpackagestatusdetails): 
    ModelPackageStatusDetails
  [ModelPackageStatusItem](#cfn-sagemaker-modelpackage-modelpackagestatusitem): 
    ModelPackageStatusItem
  [ModelPackageVersion](#cfn-sagemaker-modelpackage-modelpackageversion): Integer
  [SamplePayloadUrl](#cfn-sagemaker-modelpackage-samplepayloadurl): String
  [SourceAlgorithmSpecification](#cfn-sagemaker-modelpackage-sourcealgorithmspecification): 
    SourceAlgorithmSpecification
  [Tags](#cfn-sagemaker-modelpackage-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Task](#cfn-sagemaker-modelpackage-task): String
  [ValidationSpecification](#cfn-sagemaker-modelpackage-validationspecification): 
    ValidationSpecification
```

## Properties<a name="aws-resource-sagemaker-modelpackage-properties"></a>

`AdditionalInferenceSpecificationDefinition`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationdefinition"></a>
A structure of additional Inference Specification\. Additional Inference Specification specifies details about inference jobs that can be run with models based on this model package  
*Required*: No  
*Type*: [AdditionalInferenceSpecificationDefinition](aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdditionalInferenceSpecifications`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecifications"></a>
An array of additional Inference Specification objects\.  
*Required*: No  
*Type*: List of [AdditionalInferenceSpecificationDefinition](aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition.md)  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdditionalInferenceSpecificationsToAdd`  <a name="cfn-sagemaker-modelpackage-additionalinferencespecificationstoadd"></a>
An array of additional Inference Specification objects to be added to the existing array\. The total number of additional Inference Specification objects cannot exceed 15\. Each additional Inference Specification object specifies artifacts based on this model package that can be used on inference endpoints\. Generally used with SageMaker Neo to store the compiled artifacts\.  
*Required*: No  
*Type*: List of [AdditionalInferenceSpecificationDefinition](aws-properties-sagemaker-modelpackage-additionalinferencespecificationdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApprovalDescription`  <a name="cfn-sagemaker-modelpackage-approvaldescription"></a>
A description provided when the model approval is set\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CertifyForMarketplace`  <a name="cfn-sagemaker-modelpackage-certifyformarketplace"></a>
Whether the model package is to be certified to be listed on AWS Marketplace\. For information about listing model packages on AWS Marketplace, see [List Your Algorithm or Model Package on AWS Marketplace](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-mkt-list.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientToken`  <a name="cfn-sagemaker-modelpackage-clienttoken"></a>
A unique token that guarantees that the call to this API is idempotent\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CreatedBy`  <a name="cfn-sagemaker-modelpackage-createdby"></a>
Information about the user who created or modified an experiment, trial, trial component, lineage group, or project\.  
*Required*: No  
*Type*: [UserContext](aws-properties-sagemaker-modelpackage-usercontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomerMetadataProperties`  <a name="cfn-sagemaker-modelpackage-customermetadataproperties"></a>
The metadata properties for the model package\.   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-sagemaker-modelpackage-domain"></a>
The machine learning domain of your model package and its components\. Common machine learning domains include computer vision and natural language processing\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DriftCheckBaselines`  <a name="cfn-sagemaker-modelpackage-driftcheckbaselines"></a>
Represents the drift check baselines that can be used when the model monitor is set using the model package\.  
*Required*: No  
*Type*: [DriftCheckBaselines](aws-properties-sagemaker-modelpackage-driftcheckbaselines.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Environment`  <a name="cfn-sagemaker-modelpackage-environment"></a>
The environment variables to set in the Docker container\. Each key and value in the `Environment` string to string map can have length of up to 1024\. We support up to 16 entries in the map\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InferenceSpecification`  <a name="cfn-sagemaker-modelpackage-inferencespecification"></a>
Defines how to perform inference generation after a training job is run\.  
*Required*: No  
*Type*: [InferenceSpecification](aws-properties-sagemaker-modelpackage-inferencespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LastModifiedBy`  <a name="cfn-sagemaker-modelpackage-lastmodifiedby"></a>
Information about the user who created or modified an experiment, trial, trial component, lineage group, or project\.  
*Required*: No  
*Type*: [UserContext](aws-properties-sagemaker-modelpackage-usercontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastModifiedTime`  <a name="cfn-sagemaker-modelpackage-lastmodifiedtime"></a>
The last time the model package was modified\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetadataProperties`  <a name="cfn-sagemaker-modelpackage-metadataproperties"></a>
Metadata properties of the tracking entity, trial, or trial component\.  
*Required*: No  
*Type*: [MetadataProperties](aws-properties-sagemaker-modelpackage-metadataproperties.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelApprovalStatus`  <a name="cfn-sagemaker-modelpackage-modelapprovalstatus"></a>
The approval status of the model\. This can be one of the following values\.  
+  `APPROVED` \- The model is approved
+  `REJECTED` \- The model is rejected\.
+  `PENDING_MANUAL_APPROVAL` \- The model is waiting for manual approval\.
*Required*: No  
*Type*: String  
*Allowed values*: `Approved | PendingManualApproval | Rejected`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelMetrics`  <a name="cfn-sagemaker-modelpackage-modelmetrics"></a>
Metrics for the model\.  
*Required*: No  
*Type*: [ModelMetrics](aws-properties-sagemaker-modelpackage-modelmetrics.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPackageDescription`  <a name="cfn-sagemaker-modelpackage-modelpackagedescription"></a>
The description of the model package\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPackageGroupName`  <a name="cfn-sagemaker-modelpackage-modelpackagegroupname"></a>
The model group to which the model belongs\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelPackageName`  <a name="cfn-sagemaker-modelpackage-modelpackagename"></a>
The name of the model\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelPackageStatusDetails`  <a name="cfn-sagemaker-modelpackage-modelpackagestatusdetails"></a>
Specifies the validation and image scan statuses of the model package\.  
*Required*: No  
*Type*: [ModelPackageStatusDetails](aws-properties-sagemaker-modelpackage-modelpackagestatusdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelPackageStatusItem`  <a name="cfn-sagemaker-modelpackage-modelpackagestatusitem"></a>
Represents the overall status of a model package\.  
*Required*: No  
*Type*: [ModelPackageStatusItem](aws-properties-sagemaker-modelpackage-modelpackagestatusitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelPackageVersion`  <a name="cfn-sagemaker-modelpackage-modelpackageversion"></a>
The version number of a versioned model\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamplePayloadUrl`  <a name="cfn-sagemaker-modelpackage-samplepayloadurl"></a>
The Amazon Simple Storage Service path where the sample payload are stored\. This path must point to a single gzip compressed tar archive \(\.tar\.gz suffix\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceAlgorithmSpecification`  <a name="cfn-sagemaker-modelpackage-sourcealgorithmspecification"></a>
A list of algorithms that were used to create a model package\.  
*Required*: No  
*Type*: [SourceAlgorithmSpecification](aws-properties-sagemaker-modelpackage-sourcealgorithmspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-modelpackage-tags"></a>
A list of the tags associated with the model package\. For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) in the * AWS General Reference Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Task`  <a name="cfn-sagemaker-modelpackage-task"></a>
The machine learning task your model package accomplishes\. Common machine learning tasks include object detection and image classification\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidationSpecification`  <a name="cfn-sagemaker-modelpackage-validationspecification"></a>
Specifies batch transform jobs that SageMaker runs to validate your model package\.  
*Required*: No  
*Type*: [ValidationSpecification](aws-properties-sagemaker-modelpackage-validationspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-modelpackage-return-values"></a>

### Ref<a name="aws-resource-sagemaker-modelpackage-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-modelpackage-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-modelpackage-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time that the model package was created\.

`ModelPackageArn`  <a name="ModelPackageArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the model package\.

`ModelPackageStatus`  <a name="ModelPackageStatus-fn::getatt"></a>
The status of the model package\. This can be one of the following values\.  
+  `PENDING` \- The model package creation is pending\.
+  `IN_PROGRESS` \- The model package is in the process of being created\.
+  `COMPLETED` \- The model package was successfully created\.
+  `FAILED` \- The model package creation failed\.
+  `DELETING` \- The model package is in the process of being deleted\.