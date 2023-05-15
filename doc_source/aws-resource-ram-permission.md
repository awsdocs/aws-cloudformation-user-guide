# AWS::RAM::Permission<a name="aws-resource-ram-permission"></a>

Creates a customer managed permission for a specified resource type that you can attach to resource shares\. It is created in the AWS Region in which you call the operation\.

## Syntax<a name="aws-resource-ram-permission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ram-permission-syntax.json"></a>

```
{
  "Type" : "AWS::RAM::Permission",
  "Properties" : {
      "[Name](#cfn-ram-permission-name)" : String,
      "[PolicyTemplate](#cfn-ram-permission-policytemplate)" : Json,
      "[ResourceType](#cfn-ram-permission-resourcetype)" : String,
      "[Tags](#cfn-ram-permission-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ram-permission-syntax.yaml"></a>

```
Type: AWS::RAM::Permission
Properties: 
  [Name](#cfn-ram-permission-name): String
  [PolicyTemplate](#cfn-ram-permission-policytemplate): Json
  [ResourceType](#cfn-ram-permission-resourcetype): String
  [Tags](#cfn-ram-permission-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ram-permission-properties"></a>

`Name`  <a name="cfn-ram-permission-name"></a>
Specifies the name of the customer managed permission\. The name must be unique within the AWS Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `36`  
*Pattern*: `[\w.-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyTemplate`  <a name="cfn-ram-permission-policytemplate"></a>
A string in JSON format string that contains the following elements of a resource\-based policy:  
+  **Effect**: must be set to `ALLOW`\.
+  **Action**: specifies the actions that are allowed by this customer managed permission\. The list must contain only actions that are supported by the specified resource type\. For a list of all actions supported by each resource type, see [Actions, resources, and condition keys for AWS services](https://docs.aws.amazon.com/service-authorization/latest/reference/reference_policies_actions-resources-contextkeys.html) in the * AWS Identity and Access Management User Guide*\.
+  **Condition**: \(optional\) specifies conditional parameters that must evaluate to true when a user attempts an action for that action to be allowed\. For more information about the Condition element, see [IAM policies: Condition element](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements_condition.html) in the * AWS Identity and Access Management User Guide*\.
This template can't include either the `Resource` or `Principal` elements\. Those are both filled in by AWS RAM when it instantiates the resource\-based policy on each resource shared using this managed permission\. The `Resource` comes from the ARN of the specific resource that you are sharing\. The `Principal` comes from the list of identities added to the resource share\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceType`  <a name="cfn-ram-permission-resourcetype"></a>
Specifies the name of the resource type that this customer managed permission applies to\.  
The format is ` <service-code>:<resource-type> ` and is not case sensitive\. For example, to specify an Amazon EC2 Subnet, you can use the string `ec2:subnet`\. To see the list of valid values for this parameter, query the [ListResourceTypes](https://docs.aws.amazon.com/ram/latest/APIReference/API_ListResourceTypes.html) operation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ram-permission-tags"></a>
Specifies a list of one or more tag key and value pairs to attach to the permission\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ram-permission-return-values"></a>

### Ref<a name="aws-resource-ram-permission-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN of the permission\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ram-permission-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ram-permission-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the new permission\.

`IsResourceTypeDefault`  <a name="IsResourceTypeDefault-fn::getatt"></a>
Specifies whether this permission is the default for new resource shares that include resources of the associated resource type\.

`PermissionType`  <a name="PermissionType-fn::getatt"></a>
The type of managed permission\. This can be one of the following values:  
+ **AWS\_MANAGED\_PERMISSION** – AWS created and manages this managed permission\. You can associate it with your resource shares, but you can't modify it\.
+ **CUSTOMER\_MANAGED\_PERMISSION** – You, or another principal in your account created this managed permission\. You can associate it with your resource shares and create new versions that have different permissions\.

`Version`  <a name="Version-fn::getatt"></a>
The version number for this version of the permission\.

## See also<a name="aws-resource-ram-permission--seealso"></a>
+  [CreatePermission](https://docs.aws.amazon.com/ram/latest/APIReference/API_CreatePermission.html) in the * AWS Resource Access Manager API Reference* 
+  [AWS Resource Access Manager User Guide](https://docs.aws.amazon.com/ram/latest/userguide) 

