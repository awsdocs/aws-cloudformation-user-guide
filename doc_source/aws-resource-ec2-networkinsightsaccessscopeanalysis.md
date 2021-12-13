# AWS::EC2::NetworkInsightsAccessScopeAnalysis<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis"></a>

Describes a Network Access Scope analysis\.

## Syntax<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInsightsAccessScopeAnalysis",
  "Properties" : {
      "[NetworkInsightsAccessScopeId](#cfn-ec2-networkinsightsaccessscopeanalysis-networkinsightsaccessscopeid)" : String,
      "[Tags](#cfn-ec2-networkinsightsaccessscopeanalysis-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkInsightsAccessScopeAnalysis
Properties: 
  [NetworkInsightsAccessScopeId](#cfn-ec2-networkinsightsaccessscopeanalysis-networkinsightsaccessscopeid): String
  [Tags](#cfn-ec2-networkinsightsaccessscopeanalysis-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-properties"></a>

`NetworkInsightsAccessScopeId`  <a name="cfn-ec2-networkinsightsaccessscopeanalysis-networkinsightsaccessscopeid"></a>
The ID of the Network Access Scope\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-networkinsightsaccessscopeanalysis-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-return-values"></a>

### Ref<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-return-values-fn--getatt-fn--getatt"></a>

`AnalyzedEniCount`  <a name="AnalyzedEniCount-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`EndDate`  <a name="EndDate-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`FindingsFound`  <a name="FindingsFound-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`NetworkInsightsAccessScopeAnalysisArn`  <a name="NetworkInsightsAccessScopeAnalysisArn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`NetworkInsightsAccessScopeAnalysisId`  <a name="NetworkInsightsAccessScopeAnalysisId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`StartDate`  <a name="StartDate-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`Status`  <a name="Status-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`StatusMessage`  <a name="StatusMessage-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.