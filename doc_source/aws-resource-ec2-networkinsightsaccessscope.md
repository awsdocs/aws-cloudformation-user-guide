# AWS::EC2::NetworkInsightsAccessScope<a name="aws-resource-ec2-networkinsightsaccessscope"></a>

Describes a Network Access Scope\.

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

### Fn::GetAtt<a name="aws-resource-ec2-networkinsightsaccessscope-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-networkinsightsaccessscope-return-values-fn--getatt-fn--getatt"></a>

`CreatedDate`  <a name="CreatedDate-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`NetworkInsightsAccessScopeArn`  <a name="NetworkInsightsAccessScopeArn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`NetworkInsightsAccessScopeId`  <a name="NetworkInsightsAccessScopeId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`UpdatedDate`  <a name="UpdatedDate-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.