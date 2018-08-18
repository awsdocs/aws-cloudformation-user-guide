# AWS::Inspector::AssessmentTarget<a name="aws-resource-inspector-assessmenttarget"></a>

The `AWS::Inspector::AssessmentTarget` resource creates an Amazon Inspector assessment target \- a resource that contains information about an Amazon Inspector application\. 

**Topics**
+ [Syntax](#aws-resource-inspector-assessmenttarget-syntax)
+ [Properties](#aws-resource-inspector-assessmenttarget-properties)
+ [Return Values](#aws-resource-inspector-assessmenttarget-returnvalues)
+ [Examples](#aws-resource-inspector-assessmenttarget-examples)

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
Type: "AWS::Inspector::AssessmentTarget"
Properties:
  [AssessmentTargetName](#cfn-inspector-assessmenttarget-assessmenttargetname): String
  [ResourceGroupArn](#cfn-inspector-assessmenttarget-resourcegrouparn): String
```

## Properties<a name="aws-resource-inspector-assessmenttarget-properties"></a>

`AssessmentTargetName`  <a name="cfn-inspector-assessmenttarget-assessmenttargetname"></a>
The name of the Amazon Inspector assessment target\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResourceGroupArn`  <a name="cfn-inspector-assessmenttarget-resourcegrouparn"></a>
The ARN that specifies the resource group that is associated with the assessment target\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-inspector-assessmenttarget-returnvalues"></a>

### Fn::GetAtt<a name="aws-resource-inspector-assessmenttarget-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) that specifies the assessment target that is created\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-inspector-assessmenttarget-examples"></a>

### Declaring an Amazon Inspector Assessment Target Resource<a name="aws-resource-inspector-assessmenttarget-example1"></a>

The following example shows how to declare an AWS::Inspector::AssessmentTarget resource to create an Amazon Inspector assessment target\. 

#### JSON<a name="aws-resource-inspector-assessmenttarget-example1.json"></a>

```
"myassessmenttarget": {
  "Type": "AWS::Inspector::AssessmentTarget",
  "Properties": {
    "AssessmentTargetName" : "MyAssessmentTarget",
    "ResourceGroupArn" : "arn:aws:inspector:us-west-2:123456789012:resourcegroup/0-AB6DMKnv"
  }
}
```

#### YAML<a name="aws-resource-inspector-assessmenttarget-example1.yaml"></a>

```
myassessmenttarget: 
  Type: "AWS::Inspector::AssessmentTarget"
  Properties: 
    AssessmentTargetName : "MyAssessmentTarget"
    ResourceGroupArn : "arn:aws:inspector:us-west-2:123456789012:resourcegroup/0-AB6DMKnv"
```