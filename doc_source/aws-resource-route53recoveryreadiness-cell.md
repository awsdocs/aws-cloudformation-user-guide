# AWS::Route53RecoveryReadiness::Cell<a name="aws-resource-route53recoveryreadiness-cell"></a>

Creates a cell in an account\.

## Syntax<a name="aws-resource-route53recoveryreadiness-cell-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53recoveryreadiness-cell-syntax.json"></a>

```
{
  "Type" : "AWS::Route53RecoveryReadiness::Cell",
  "Properties" : {
      "[CellName](#cfn-route53recoveryreadiness-cell-cellname)" : String,
      "[Cells](#cfn-route53recoveryreadiness-cell-cells)" : [ String, ... ],
      "[Tags](#cfn-route53recoveryreadiness-cell-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53recoveryreadiness-cell-syntax.yaml"></a>

```
Type: AWS::Route53RecoveryReadiness::Cell
Properties: 
  [CellName](#cfn-route53recoveryreadiness-cell-cellname): String
  [Cells](#cfn-route53recoveryreadiness-cell-cells): 
    - String
  [Tags](#cfn-route53recoveryreadiness-cell-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53recoveryreadiness-cell-properties"></a>

`CellName`  <a name="cfn-route53recoveryreadiness-cell-cellname"></a>
The name of the cell to create\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Cells`  <a name="cfn-route53recoveryreadiness-cell-cells"></a>
A list of cell Amazon Resource Names \(ARNs\) contained within this cell, for use in nested cells\. For example, Availability Zones within specific AWS Regions\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-route53recoveryreadiness-cell-tags"></a>
A collection of tags associated with a resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53recoveryreadiness-cell-return-values"></a>

### Ref<a name="aws-resource-route53recoveryreadiness-cell-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `CellName`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53recoveryreadiness-cell-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53recoveryreadiness-cell-return-values-fn--getatt-fn--getatt"></a>

`CellArn`  <a name="CellArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the cell\. 

`ParentReadinessScopes`  <a name="ParentReadinessScopes-fn::getatt"></a>
The readiness scope for the cell, which can be a cell Amazon Resource Name \(ARN\) or a recovery group ARN\. This is a list but currently can have only one element\. 