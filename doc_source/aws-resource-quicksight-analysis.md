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
The ID for the analysis that you're creating\. This ID displays in the URL of the analysis\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AwsAccountId`  <a name="cfn-quicksight-analysis-awsaccountid"></a>
The ID of the AWS account where you are creating an analysis\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^[0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Errors`  <a name="cfn-quicksight-analysis-errors"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [AnalysisError](aws-properties-quicksight-analysis-analysiserror.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-name"></a>
A descriptive name for the analysis that you're creating\. This name displays for the analysis in the Amazon QuickSight console\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-quicksight-analysis-parameters"></a>
The parameter names and override values that you want to use\. An analysis can have any parameter type, and some parameters might accept multiple values\.   
*Required*: No  
*Type*: [Parameters](aws-properties-quicksight-analysis-parameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-analysis-permissions"></a>
A structure that describes the principals and the resource\-level permissions on an analysis\. You can use the `Permissions` structure to grant permissions by providing a list of AWS Identity and Access Management \(IAM\) action information for each principal listed by Amazon Resource Name \(ARN\)\.   
To specify no permissions, omit `Permissions`\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-analysis-resourcepermission.md)  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEntity`  <a name="cfn-quicksight-analysis-sourceentity"></a>
A source entity to use for the analysis that you're creating\. This metadata structure contains details that describe a source template and one or more datasets\.  
Either a `SourceEntity` or a `Definition` must be provided in order for the request to be valid\.  
*Required*: Yes  
*Type*: [AnalysisSourceEntity](aws-properties-quicksight-analysis-analysissourceentity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-analysis-tags"></a>
Contains a map of the key\-value pairs for the resource tag or tags assigned to the analysis\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThemeArn`  <a name="cfn-quicksight-analysis-themearn"></a>
The ARN for the theme to apply to the analysis that you're creating\. To see the theme in the Amazon QuickSight console, make sure that you have access to it\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-analysis-return-values"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-analysis-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-analysis-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the analysis\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Property description not available\.

`DataSetArns`  <a name="DataSetArns-fn::getatt"></a>
The ARNs of the datasets of the analysis\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The time that the analysis was last updated\.