# AWS::EC2::VerifiedAccessGroup<a name="aws-resource-ec2-verifiedaccessgroup"></a>

Describes a Verified Access group\.

## Syntax<a name="aws-resource-ec2-verifiedaccessgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-verifiedaccessgroup-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VerifiedAccessGroup",
  "Properties" : {
      "[Description](#cfn-ec2-verifiedaccessgroup-description)" : String,
      "[PolicyDocument](#cfn-ec2-verifiedaccessgroup-policydocument)" : String,
      "[PolicyEnabled](#cfn-ec2-verifiedaccessgroup-policyenabled)" : Boolean,
      "[Tags](#cfn-ec2-verifiedaccessgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VerifiedAccessInstanceId](#cfn-ec2-verifiedaccessgroup-verifiedaccessinstanceid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-verifiedaccessgroup-syntax.yaml"></a>

```
Type: AWS::EC2::VerifiedAccessGroup
Properties: 
  [Description](#cfn-ec2-verifiedaccessgroup-description): String
  [PolicyDocument](#cfn-ec2-verifiedaccessgroup-policydocument): String
  [PolicyEnabled](#cfn-ec2-verifiedaccessgroup-policyenabled): Boolean
  [Tags](#cfn-ec2-verifiedaccessgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VerifiedAccessInstanceId](#cfn-ec2-verifiedaccessgroup-verifiedaccessinstanceid): String
```

## Properties<a name="aws-resource-ec2-verifiedaccessgroup-properties"></a>

`Description`  <a name="cfn-ec2-verifiedaccessgroup-description"></a>
A description for the AWS Verified Access group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyDocument`  <a name="cfn-ec2-verifiedaccessgroup-policydocument"></a>
The Verified Access policy document\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyEnabled`  <a name="cfn-ec2-verifiedaccessgroup-policyenabled"></a>
The status of the Verified Access policy\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-verifiedaccessgroup-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifiedAccessInstanceId`  <a name="cfn-ec2-verifiedaccessgroup-verifiedaccessinstanceid"></a>
The ID of the AWS Verified Access instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-verifiedaccessgroup-return-values"></a>

### Ref<a name="aws-resource-ec2-verifiedaccessgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ID of the Verified Access group\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-verifiedaccessgroup-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-verifiedaccessgroup-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The creation time\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The last updated time\.

`Owner`  <a name="Owner-fn::getatt"></a>
The ID of the AWS account that owns the group\.

`VerifiedAccessGroupArn`  <a name="VerifiedAccessGroupArn-fn::getatt"></a>
The ARN of the Verified Access group\.

`VerifiedAccessGroupId`  <a name="VerifiedAccessGroupId-fn::getatt"></a>
The ID of the Verified Access group\.