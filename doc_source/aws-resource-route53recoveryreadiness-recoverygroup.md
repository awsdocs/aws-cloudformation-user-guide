# AWS::Route53RecoveryReadiness::RecoveryGroup<a name="aws-resource-route53recoveryreadiness-recoverygroup"></a>

Creates a recovery group in Amazon Route 53 Application Recovery Controller\. A recovery group represents your application\. It typically consists of two or more cells that are replicas of each other in terms of resources and functionality, so that you can fail over from one to the other, for example, from one Region to another\. You create recovery groups so you can use readiness checks to audit resources in your application\.

For more information, see [Readiness checks, resource sets, and readiness scopes](https://docs.aws.amazon.com/r53recovery/latest/dg/recovery-readiness.recovery-groups.readiness-scope.html) in the Amazon Route 53 Application Recovery Controller Developer Guide\.

Route 53 ARC Readiness supports us\-east\-1 and us\-west\-2 AWS Regions only\.

## Syntax<a name="aws-resource-route53recoveryreadiness-recoverygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53recoveryreadiness-recoverygroup-syntax.json"></a>

```
{
  "Type" : "AWS::Route53RecoveryReadiness::RecoveryGroup",
  "Properties" : {
      "[Cells](#cfn-route53recoveryreadiness-recoverygroup-cells)" : [ String, ... ],
      "[RecoveryGroupName](#cfn-route53recoveryreadiness-recoverygroup-recoverygroupname)" : String,
      "[Tags](#cfn-route53recoveryreadiness-recoverygroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53recoveryreadiness-recoverygroup-syntax.yaml"></a>

```
Type: AWS::Route53RecoveryReadiness::RecoveryGroup
Properties: 
  [Cells](#cfn-route53recoveryreadiness-recoverygroup-cells): 
    - String
  [RecoveryGroupName](#cfn-route53recoveryreadiness-recoverygroup-recoverygroupname): String
  [Tags](#cfn-route53recoveryreadiness-recoverygroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53recoveryreadiness-recoverygroup-properties"></a>

`Cells`  <a name="cfn-route53recoveryreadiness-recoverygroup-cells"></a>
A list of the cell Amazon Resource Names \(ARNs\) in the recovery group\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecoveryGroupName`  <a name="cfn-route53recoveryreadiness-recoverygroup-recoverygroupname"></a>
The name of the recovery group to create\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-route53recoveryreadiness-recoverygroup-tags"></a>
A collection of tags associated with a resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53recoveryreadiness-recoverygroup-return-values"></a>

### Ref<a name="aws-resource-route53recoveryreadiness-recoverygroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the `RecoveryGroupName`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53recoveryreadiness-recoverygroup-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53recoveryreadiness-recoverygroup-return-values-fn--getatt-fn--getatt"></a>

`RecoveryGroupArn`  <a name="RecoveryGroupArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the recovery group\. 