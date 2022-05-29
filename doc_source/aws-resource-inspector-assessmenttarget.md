# AWS::Inspector::AssessmentTarget<a name="aws-resource-inspector-assessmenttarget"></a>

The `AWS::Inspector::AssessmentTarget` resource is used to create Amazon Inspector assessment targets, which specify the Amazon EC2 instances that will be analyzed during an assessment run\.

## Syntax<a name="aws-resource-inspector-assessmenttarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-inspector-assessmenttarget-syntax.json"></a>

```
{
  "Type" : "AWS::Inspector::AssessmentTarget",
  "Properties" : {
      "[AssessmentTargetName](#cfn-inspector-assessmenttarget-assessmenttargetname)" : String,
      "[ResourceGroupArn](#cfn-inspector-assessmenttarget-resourcegrouparn)" : String
    }
}
```

### YAML<a name="aws-resource-inspector-assessmenttarget-syntax.yaml"></a>

```
Type: AWS::Inspector::AssessmentTarget
Properties: 
  [AssessmentTargetName](#cfn-inspector-assessmenttarget-assessmenttargetname): String
  [ResourceGroupArn](#cfn-inspector-assessmenttarget-resourcegrouparn): String
```

## Properties<a name="aws-resource-inspector-assessmenttarget-properties"></a>

`AssessmentTargetName`  <a name="cfn-inspector-assessmenttarget-assessmenttargetname"></a>
The name of the Amazon Inspector assessment target\. The name must be unique within the AWS account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceGroupArn`  <a name="cfn-inspector-assessmenttarget-resourcegrouparn"></a>
The ARN that specifies the resource group that is used to create the assessment target\. If `resourceGroupArn` is not specified, all EC2 instances in the current AWS account and Region are included in the assessment target\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-inspector-assessmenttarget-return-values"></a>

### Ref<a name="aws-resource-inspector-assessmenttarget-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ResourceGroupArn` of the new assessment target\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-inspector-assessmenttarget-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-inspector-assessmenttarget-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) that specifies the assessment target that is created\.

## Examples<a name="aws-resource-inspector-assessmenttarget--examples"></a>



### Declaring an Amazon Inspector Assessment Target Resource<a name="aws-resource-inspector-assessmenttarget--examples--Declaring_an_Amazon_Inspector_Assessment_Target_Resource"></a>

The following examples show how to declare an `AWS::Inspector::AssessmentTarget` resource to create an Amazon Inspector assessment target\.

#### JSON<a name="aws-resource-inspector-assessmenttarget--examples--Declaring_an_Amazon_Inspector_Assessment_Target_Resource--json"></a>

```
"myassessmenttarget": {
  "Type": "AWS::Inspector::AssessmentTarget",
  "Properties": {
    "AssessmentTargetName" : "MyAssessmentTarget",
    "ResourceGroupArn" : "arn:aws:inspector:us-west-2:123456789012:resourcegroup/0-AB6DMKnv"
  }
}
```

#### YAML<a name="aws-resource-inspector-assessmenttarget--examples--Declaring_an_Amazon_Inspector_Assessment_Target_Resource--yaml"></a>

```
myassessmenttarget: 
  Type: AWS::Inspector::AssessmentTarget
  Properties: 
      AssessmentTargetName : "MyAssessmentTarget"
      ResourceGroupArn : "arn:aws:inspector:us-west-2:123456789012:resourcegroup/0-AB6DMKnv"
```