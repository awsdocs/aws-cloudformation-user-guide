# AWS::QuickSight::Analysis<a name="aws-resource-quicksight-analysis"></a>

Creates an analysis in Amazon QuickSight\.

## Syntax<a name="aws-resource-quicksight-analysis-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-quicksight-analysis-syntax.json"></a>

```
{
  "Type" : "AWS::QuickSight::Analysis",
  "Properties" : {
      "[AnalysisId](#cfn-quicksight-analysis-analysisid)" : String,
      "[AwsAccountId](#cfn-quicksight-analysis-awsaccountid)" : String,
      "[Errors](#cfn-quicksight-analysis-errors)" : [ AnalysisError, ... ],
      "[Name](#cfn-quicksight-analysis-name)" : String,
      "[Parameters](#cfn-quicksight-analysis-parameters)" : Parameters,
      "[Permissions](#cfn-quicksight-analysis-permissions)" : [ ResourcePermission, ... ],
      "[SourceEntity](#cfn-quicksight-analysis-sourceentity)" : AnalysisSourceEntity,
      "[Tags](#cfn-quicksight-analysis-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ThemeArn](#cfn-quicksight-analysis-themearn)" : String
    }
}
```

### YAML<a name="aws-resource-quicksight-analysis-syntax.yaml"></a>

```
Type: AWS::QuickSight::Analysis
Properties: 
  [AnalysisId](#cfn-quicksight-analysis-analysisid): String
  [AwsAccountId](#cfn-quicksight-analysis-awsaccountid): String
  [Errors](#cfn-quicksight-analysis-errors): 
    - AnalysisError
  [Name](#cfn-quicksight-analysis-name): String
  [Parameters](#cfn-quicksight-analysis-parameters): 
    Parameters
  [Permissions](#cfn-quicksight-analysis-permissions): 
    - ResourcePermission
  [SourceEntity](#cfn-quicksight-analysis-sourceentity): 
    AnalysisSourceEntity
  [Tags](#cfn-quicksight-analysis-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ThemeArn](#cfn-quicksight-analysis-themearn): String
```

## Properties<a name="aws-resource-quicksight-analysis-properties"></a>

`AnalysisId`  <a name="cfn-quicksight-analysis-analysisid"></a>
The ID of the analysis\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\w\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AwsAccountId`  <a name="cfn-quicksight-analysis-awsaccountid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Errors`  <a name="cfn-quicksight-analysis-errors"></a>
Errors associated with the analysis\.  
*Required*: No  
*Type*: List of [AnalysisError](aws-properties-quicksight-analysis-analysiserror.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-name"></a>
The descriptive name of the analysis\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-quicksight-analysis-parameters"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Parameters](aws-properties-quicksight-analysis-parameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-analysis-permissions"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-analysis-resourcepermission.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEntity`  <a name="cfn-quicksight-analysis-sourceentity"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [AnalysisSourceEntity](aws-properties-quicksight-analysis-analysissourceentity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-analysis-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThemeArn`  <a name="cfn-quicksight-analysis-themearn"></a>
The ARN of the theme of the analysis\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-analysis-return-values"></a>

### Ref<a name="aws-resource-quicksight-analysis-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-analysis-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-analysis-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`DataSetArns`  <a name="DataSetArns-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`Sheets`  <a name="Sheets-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`Status`  <a name="Status-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.