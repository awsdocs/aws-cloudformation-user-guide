# AWS::CUR::ReportDefinition<a name="aws-resource-cur-reportdefinition"></a>

The definition of AWS Cost and Usage Report\. You can specify the report name, time unit, report format, compression format, S3 bucket, additional artifacts, and schema elements in the definition\. 

## Syntax<a name="aws-resource-cur-reportdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cur-reportdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::CUR::ReportDefinition",
  "Properties" : {
      "[AdditionalArtifacts](#cfn-cur-reportdefinition-additionalartifacts)" : [ String, ... ],
      "[AdditionalSchemaElements](#cfn-cur-reportdefinition-additionalschemaelements)" : [ String, ... ],
      "[BillingViewArn](#cfn-cur-reportdefinition-billingviewarn)" : String,
      "[Compression](#cfn-cur-reportdefinition-compression)" : String,
      "[Format](#cfn-cur-reportdefinition-format)" : String,
      "[RefreshClosedReports](#cfn-cur-reportdefinition-refreshclosedreports)" : Boolean,
      "[ReportName](#cfn-cur-reportdefinition-reportname)" : String,
      "[ReportVersioning](#cfn-cur-reportdefinition-reportversioning)" : String,
      "[S3Bucket](#cfn-cur-reportdefinition-s3bucket)" : String,
      "[S3Prefix](#cfn-cur-reportdefinition-s3prefix)" : String,
      "[S3Region](#cfn-cur-reportdefinition-s3region)" : String,
      "[TimeUnit](#cfn-cur-reportdefinition-timeunit)" : String
    }
}
```

### YAML<a name="aws-resource-cur-reportdefinition-syntax.yaml"></a>

```
Type: AWS::CUR::ReportDefinition
Properties: 
  [AdditionalArtifacts](#cfn-cur-reportdefinition-additionalartifacts): 
    - String
  [AdditionalSchemaElements](#cfn-cur-reportdefinition-additionalschemaelements): 
    - String
  [BillingViewArn](#cfn-cur-reportdefinition-billingviewarn): String
  [Compression](#cfn-cur-reportdefinition-compression): String
  [Format](#cfn-cur-reportdefinition-format): String
  [RefreshClosedReports](#cfn-cur-reportdefinition-refreshclosedreports): Boolean
  [ReportName](#cfn-cur-reportdefinition-reportname): String
  [ReportVersioning](#cfn-cur-reportdefinition-reportversioning): String
  [S3Bucket](#cfn-cur-reportdefinition-s3bucket): String
  [S3Prefix](#cfn-cur-reportdefinition-s3prefix): String
  [S3Region](#cfn-cur-reportdefinition-s3region): String
  [TimeUnit](#cfn-cur-reportdefinition-timeunit): String
```

## Properties<a name="aws-resource-cur-reportdefinition-properties"></a>

`AdditionalArtifacts`  <a name="cfn-cur-reportdefinition-additionalartifacts"></a>
A list of manifests that you want AWS to create for this report\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdditionalSchemaElements`  <a name="cfn-cur-reportdefinition-additionalschemaelements"></a>
A list of strings that indicate additional content that AWS includes in the report, such as individual resource IDs\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BillingViewArn`  <a name="cfn-cur-reportdefinition-billingviewarn"></a>
The Amazon Resource Name \(ARN\) of the billing view\. You can get this value by using the billing view service public APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Compression`  <a name="cfn-cur-reportdefinition-compression"></a>
The compression format that Amazon Web Services uses for the report\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-cur-reportdefinition-format"></a>
The format that Amazon Web Services saves the report in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshClosedReports`  <a name="cfn-cur-reportdefinition-refreshclosedreports"></a>
Whether you want AWS to update your reports after they have been finalized if AWS detects charges related to previous months\. These charges can include refunds, credits, or support fees\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportName`  <a name="cfn-cur-reportdefinition-reportname"></a>
The name of the report that you want to create\. The name must be unique, is case sensitive, and can't include spaces\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReportVersioning`  <a name="cfn-cur-reportdefinition-reportversioning"></a>
Whether you want AWS to overwrite the previous version of each report or to deliver the report in addition to the previous versions\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CREATE_NEW_REPORT | OVERWRITE_REPORT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Bucket`  <a name="cfn-cur-reportdefinition-s3bucket"></a>
The S3 bucket where Amazon Web Services delivers the report\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Prefix`  <a name="cfn-cur-reportdefinition-s3prefix"></a>
The prefix that Amazon Web Services adds to the report name when Amazon Web Services delivers the report\. Your prefix can't include spaces\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Region`  <a name="cfn-cur-reportdefinition-s3region"></a>
The Region of the S3 bucket that Amazon Web Services delivers the report into\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeUnit`  <a name="cfn-cur-reportdefinition-timeunit"></a>
The granularity of the line items in the report\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cur-reportdefinition-return-values"></a>

### Ref<a name="aws-resource-cur-reportdefinition-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns

 `{ "Ref": "ReportName" }` 

The name of the report that you want to create\. The name must be unique, is case sensitive, and can't include spaces\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.