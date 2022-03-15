# AWS::EC2::NetworkInsightsAccessScope<a name="aws-resource-ec2-networkinsightsaccessscope"></a>

Describes a Network Access Scope\. A Network Access Scope defines outbound \(egress\) and inbound \(ingress\) traffic patterns, including sources, destinations, paths, and traffic types\.

Network Access Analyzer identifies unintended network access to your resources on AWS\. When you start an analysis on a Network Access Scope, Network Access Analyzer produces findings\. For more information, see the [Network Access Analyzer User Guide](https://docs.aws.amazon.com/vpc/latest/network-access-analyzer/)\.

## Syntax<a name="aws-resource-ec2-networkinsightsaccessscope-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinsightsaccessscope-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInsightsAccessScope",
  "Properties" : {
      "[ExcludePaths](#cfn-ec2-networkinsightsaccessscope-excludepaths)" : [ AccessScopePathRequest, ... ],
      "[MatchPaths](#cfn-ec2-networkinsightsaccessscope-matchpaths)" : [ AccessScopePathRequest, ... ],
      "[Tags](#cfn-ec2-networkinsightsaccessscope-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-networkinsightsaccessscope-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkInsightsAccessScope
Properties: 
  [ExcludePaths](#cfn-ec2-networkinsightsaccessscope-excludepaths): 
    - AccessScopePathRequest
  [MatchPaths](#cfn-ec2-networkinsightsaccessscope-matchpaths): 
    - AccessScopePathRequest
  [Tags](#cfn-ec2-networkinsightsaccessscope-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-networkinsightsaccessscope-properties"></a>

`ExcludePaths`  <a name="cfn-ec2-networkinsightsaccessscope-excludepaths"></a>
The paths to exclude\.  
*Required*: No  
*Type*: List of [AccessScopePathRequest](aws-properties-ec2-networkinsightsaccessscope-accessscopepathrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MatchPaths`  <a name="cfn-ec2-networkinsightsaccessscope-matchpaths"></a>
The paths to match\.  
*Required*: No  
*Type*: List of [AccessScopePathRequest](aws-properties-ec2-networkinsightsaccessscope-accessscopepathrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-networkinsightsaccessscope-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-networkinsightsaccessscope-return-values"></a>

### Ref<a name="aws-resource-ec2-networkinsightsaccessscope-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the network insights scope\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-networkinsightsaccessscope-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-networkinsightsaccessscope-return-values-fn--getatt-fn--getatt"></a>

`CreatedDate`  <a name="CreatedDate-fn::getatt"></a>
The creation date\.

`NetworkInsightsAccessScopeArn`  <a name="NetworkInsightsAccessScopeArn-fn::getatt"></a>
The ARN of the Network Access Scope\.

`NetworkInsightsAccessScopeId`  <a name="NetworkInsightsAccessScopeId-fn::getatt"></a>
The ID of the Network Access Scope\.

`UpdatedDate`  <a name="UpdatedDate-fn::getatt"></a>
The last updated date\.