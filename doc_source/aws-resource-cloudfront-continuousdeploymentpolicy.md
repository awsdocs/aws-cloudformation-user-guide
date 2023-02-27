# AWS::CloudFront::ContinuousDeploymentPolicy<a name="aws-resource-cloudfront-continuousdeploymentpolicy"></a>

Creates a continuous deployment policy that routes a subset of production traffic from a primary distribution to a staging distribution\.

After you create and update a staging distribution, you can use a continuous deployment policy to incrementally move traffic to the staging distribution\. This enables you to test changes to a distribution's configuration before moving all of your production traffic to the new configuration\.

For more information, see [Using CloudFront continuous deployment to safely test CDN configuration changes](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/continuous-deployment.html) in the *Amazon CloudFront Developer Guide*\.

## Syntax<a name="aws-resource-cloudfront-continuousdeploymentpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-continuousdeploymentpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::ContinuousDeploymentPolicy",
  "Properties" : {
      "[ContinuousDeploymentPolicyConfig](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig)" : ContinuousDeploymentPolicyConfig
    }
}
```

### YAML<a name="aws-resource-cloudfront-continuousdeploymentpolicy-syntax.yaml"></a>

```
Type: AWS::CloudFront::ContinuousDeploymentPolicy
Properties: 
  [ContinuousDeploymentPolicyConfig](#cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig): 
    ContinuousDeploymentPolicyConfig
```

## Properties<a name="aws-resource-cloudfront-continuousdeploymentpolicy-properties"></a>

`ContinuousDeploymentPolicyConfig`  <a name="cfn-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig"></a>
Contains the configuration for a continuous deployment policy\.  
*Required*: Yes  
*Type*: [ContinuousDeploymentPolicyConfig](aws-properties-cloudfront-continuousdeploymentpolicy-continuousdeploymentpolicyconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-continuousdeploymentpolicy-return-values"></a>

### Ref<a name="aws-resource-cloudfront-continuousdeploymentpolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier for the continuous deployment policy\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-continuousdeploymentpolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-continuousdeploymentpolicy-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The identifier of the cotinuous deployment policy\.

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
The date and time when the continuous deployment policy was last modified\.