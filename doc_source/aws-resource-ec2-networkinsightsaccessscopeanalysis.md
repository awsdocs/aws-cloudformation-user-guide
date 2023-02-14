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

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the network insights analysis\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-networkinsightsaccessscopeanalysis-return-values-fn--getatt-fn--getatt"></a>

`AnalyzedEniCount`  <a name="AnalyzedEniCount-fn::getatt"></a>
The number of network interfaces analyzed\.

`EndDate`  <a name="EndDate-fn::getatt"></a>
The end date of the analysis\.

`FindingsFound`  <a name="FindingsFound-fn::getatt"></a>
Indicates whether there are findings \(true \| false \| unknown\)\.

`NetworkInsightsAccessScopeAnalysisArn`  <a name="NetworkInsightsAccessScopeAnalysisArn-fn::getatt"></a>
The ARN of the Network Access Scope analysis\.

`NetworkInsightsAccessScopeAnalysisId`  <a name="NetworkInsightsAccessScopeAnalysisId-fn::getatt"></a>
The ID of the Network Access Scope analysis\.

`StartDate`  <a name="StartDate-fn::getatt"></a>
The start date of the analysis\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the analysis \(running \| succeeded \| failed\)\.

`StatusMessage`  <a name="StatusMessage-fn::getatt"></a>
The status message\.