# AWS::CleanRooms::Membership<a name="aws-resource-cleanrooms-membership"></a>

Creates a membership for a specific collaboration identifier and joins the collaboration\.

## Syntax<a name="aws-resource-cleanrooms-membership-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cleanrooms-membership-syntax.json"></a>

```
{
  "Type" : "AWS::CleanRooms::Membership",
  "Properties" : {
      "[CollaborationIdentifier](#cfn-cleanrooms-membership-collaborationidentifier)" : String,
      "[QueryLogStatus](#cfn-cleanrooms-membership-querylogstatus)" : String,
      "[Tags](#cfn-cleanrooms-membership-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cleanrooms-membership-syntax.yaml"></a>

```
Type: AWS::CleanRooms::Membership
Properties: 
  [CollaborationIdentifier](#cfn-cleanrooms-membership-collaborationidentifier): String
  [QueryLogStatus](#cfn-cleanrooms-membership-querylogstatus): String
  [Tags](#cfn-cleanrooms-membership-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cleanrooms-membership-properties"></a>

`CollaborationIdentifier`  <a name="cfn-cleanrooms-membership-collaborationidentifier"></a>
The unique ID for the associated collaboration\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `.*[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`QueryLogStatus`  <a name="cfn-cleanrooms-membership-querylogstatus"></a>
An indicator as to whether query logging has been enabled or disabled for the collaboration\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cleanrooms-membership-tags"></a>
An optional label that you can assign to a resource when you create it\. Each tag consists of a key and an optional value, both of which you define\. When you use tagging, you can also use tag\-based access control in IAM policies to control access to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cleanrooms-membership-return-values"></a>

### Ref<a name="aws-resource-cleanrooms-membership-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the `MembershipId`, such as `a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`\. For example: 

`{ "Ref": "MyMembership" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cleanrooms-membership-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cleanrooms-membership-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the specified membership\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:membership/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`

`CollaborationArn`  <a name="CollaborationArn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the specified collaboration\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:collaboration/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`

`CollaborationCreatorAccountId`  <a name="CollaborationCreatorAccountId-fn::getatt"></a>
Returns the unique identifier of the specified collaboration creator account\.  
Example: `a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`

`MembershipIdentifier`  <a name="MembershipIdentifier-fn::getatt"></a>
Returns the unique identifier of the specified membership\.  
Example: `a1b2c3d4-5678-90ab-cdef-EXAMPLE22222`

## Remarks<a name="aws-resource-cleanrooms-membership--remarks"></a>

If you are a collaboration owner, ensure that you add `"DeletionPolicy: Retain"` and `"UpdateReplacePolicy: Retain"` to the `Membership` resource in your CloudFormation template\.

If your `Membership` resource depends on the collaboration explicitly or implicitly by using a `"Ref"` on the `Collaboration` \(`CollaborationIdentifier: !Ref Collaboration`\), CloudFormation tries to delete the `Membership` resource before the `Collaboration` resource\. However, this attempt will fail because collaboration owners must delete the collaboration before deleting their membership to the collaboration\.

For more information, see [DeletionPolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) and [UpdateReplacePolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatereplacepolicy.html)\.