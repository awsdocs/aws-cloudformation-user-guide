# AWS::Route53RecoveryReadiness::ReadinessCheck<a name="aws-resource-route53recoveryreadiness-readinesscheck"></a>

Creates a readiness check in an account\. A readiness check monitors a resource set in your application, such as a set of Amazon Aurora instances, that Application Recovery Controller is auditing recovery readiness for\. The audits run once every minute on every resource that's associated with a readiness check\.

## Syntax<a name="aws-resource-route53recoveryreadiness-readinesscheck-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53recoveryreadiness-readinesscheck-syntax.json"></a>

```
{
  "Type" : "AWS::Route53RecoveryReadiness::ReadinessCheck",
  "Properties" : {
      "[ReadinessCheckName](#cfn-route53recoveryreadiness-readinesscheck-readinesscheckname)" : String,
      "[ResourceSetName](#cfn-route53recoveryreadiness-readinesscheck-resourcesetname)" : String,
      "[Tags](#cfn-route53recoveryreadiness-readinesscheck-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53recoveryreadiness-readinesscheck-syntax.yaml"></a>

```
Type: AWS::Route53RecoveryReadiness::ReadinessCheck
Properties: 
  [ReadinessCheckName](#cfn-route53recoveryreadiness-readinesscheck-readinesscheckname): String
  [ResourceSetName](#cfn-route53recoveryreadiness-readinesscheck-resourcesetname): String
  [Tags](#cfn-route53recoveryreadiness-readinesscheck-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53recoveryreadiness-readinesscheck-properties"></a>

`ReadinessCheckName`  <a name="cfn-route53recoveryreadiness-readinesscheck-readinesscheckname"></a>
The name of the readiness check to create\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceSetName`  <a name="cfn-route53recoveryreadiness-readinesscheck-resourcesetname"></a>
The name of the resource set to check\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-route53recoveryreadiness-readinesscheck-tags"></a>
A collection of tags associated with a resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53recoveryreadiness-readinesscheck-return-values"></a>

### Ref<a name="aws-resource-route53recoveryreadiness-readinesscheck-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ReadinessCheckName`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53recoveryreadiness-readinesscheck-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53recoveryreadiness-readinesscheck-return-values-fn--getatt-fn--getatt"></a>

`ReadinessCheckArn`  <a name="ReadinessCheckArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the readiness check\. 