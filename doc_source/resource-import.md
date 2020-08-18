# Bringing existing resources into CloudFormation management<a name="resource-import"></a>

If you created an AWS resource outside of AWS CloudFormation management, you can bring this existing resource into AWS CloudFormation management using `resource import`\. You can manage your resources using AWS CloudFormation regardless of where they were created without having to delete and re\-create them as part of a stack\.

For a list of AWS resources that support import operations, see [Resources that support import operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)\.

## Resource import overview<a name="resource-import-overview"></a>

During an import operation, you create a change set that imports your existing resources into a stack or creates a new stack from your existing resources\. You provide the following during import\.
+ A template that describes the entire stack, including both the original stack resources and the resources you're importing\. Each resource to import must have a [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) attribute\.
+ Identifiers for the resources to import\. You provide two values to identify each target resource\.
  + An identifier property\. This is a resource property that can be used to identify each resource type\. For example, an `AWS::S3::Bucket` resource can be identified using its `BucketName`\.
  + An identifier value\. This is the target resource's actual property value\. For example, the actual value for the `BucketName` property might be `MyS3Bucket`\.

## Resource import validation<a name="resource-import-validation"></a>

During an import operation, AWS CloudFormation performs the following validations\.
+ The resource to import exists\.
+ The properties and configuration values for each resource to import adhere to the resource type schema, which defines its accepted properties, required properties, and supported property values\.
+ The required properties are specified in the template\. Required properties for each resource type are listed in the [Resource and property reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html)\.
+ The resource to import does not belong to another stack in the same Region\.

AWS CloudFormation does not check that the template configuration matches the actual configuration of resource properties\.

## Resource import status codes<a name="resource-import-status-codes"></a>

This table describes the various status types used with `resource import`\.


| Import operation status | Description | 
| --- | --- | 
|  `IMPORT_IN_PROGRESS`  |  The import operation is currently in progress\.  | 
|  `IMPORT_COMPLETE`  |  The import operation successfully completed for all resources in the stack that support `resource import`\.   | 
|  `IMPORT_ROLLBACK_IN_PROGRESS`  |  Import will roll back to the previous template configuration\.  | 
|  `IMPORT_ROLLBACK_FAILED`  |  The import rollback operation failed for at least one resource in the stack\. Results will be available for the resources CloudFormation successfully imported\.  | 
|  `IMPORT_ROLLBACK_COMPLETE`  |  Import successfully rolled back to the previous template configuration\.  | 

## Considerations during an import operation<a name="resource-import-considerations"></a>
+ After the import is complete and before performing subsequent stack operations, we recommend running [drift detection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/detect-drift-stack.html) on imported resources\. Drift detection ensures that the template configuration matches the actual configuration\.
+ Import operations don't allow new resource creations, resource deletions, or changes to property configurations\.
+ Each resource to import must have a `DeletionPolicy` attribute for the import operation to succeed\. The `DeletionPolicy` can be set to any possible value\. Only target resources need a `DeletionPolicy`\. Resources that are already part of the stack don't need a `DeletionPolicy`\.
+ You cannot import the same resource into multiple stacks\.
+ You can use the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-template-conditions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-template-conditions) IAM policy condition to control which resource types IAM users can work with during an import operation\.
+ The AWS CloudFormation stack limits apply when importing resources\. For more information on limits, see [AWS CloudFormation limits](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html)\.

## Getting started with resource import<a name="resource-import-getting-started"></a>
+ [Creating a stack from existing resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-new-stack.html)
+ [Importing existing resources into a stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-existing-stack.html)
+ [Moving resources between stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/refactor-stacks.html)
+ [Nesting an existing stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-nested-stacks.html)
+ [Reverting an import operation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-revert.html)
+ [Resources that support import operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)