# AWS::EC2::NetworkInsightsAnalysis<a name="aws-resource-ec2-networkinsightsanalysis"></a>

Specifies a network insights analysis\.

## Syntax<a name="aws-resource-ec2-networkinsightsanalysis-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinsightsanalysis-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInsightsAnalysis",
  "Properties" : {
      "[FilterInArns](#cfn-ec2-networkinsightsanalysis-filterinarns)" : [ String, ... ],
      "[NetworkInsightsPathId](#cfn-ec2-networkinsightsanalysis-networkinsightspathid)" : String,
      "[StatusMessage](#cfn-ec2-networkinsightsanalysis-statusmessage)" : String,
      "[Tags](#cfn-ec2-networkinsightsanalysis-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-networkinsightsanalysis-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkInsightsAnalysis
Properties: 
  [FilterInArns](#cfn-ec2-networkinsightsanalysis-filterinarns): 
    - String
  [NetworkInsightsPathId](#cfn-ec2-networkinsightsanalysis-networkinsightspathid): String
  [StatusMessage](#cfn-ec2-networkinsightsanalysis-statusmessage): String
  [Tags](#cfn-ec2-networkinsightsanalysis-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-networkinsightsanalysis-properties"></a>

`FilterInArns`  <a name="cfn-ec2-networkinsightsanalysis-filterinarns"></a>
The Amazon Resource Names \(ARN\) of the resources that the path must traverse\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInsightsPathId`  <a name="cfn-ec2-networkinsightsanalysis-networkinsightspathid"></a>
The ID of the path\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StatusMessage`  <a name="cfn-ec2-networkinsightsanalysis-statusmessage"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-networkinsightsanalysis-tags"></a>
The tags to apply\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-networkinsightsanalysis-return-values"></a>

### Ref<a name="aws-resource-ec2-networkinsightsanalysis-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the network insights analysis\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-networkinsightsanalysis-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-networkinsightsanalysis-return-values-fn--getatt-fn--getatt"></a>

`AlternatePathHints`  <a name="AlternatePathHints-fn::getatt"></a>
Potential intermediate components\.

`Explanations`  <a name="Explanations-fn::getatt"></a>
The explanations\. For more information, see [Reachability Analyzer explanation codes](https://docs.aws.amazon.com/vpc/latest/reachability/explanation-codes.html)\.

`ForwardPathComponents`  <a name="ForwardPathComponents-fn::getatt"></a>
The components in the path from source to destination\.

`NetworkInsightsAnalysisArn`  <a name="NetworkInsightsAnalysisArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the network insights analysis\.

`NetworkInsightsAnalysisId`  <a name="NetworkInsightsAnalysisId-fn::getatt"></a>
The ID of the network insights analysis\.

`NetworkPathFound`  <a name="NetworkPathFound-fn::getatt"></a>
Indicates whether the destination is reachable from the source\.

`ReturnPathComponents`  <a name="ReturnPathComponents-fn::getatt"></a>
The components in the path from destination to source\.

`StartDate`  <a name="StartDate-fn::getatt"></a>
The time the analysis started\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the network insights analysis\.