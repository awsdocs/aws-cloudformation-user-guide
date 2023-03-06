# AWS::SSO::PermissionSet<a name="aws-resource-sso-permissionset"></a>

Specifies a permission set within a specified IAM Identity Center instance\.

## Syntax<a name="aws-resource-sso-permissionset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sso-permissionset-syntax.json"></a>

```
{
  "Type" : "AWS::SSO::PermissionSet",
  "Properties" : {
      "[CustomerManagedPolicyReferences](#cfn-sso-permissionset-customermanagedpolicyreferences)" : [ CustomerManagedPolicyReference, ... ],
      "[Description](#cfn-sso-permissionset-description)" : String,
      "[InlinePolicy](#cfn-sso-permissionset-inlinepolicy)" : Json,
      "[InstanceArn](#cfn-sso-permissionset-instancearn)" : String,
      "[ManagedPolicies](#cfn-sso-permissionset-managedpolicies)" : [ String, ... ],
      "[Name](#cfn-sso-permissionset-name)" : String,
      "[PermissionsBoundary](#cfn-sso-permissionset-permissionsboundary)" : PermissionsBoundary,
      "[RelayStateType](#cfn-sso-permissionset-relaystatetype)" : String,
      "[SessionDuration](#cfn-sso-permissionset-sessionduration)" : String,
      "[Tags](#cfn-sso-permissionset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sso-permissionset-syntax.yaml"></a>

```
Type: AWS::SSO::PermissionSet
Properties: 
  [CustomerManagedPolicyReferences](#cfn-sso-permissionset-customermanagedpolicyreferences): 
    - CustomerManagedPolicyReference
  [Description](#cfn-sso-permissionset-description): String
  [InlinePolicy](#cfn-sso-permissionset-inlinepolicy): Json
  [InstanceArn](#cfn-sso-permissionset-instancearn): String
  [ManagedPolicies](#cfn-sso-permissionset-managedpolicies): 
    - String
  [Name](#cfn-sso-permissionset-name): String
  [PermissionsBoundary](#cfn-sso-permissionset-permissionsboundary): 
    PermissionsBoundary
  [RelayStateType](#cfn-sso-permissionset-relaystatetype): String
  [SessionDuration](#cfn-sso-permissionset-sessionduration): String
  [Tags](#cfn-sso-permissionset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sso-permissionset-properties"></a>

`CustomerManagedPolicyReferences`  <a name="cfn-sso-permissionset-customermanagedpolicyreferences"></a>
Specifies the names and paths of the customer managed policies that you have attached to your permission set\.  
*Required*: No  
*Type*: List of [CustomerManagedPolicyReference](aws-properties-sso-permissionset-customermanagedpolicyreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-sso-permissionset-description"></a>
The description of the [AWS::SSO::PermissionSet](#aws-resource-sso-permissionset)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `700`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u007E\u00A1-\u00FF]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InlinePolicy`  <a name="cfn-sso-permissionset-inlinepolicy"></a>
The inline policy that is attached to the permission set\.  
For `Length Constraints`, if a valid ARN is provided for a permission set, it is possible for an empty inline policy to be returned\.
*Required*: No  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `32768`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-sso-permissionset-instancearn"></a>
The ARN of the IAM Identity Center instance under which the operation will be executed\. For more information about ARNs, see [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `1224`  
*Pattern*: `arn:(aws|aws-us-gov|aws-cn|aws-iso|aws-iso-b):sso:::instance/(sso)?ins-[a-zA-Z0-9-.]{16}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ManagedPolicies`  <a name="cfn-sso-permissionset-managedpolicies"></a>
A structure that stores the details of the AWS managed policy\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-sso-permissionset-name"></a>
The name of the permission set\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PermissionsBoundary`  <a name="cfn-sso-permissionset-permissionsboundary"></a>
Specifies the configuration of the AWS managed or customer managed policy that you want to set as a permissions boundary\. Specify either `CustomerManagedPolicyReference` to use the name and path of a customer managed policy, or `ManagedPolicyArn` to use the ARN of an AWS managed policy\. A permissions boundary represents the maximum permissions that any policy can grant your role\. For more information, see [Permissions boundaries for IAM entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html) in the *IAM User Guide*\.  
Policies used as permissions boundaries don't provide permissions\. You must also attach an IAM policy to the role\. To learn how the effective permissions for a role are evaluated, see [IAM JSON policy evaluation logic](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html) in the *IAM User Guide*\.
*Required*: No  
*Type*: [PermissionsBoundary](aws-properties-sso-permissionset-permissionsboundary.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelayStateType`  <a name="cfn-sso-permissionset-relaystatetype"></a>
Used to redirect users within the application during the federation authentication process\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `240`  
*Pattern*: `[a-zA-Z0-9&$@#\\\/%?=~\-_'"|!:,.;*+\[\]\ \(\)\{\}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionDuration`  <a name="cfn-sso-permissionset-sessionduration"></a>
The length of time that the application user sessions are valid for in the ISO\-8601 standard\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^(-?)P(?=\d|T\d)(?:(\d+)Y)?(?:(\d+)M)?(?:(\d+)([DW]))?(?:T(?:(\d+)H)?(?:(\d+)M)?(?:(\d+(?:\.\d+)?)S)?)?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sso-permissionset-tags"></a>
The tags to attach to the new [AWS::SSO::PermissionSet](#aws-resource-sso-permissionset)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sso-permissionset-return-values"></a>

### Ref<a name="aws-resource-sso-permissionset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a generated ID, such as `permission-arn|sso-instance-arn`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sso-permissionset-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-sso-permissionset-return-values-fn--getatt-fn--getatt"></a>

`PermissionSetArn`  <a name="PermissionSetArn-fn::getatt"></a>
The permission set ARN of the permission set, such as `arn:aws:sso:::permissionSet/ins-instanceid/ps-permissionsetid`\.

## Examples<a name="aws-resource-sso-permissionset--examples"></a>



### Creating a new custom permission set for IAM Identity Center<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for_"></a>

The following example creates a custom permission set, `PermissionSet`, with a managed policies attachment and inline policy\.

#### JSON<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for_--json"></a>

```
{
  "PermissionSet": {
    "Type": "AWS::SSO::PermissionSet",
    "Properties": {
      "InstanceArn": "arn:aws:sso:::instance/ssoins-instanceId",
      "Name": "PermissionSet",
      "Description": "This is a sample permission set.",
      "SessionDuration": "PT8H",
      "ManagedPolicies": [
         "arn:aws:iam::aws:policy/AdministratorAccess"
      ],
      "InlinePolicy": "Inline policy json string",
      "Tags": [
        {
          "Key": "tagKey",
          "Value": "tagValue"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for_--yaml"></a>

```
PermissionSet:
  Type: AWS::SSO::PermissionSet
    Properties:
    InstanceArn: 'arn:aws:sso:::instance/ssoins-instanceId'
    Name: 'PermissionSet'
    Description: 'This is a sample permission set.'
    SessionDuration: 'PT8H'
    ManagedPolicies:
      - 'arn:aws:iam::aws:policy/AdministratorAccess'  
    InlinePolicy: 'Inline policy json string'
    Tags:
      - Key: tagKey
        Value: tagValue
```

### Creating a new custom permission set for IAM Identity Center with a customer managed policy as a permissions boundary<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for__with_a_customer_managed_policy_as_a_permissions_boundary"></a>

The following example creates a custom permission set, `PermissionSetWithCmpPb`, with policies attached and a customer managed policy as a permissions boundary\.

#### JSON<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for__with_a_customer_managed_policy_as_a_permissions_boundary--json"></a>

```
{
  "PermissionSetWithCustomerManagedPolicyReferenceForPermissionsBoundary": {
    "Type": "AWS::SSO::PermissionSet",
    "Properties": {
      "InstanceArn": "arn:aws:sso:::instance/ssoins-instanceId",
      "Name": "PermissionSetWithCmpPb",
      "Description": "This is a sample permission set.",
      "SessionDuration": "PT8H",
      "ManagedPolicies": [
        "arn:aws:iam::aws:policy/AdministratorAccess"
      ],
      "CustomerManagedPolicyReferences": [{
          "Name": "MyCustomPolicyName",
          "Path": "/myCustomPath/"
        },
        {
          "Name": "AnotherCustomPolicyName",
        },
        {
          "Name": "YetAnotherCustomPolicyName",
          "Path": "/"
        }
      ],
      "PermissionsBoundary": {
        "CustomerManagedPolicyReference": {
          "Name": "PolicyName",
          "Path": "/myPolicyPath/"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for__with_a_customer_managed_policy_as_a_permissions_boundary--yaml"></a>

```
PermissionSetWithCustomerManagedPolicyReferenceForPermissionsBoundary:
  Type: AWS::SSO::PermissionSet
   Properties:
     InstanceArn: 'arn:aws:sso:::instance/ssoins-instanceId'
     Name: 'PermissionSetWithCmpPb'
     Description: 'This is a sample permission set.'
     SessionDuration: 'PT8H'
     ManagedPolicies:
     - 'arn:aws:iam::aws:policy/AdministratorAccess'
     CustomerManagedPolicyReferences:
     - Name: 'MyCustomPolicyName'
       Path: '/myCustomPath/'
     - Name: 'AnotherCustomPolicyName'
     - Name: 'YetAnotherCustomPolicyName'
       Path: '/'
     PermissionsBoundary:
       CustomerManagedPolicyReference:
         Name: PolicyName
         Path: /myPolicyPath/
```

### Creating a new custom permission set for IAM Identity Center with an AWS managed policy as a permissions boundary<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for__with_an__managed_policy_as_a_permissions_boundary"></a>

The following example creates a custom permission set, `PermissionSetWithAmpPb`, with policies attached and an AWS managed policy as a permissions boundary\.

#### JSON<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for__with_an__managed_policy_as_a_permissions_boundary--json"></a>

```
{
  "PermissionSetWithAWSManagedPolicyForPermissionsBoundary": {
    "Type": "AWS::SSO::PermissionSet",
    "Properties": {
      "InstanceArn": "arn:aws:sso:::instance/ssoins-instanceId",
      "Name": "PermissionSetWithAmpPb",
      "Description": "This is a sample permission set.",
      "SessionDuration": "PT8H",
      "ManagedPolicies": [
        "arn:aws:iam::aws:policy/AdministratorAccess"
      ],
      "CustomerManagedPolicyReferences": [{
          "Name": "MyCustomPolicyName",
          "Path": "/myCustomPath/"
        },
        {
          "Name": "AnotherCustomPolicyName",
        },
        {
          "Name": "YetAnotherCustomPolicyName",
          "Path": "/"
        }
      ],
      "PermissionsBoundary": {
        "ManagedPolicyArn": {
          "Fn::Sub": "arn:aws:iam::aws:policy/ReadOnlyAccess"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for__with_an__managed_policy_as_a_permissions_boundary--yaml"></a>

```
PermissionSetWithAwsManagedPolicyForPermissionsBoundary:
  Type: AWS::SSO::PermissionSet
    Properties:
      InstanceArn: 'arn:aws:sso:::instance/ssoins-instanceId'
      Name: 'PermissionSetWithAmpPb'
      Description: 'This is a sample permission set.'
      SessionDuration: 'PT8H'
      ManagedPolicies:
         - 'arn:aws:iam::aws:policy/AdministratorAccess'
      CustomerManagedPolicyReferences:
        - Name: 'MyCustomPolicy'
          Path: '/myCustomPath/'
        - Name: 'AnotherCustomPolicy'
        - Name: YetAnotherCustomPolicyName
          Path: /
      PermissionsBoundary:
        ManagedPolicyArn: arn:aws:iam::aws:policy/ReadOnlyAccess'
```