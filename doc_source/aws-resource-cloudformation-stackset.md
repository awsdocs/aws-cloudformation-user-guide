# AWS::CloudFormation::StackSet<a name="aws-resource-cloudformation-stackset"></a>

The `AWS::CloudFormation::StackSet` enables you to provision stacks into AWS accounts and across Regions by using a single CloudFormation template\. In the stack set, you specify the template to use, in addition to any parameters and capabilities that the template requires\.

## Syntax<a name="aws-resource-cloudformation-stackset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-stackset-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::StackSet",
  "Properties" : {
      "[AdministrationRoleARN](#cfn-cloudformation-stackset-administrationrolearn)" : String,
      "[AutoDeployment](#cfn-cloudformation-stackset-autodeployment)" : AutoDeployment,
      "[CallAs](#cfn-cloudformation-stackset-callas)" : String,
      "[Capabilities](#cfn-cloudformation-stackset-capabilities)" : [ String, ... ],
      "[Description](#cfn-cloudformation-stackset-description)" : String,
      "[ExecutionRoleName](#cfn-cloudformation-stackset-executionrolename)" : String,
      "[ManagedExecution](#cfn-cloudformation-stackset-managedexecution)" : ManagedExecution,
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
  [CallAs](#cfn-cloudformation-stackset-callas): String
  [Capabilities](#cfn-cloudformation-stackset-capabilities): 
    - String
  [Description](#cfn-cloudformation-stackset-description): String
  [ExecutionRoleName](#cfn-cloudformation-stackset-executionrolename): String
  [ManagedExecution](#cfn-cloudformation-stackset-managedexecution): 
    ManagedExecution
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

`CallAs`  <a name="cfn-cloudformation-stackset-callas"></a>
\[Service\-managed permissions\] Specifies whether you are acting as an account administrator in the organization's management account or as a delegated administrator in a member account\.  
By default, `SELF` is specified\. Use `SELF` for stack sets with self\-managed permissions\.  
+ To create a stack set with service\-managed permissions while signed in to the management account, specify `SELF`\.
+ To create a stack set with service\-managed permissions while signed in to a delegated administrator account, specify `DELEGATED_ADMIN`\.

  Your AWS account must be registered as a delegated admin in the management account\. For more information, see [Register a delegated administrator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-delegated-admin.html) in the *AWS CloudFormation User Guide*\.
Stack sets with service\-managed permissions are created in the management account, including stack sets that are created by delegated administrators\.  
*Valid Values*: `SELF` \| `DELEGATED_ADMIN`  
*Required*: No  
*Type*: String  
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
The name of the IAM execution role to use to create the stack set\. If you don't specify an execution role, AWS CloudFormation uses the `AWSCloudFormationStackSetExecutionRole` role for the stack set operation\.  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[a-zA-Z_0-9+=,.@-]+`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedExecution`  <a name="cfn-cloudformation-stackset-managedexecution"></a>
Describes whether StackSets performs non\-conflicting operations concurrently and queues conflicting operations\.  
When active, StackSets performs non\-conflicting operations concurrently and queues conflicting operations\. After conflicting operations finish, StackSets starts queued operations in request order\.  
If there are already running or queued operations, StackSets queues all incoming operations even if they are non\-conflicting\.  
You can't modify your stack set's execution configuration while there are running or queued operations for that stack set\.
When inactive \(default\), StackSets performs one operation at a time in request order\.  
*Required*: No  
*Type*: [ManagedExecution](aws-properties-cloudformation-stackset-managedexecution.md)  
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
*Allowed values*: `SELF_MANAGED | SERVICE_MANAGED`  
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
You must include either `TemplateURL` or `TemplateBody` in a StackSet, but you can't use both\. Dynamic references in the `TemplateBody` may not work correctly in all cases\. It's recommended to pass templates containing dynamic references through `TemplateUrl` instead\.  
*Minimum*: `1`  
*Maximum*: `51200`  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateURL`  <a name="cfn-cloudformation-stackset-templateurl"></a>
Location of file containing the template body\. The URL must point to a template \(max size: 460,800 bytes\) that's located in an Amazon S3 bucket\.  
You must include either `TemplateURL` or `TemplateBody` in a StackSet, but you can't use both\.  
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

For more information about using the `Fn::GetAtt` intrinsic function, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-stackset-return-values-fn--getatt-fn--getatt"></a>

`StackSetId`  <a name="StackSetId-fn::getatt"></a>
The ID of the stack that you're creating\.

## Examples<a name="aws-resource-cloudformation-stackset--examples"></a>



### Activate managed execution for your stack set<a name="aws-resource-cloudformation-stackset--examples--Activate_managed_execution_for_your_stack_set"></a>

The following example creates a stack set and specifies `ManagedExecution`\. With managed execution activated, StackSets performs non\-conflicting operations concurrently and queues conflicting operations\.

#### JSON<a name="aws-resource-cloudformation-stackset--examples--Activate_managed_execution_for_your_stack_set--json"></a>

```
{
    "TestStackSet1": {
        "Type": "AWS::CloudFormation::StackSet",
        "DeletionPolicy": "Retain",
        "Properties": {
            "StackSetName": "TestStackSet12345",
            "Description": "Updatedescription1",
            "PermissionModel": "SELF_MANAGED",
            "ManagedExecution": {
                "Active": true
            },
            "Tags": [
                {
                    "Key": "tag1",
                    "Value": "value1"
                }
            ],
            "TemplateBody": "{\n  \"AWSTemplateFormatVersion\": \"2010-09-09\",\n  \"Resources\": {\n    \"testWaitHandle\": {\n      \"Type\": \"AWS::CloudFormation::WaitConditionHandle\"\n    }\n  }\n}\n"
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-stackset--examples--Activate_managed_execution_for_your_stack_set--yaml"></a>

```
TestStackSet1:
  Type: 'AWS::CloudFormation::StackSet'
  DeletionPolicy: Retain
  Properties:
    StackSetName: TestStackSet12345
    Description: Updatedescription1
    PermissionModel: SELF_MANAGED
    ManagedExecution:
      Active: true
    Tags:
      - Key: tag1
        Value: value1
    TemplateBody: |
      {
        "AWSTemplateFormatVersion": "2010-09-09",
        "Resources": {
          "testWaitHandle": {
            "Type": "AWS::CloudFormation::WaitConditionHandle"
          }
        }
      }
```

### Specifying Secrets Manager secrets in CloudFormation<a name="aws-resource-cloudformation-stackset--examples--Specifying__secrets_in_"></a>

When using the `TemplateBody` property, if the template intends to resolve secrets from Secrets Manager secret's through an `ARN` and `!Join` is used to construct Secrets Manager's dynamic reference, secret's resolution needs to be avoided at stack level so that it will only be performed upon stack instance creation\.

In the following example, secret's resolution are avoided at stack level by providing `{{` and `resolve:secretsmanager:` as separate strings to \!Join instead of `{{resolve:secretsmanager:` being provided as a single string:

#### JSON<a name="aws-resource-cloudformation-stackset--examples--Specifying__secrets_in_--json"></a>

```
{
    "Fn::Join": [
        "",
        [
            "{{",
            "resolve:secretsmanager:",
            {
                "Fn::Sub": "arn:aws:secretsmanager:${AWS::Region}:${AWS::AccountId}:secret:my-secret"
            },
            "::my-secret-key::}}"
        ]
    ]
}
```

#### YAML<a name="aws-resource-cloudformation-stackset--examples--Specifying__secrets_in_--yaml"></a>

```
!Join 
- ''
- - '{{'
  - 'resolve:secretsmanager:'
  - !Sub 'arn:aws:secretsmanager:${AWS::Region}:${AWS::AccountId}:secret:my-secret'
  - '::my-secret-key::}}'
```

## See also<a name="aws-resource-cloudformation-stackset--seealso"></a>
+ [AWS CloudFormation StackSets sample templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-sampletemplates.html)

