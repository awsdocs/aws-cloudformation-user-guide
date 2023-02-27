# AWS::Connect::UserHierarchyGroup<a name="aws-resource-connect-userhierarchygroup"></a>

Specifies a new user hierarchy group\.

## Syntax<a name="aws-resource-connect-userhierarchygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-userhierarchygroup-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::UserHierarchyGroup",
  "Properties" : {
      "[InstanceArn](#cfn-connect-userhierarchygroup-instancearn)" : String,
      "[Name](#cfn-connect-userhierarchygroup-name)" : String,
      "[ParentGroupArn](#cfn-connect-userhierarchygroup-parentgrouparn)" : String
    }
}
```

### YAML<a name="aws-resource-connect-userhierarchygroup-syntax.yaml"></a>

```
Type: AWS::Connect::UserHierarchyGroup
Properties: 
  [InstanceArn](#cfn-connect-userhierarchygroup-instancearn): String
  [Name](#cfn-connect-userhierarchygroup-name): String
  [ParentGroupArn](#cfn-connect-userhierarchygroup-parentgrouparn): String
```

## Properties<a name="aws-resource-connect-userhierarchygroup-properties"></a>

`InstanceArn`  <a name="cfn-connect-userhierarchygroup-instancearn"></a>
The Amazon Resource Name \(ARN\) of the user hierarchy group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-userhierarchygroup-name"></a>
The name of the user hierarchy group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParentGroupArn`  <a name="cfn-connect-userhierarchygroup-parentgrouparn"></a>
The Amazon Resource Name \(ARN\) of the parent group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-connect-userhierarchygroup-return-values"></a>

### Ref<a name="aws-resource-connect-userhierarchygroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the user hierarchy group\. For example:

`{ "Ref": "myUserHierarchyGroup" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-userhierarchygroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-userhierarchygroup-return-values-fn--getatt-fn--getatt"></a>

`UserHierarchyGroupArn`  <a name="UserHierarchyGroupArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the user hierarchy group\.

## Examples<a name="aws-resource-connect-userhierarchygroup--examples"></a>



### Specify a user hierarchy group<a name="aws-resource-connect-userhierarchygroup--examples--Specify_a_user_hierarchy_group"></a>

The following example specifies a user hierarchy group for an Amazon Connect instance\. This example specifies a user hierachy group for the instance on top of existing HierarchyStructure

#### YAML<a name="aws-resource-connect-userhierarchygroup--examples--Specify_a_user_hierarchy_group--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a user hierarchy group for an Amazon Connect instance
Resources:
    HierarchyGroup:
    Type: 'AWS::Connect::UserHierarchyGroup'
    Properties:
      Name: 'exampleUserHierarchyGroup'
      InstanceArn: 'arn:aws:connect:region-name:aws-account-id:instance/instance-arn'
```