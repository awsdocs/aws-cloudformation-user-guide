# AWS::CloudFormation::StackSet<a name="aws-resource-cloudformation-stackset"></a>

The `AWS::CloudFormation::StackSet` enables you to provision stacks into AWS accounts and across Regions by using a single CloudFormation template\. In the stack set, you specify the template to use, as well as any parameters and capabilities that the template requires\.

## Syntax<a name="aws-resource-cloudformation-stackset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-stackset-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::StackSet",
  "Properties" : {
      "[AdministrationRoleARN](#cfn-cloudformation-stackset-administrationrolearn)" : String,
      "[AutoDeployment](#cfn-cloudformation-stackset-autodeployment)" : AutoDeployment,
      "[Capabilities](#cfn-cloudformation-stackset-capabilities)" : [ String, ... ],
      "[Description](#cfn-cloudformation-stackset-description)" : String,
      "[ExecutionRoleName](#cfn-cloudformation-stackset-executionrolename)" : String,
      "[OperationPreferences](#cfn-cloudformation-stackset-operationpreferences)" : OperationPreferences,
      "[Parameters](#cfn-cloudformation-stackset-parameters)" : [ Parameter, ... ],
      "[PermissionModel](#cfn-cloudformation-stackset-permissionmodel)" : String,
      "[StackInstancesGroup](#cfn-cloudformation-stackset-stackinstancesgroup)" : [ StackInstances, ... ],
      "[StackSetName](#cfn-cloudformation-stackset-stacksetname)" : String,
      "[Tags](#cfn-cloudformation-stackset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TemplateBody](#cfn-cloudformation-stackset-templatebody)" : String,
      "[TemplateURL](#cfn-cloudformation-stackset-templateurl)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-stackset-syntax.yaml"></a>

```
Type: AWS::CloudFormation::StackSet
Properties: 
  [AdministrationRoleARN](#cfn-cloudformation-stackset-administrationrolearn): String
  [AutoDeployment](#cfn-cloudformation-stackset-autodeployment): 
    AutoDeployment
  [Capabilities](#cfn-cloudformation-stackset-capabilities): 
    - String
  [Description](#cfn-cloudformation-stackset-description): String
  [ExecutionRoleName](#cfn-cloudformation-stackset-executionrolename): String
  [OperationPreferences](#cfn-cloudformation-stackset-operationpreferences): 
    OperationPreferences
  [Parameters](#cfn-cloudformation-stackset-parameters): 
    - Parameter
  [PermissionModel](#cfn-cloudformation-stackset-permissionmodel): String
  [StackInstancesGroup](#cfn-cloudformation-stackset-stackinstancesgroup): 
    - StackInstances
  [StackSetName](#cfn-cloudformation-stackset-stacksetname): String
  [Tags](#cfn-cloudformation-stackset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TemplateBody](#cfn-cloudformation-stackset-templatebody): String
  [TemplateURL](#cfn-cloudformation-stackset-templateurl): String
```

## Properties<a name="aws-resource-cloudformation-stackset-properties"></a>

`AdministrationRoleARN`  <a name="cfn-cloudformation-stackset-administrationrolearn"></a>
The Amazon Resource Number \(ARN\) of the IAM role to use to create this stack set\. Specify an IAM role only if you are using customized administrator roles to control which users or groups can manage specific stack sets within the same administrator account\.  
Use customized administrator roles to control which users or groups can manage specific stack sets within the same administrator account\. For more information, see [Prerequisites: Granting Permissions for Stack Set Operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs.html) in the *AWS CloudFormation User Guide*\.  
*Minimum*: `20`  
*Maximum*: `2048`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoDeployment`  <a name="cfn-cloudformation-stackset-autodeployment"></a>
\[`Service-managed` permissions\] Describes whether StackSets automatically deploys to AWS Organizations accounts that are added to a target organization or organizational unit \(OU\)\.   
*Required*: No  
*Type*: [AutoDeployment](aws-properties-cloudformation-stackset-autodeployment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Capabilities`  <a name="cfn-cloudformation-stackset-capabilities"></a>
The capabilities that are allowed in the stack set\. Some stack set templates might include resources that can affect permissions in your AWS account—for example, by creating new AWS Identity and Access Management \(IAM\) users\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#capabilities)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-cloudformation-stackset-description"></a>
A description of the stack set\.  
*Minimum*: `1`  
*Maximum*: `1024`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleName`  <a name="cfn-cloudformation-stackset-executionrolename"></a>
The name of the IAM execution role to use to create the stack set\. If you do not specify an execution role, AWS CloudFormation uses the AWSCloudFormationStackSetExecutionRole role for the stack set operation\.  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[a-zA-Z_0-9+=,.@-]+`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperationPreferences`  <a name="cfn-cloudformation-stackset-operationpreferences"></a>
The user\-specified preferences for how AWS CloudFormation performs a stack set operation\.  
*Required*: No  
*Type*: [OperationPreferences](aws-properties-cloudformation-stackset-operationpreferences.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-cloudformation-stackset-parameters"></a>
The input parameters for the stack set template\.  
*Required*: No  
*Type*: List of [Parameter](aws-properties-cloudformation-stackset-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PermissionModel`  <a name="cfn-cloudformation-stackset-permissionmodel"></a>
Describes how the IAM roles required for stack set operations are created\.  
+ With `SELF_MANAGED` permissions, you must create the administrator and execution roles required to deploy to target accounts\. For more information, see [Grant Self\-Managed Stack Set Permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs-self-managed.html)\.
+ With `SERVICE_MANAGED` permissions, StackSets automatically creates the IAM roles required to deploy to accounts managed by AWS Organizations\. For more information, see [Grant Service\-Managed Stack Set Permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs-service-managed.html)\.
*Allowed Values*: `SERVICE_MANAGED` \| `SELF_MANAGED`  
The `PermissionModel` property is required\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StackInstancesGroup`  <a name="cfn-cloudformation-stackset-stackinstancesgroup"></a>
A group of stack instances with parameters in some specific accounts and Regions\.  
*Required*: No  
*Type*: List of [StackInstances](aws-properties-cloudformation-stackset-stackinstances.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetName`  <a name="cfn-cloudformation-stackset-stacksetname"></a>
The name to associate with the stack set\. The name must be unique in the Region where you create your stack set\.  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9-]{0,127}$`  
The `StackSetName` property is required\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-cloudformation-stackset-tags"></a>
The key\-value pairs to associate with this stack set and the stacks created from it\. AWS CloudFormation also propagates these tags to supported resources that are created in the stacks\. A maximum number of 50 tags can be specified\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateBody`  <a name="cfn-cloudformation-stackset-templatebody"></a>
The structure that contains the template body, with a minimum length of 1 byte and a maximum length of 51,200 bytes\.  
You must include either `TemplateURL` or `TemplateBody` in a StackSet, but you cannot use both\.  
*Minimum*: `1`  
*Maximum*: `51200`  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateURL`  <a name="cfn-cloudformation-stackset-templateurl"></a>
Location of file containing the template body\. The URL must point to a template \(max size: 460,800 bytes\) that is located in an Amazon S3 bucket\.  
You must include either `TemplateURL` or `TemplateBody` in a StackSet, but you cannot use both\.  
*Minimum*: `1`  
*Maximum*: `1024`  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudformation-stackset-return-values"></a>

### Ref<a name="aws-resource-cloudformation-stackset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the StackSetId\.

### Fn::GetAtt<a name="aws-resource-cloudformation-stackset-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\.

For more information about using the `Fn::GetAtt` instrinsic function, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-stackset-return-values-fn--getatt-fn--getatt"></a>

`StackSetId`  <a name="StackSetId-fn::getatt"></a>
The ID of the stack that you're creating\.