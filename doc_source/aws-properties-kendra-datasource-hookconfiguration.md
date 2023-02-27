# AWS::Kendra::DataSource HookConfiguration<a name="aws-properties-kendra-datasource-hookconfiguration"></a>

Provides the configuration information for invoking a Lambda function in AWS Lambda to alter document metadata and content when ingesting documents into Amazon Kendra\. You can configure your Lambda function using [PreExtractionHookConfiguration](https://docs.aws.amazon.com/kendra/latest/dg/API_CustomDocumentEnrichmentConfiguration.html) if you want to apply advanced alterations on the original or raw documents\. If you want to apply advanced alterations on the Amazon Kendra structured documents, you must configure your Lambda function using [PostExtractionHookConfiguration](https://docs.aws.amazon.com/kendra/latest/dg/API_CustomDocumentEnrichmentConfiguration.html)\. You can only invoke one Lambda function\. However, this function can invoke other functions it requires\.

For more information, see [Customizing document metadata during the ingestion process](https://docs.aws.amazon.com/kendra/latest/dg/custom-document-enrichment.html)\.

## Syntax<a name="aws-properties-kendra-datasource-hookconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-hookconfiguration-syntax.json"></a>

```
{
  "[InvocationCondition](#cfn-kendra-datasource-hookconfiguration-invocationcondition)" : DocumentAttributeCondition,
  "[LambdaArn](#cfn-kendra-datasource-hookconfiguration-lambdaarn)" : String,
  "[S3Bucket](#cfn-kendra-datasource-hookconfiguration-s3bucket)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-hookconfiguration-syntax.yaml"></a>

```
  [InvocationCondition](#cfn-kendra-datasource-hookconfiguration-invocationcondition): 
    DocumentAttributeCondition
  [LambdaArn](#cfn-kendra-datasource-hookconfiguration-lambdaarn): String
  [S3Bucket](#cfn-kendra-datasource-hookconfiguration-s3bucket): String
```

## Properties<a name="aws-properties-kendra-datasource-hookconfiguration-properties"></a>

`InvocationCondition`  <a name="cfn-kendra-datasource-hookconfiguration-invocationcondition"></a>
The condition used for when a Lambda function should be invoked\.  
For example, you can specify a condition that if there are empty date\-time values, then Amazon Kendra should invoke a function that inserts the current date\-time\.  
*Required*: No  
*Type*: [DocumentAttributeCondition](aws-properties-kendra-datasource-documentattributecondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaArn`  <a name="cfn-kendra-datasource-hookconfiguration-lambdaarn"></a>
The Amazon Resource Name \(ARN\) of a role with permission to run a Lambda function during ingestion\. For more information, see [IAM roles for Amazon Kendra](https://docs.aws.amazon.com/kendra/latest/dg/iam-roles.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `/arn:aws[a-zA-Z-]*:lambda:[a-z]+-[a-z]+-[0-9]:[0-9]{12}:function:[a-zA-Z0-9-_]+(\/[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12})?(:[a-zA-Z0-9-_]+)?/`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Bucket`  <a name="cfn-kendra-datasource-hookconfiguration-s3bucket"></a>
Stores the original, raw documents or the structured, parsed documents before and after altering them\. For more information, see [Data contracts for Lambda functions](https://docs.aws.amazon.com/kendra/latest/dg/custom-document-enrichment.html#cde-data-contracts-lambda)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)