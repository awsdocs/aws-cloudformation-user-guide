# AWS::CodeBuild::ReportGroup<a name="aws-resource-codebuild-reportgroup"></a>

 Creates a report group\. A report group contains a collection of reports\. 

## Syntax<a name="aws-resource-codebuild-reportgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codebuild-reportgroup-syntax.json"></a>

```
{
  "Type" : "AWS::CodeBuild::ReportGroup",
  "Properties" : {
      "[ExportConfig](#cfn-codebuild-reportgroup-exportconfig)" : ReportExportConfig,
      "[Name](#cfn-codebuild-reportgroup-name)" : String,
      "[Tags](#cfn-codebuild-reportgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-codebuild-reportgroup-type)" : String
    }
}
```

### YAML<a name="aws-resource-codebuild-reportgroup-syntax.yaml"></a>

```
Type: AWS::CodeBuild::ReportGroup
Properties: 
  [ExportConfig](#cfn-codebuild-reportgroup-exportconfig): 
    ReportExportConfig
  [Name](#cfn-codebuild-reportgroup-name): String
  [Tags](#cfn-codebuild-reportgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-codebuild-reportgroup-type): String
```

## Properties<a name="aws-resource-codebuild-reportgroup-properties"></a>

`ExportConfig`  <a name="cfn-codebuild-reportgroup-exportconfig"></a>
 Information about the destination where the raw data of this `ReportGroup` is exported\.   
*Required*: Yes  
*Type*: [ReportExportConfig](aws-properties-codebuild-reportgroup-reportexportconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codebuild-reportgroup-name"></a>
 The name of a `ReportGroup`\.   
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-codebuild-reportgroup-tags"></a>
 A list of tag key and value pairs associated with this report group\.   
These tags are available for use by AWS services that support AWS CodeBuild report group tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codebuild-reportgroup-type"></a>
 The type of the `ReportGroup`\. The one valid value is `TEST`\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `CODE_COVERAGE | TEST`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-codebuild-reportgroup-return-values"></a>

### Ref<a name="aws-resource-codebuild-reportgroup-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN of the AWS CodeBuild report group, such as `arn:aws:codebuild:region:123456789012:report-group/myReportGroupName`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-codebuild-reportgroup-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-codebuild-reportgroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the AWS CodeBuild report group, such as `arn:aws:codebuild:region:123456789012:report-group/myReportGroupName`\. 