# AWS::VpcLattice::TargetGroup<a name="aws-resource-vpclattice-targetgroup"></a>

Creates a target group\. A target group is a collection of targets, or compute resources, that run your application or service\. A target group can only be used by a single service\.

For more information, see [Target groups](https://docs.aws.amazon.com/vpc-lattice/latest/ug/target-groups.html) in the *Amazon VPC Lattice User Guide*\.

## Syntax<a name="aws-resource-vpclattice-targetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-vpclattice-targetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::VpcLattice::TargetGroup",
  "Properties" : {
      "[Config](#cfn-vpclattice-targetgroup-config)" : TargetGroupConfig,
      "[Name](#cfn-vpclattice-targetgroup-name)" : String,
      "[Tags](#cfn-vpclattice-targetgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Targets](#cfn-vpclattice-targetgroup-targets)" : [ Target, ... ],
      "[Type](#cfn-vpclattice-targetgroup-type)" : String
    }
}
```

### YAML<a name="aws-resource-vpclattice-targetgroup-syntax.yaml"></a>

```
Type: AWS::VpcLattice::TargetGroup
Properties: 
  [Config](#cfn-vpclattice-targetgroup-config): 
    TargetGroupConfig
  [Name](#cfn-vpclattice-targetgroup-name): String
  [Tags](#cfn-vpclattice-targetgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Targets](#cfn-vpclattice-targetgroup-targets): 
    - Target
  [Type](#cfn-vpclattice-targetgroup-type): String
```

## Properties<a name="aws-resource-vpclattice-targetgroup-properties"></a>

`Config`  <a name="cfn-vpclattice-targetgroup-config"></a>
The target group configuration\.  
*Required*: No  
*Type*: [TargetGroupConfig](aws-properties-vpclattice-targetgroup-targetgroupconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-vpclattice-targetgroup-name"></a>
The name of the target group\. The name must be unique within the account\. The valid characters are a\-z, 0\-9, and hyphens \(\-\)\. You can't use a hyphen as the first or last character, or immediately after another hyphen\.  
If you don't specify a name, CloudFormation generates one\. However, if you specify a name, and later want to replace the resource, you must specify a new name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-vpclattice-targetgroup-tags"></a>
The tags for the target group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-vpclattice-targetgroup-targets"></a>
Describes a target\.  
*Required*: No  
*Type*: List of [Target](aws-properties-vpclattice-targetgroup-target.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-vpclattice-targetgroup-type"></a>
The type of target group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-vpclattice-targetgroup-return-values"></a>

### Ref<a name="aws-resource-vpclattice-targetgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the Amazon Resource Name \(ARN\) of the target group\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-vpclattice-targetgroup-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-vpclattice-targetgroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the target group\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The date and time that the target group was created, specified in ISO\-8601 format\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the target group\.

`LastUpdatedAt`  <a name="LastUpdatedAt-fn::getatt"></a>
The date and time that the target group was last updated, specified in ISO\-8601 format\.

`Status`  <a name="Status-fn::getatt"></a>
The operation's status\. You can retry the operation if the status is `CREATE_FAILED`\. However, if you retry it while the status is `CREATE_IN_PROGRESS`, there is no change in the status\. 