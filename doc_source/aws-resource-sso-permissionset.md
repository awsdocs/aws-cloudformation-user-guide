# AWS::SSO::PermissionSet<a name="aws-resource-sso-permissionset"></a>

Specifies a permission set within a specified SSO instance\.

## Syntax<a name="aws-resource-sso-permissionset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sso-permissionset-syntax.json"></a>

```
{
  "Type" : "AWS::SSO::PermissionSet",
  "Properties" : {
      "[Description](#cfn-sso-permissionset-description)" : String,
      "[InlinePolicy](#cfn-sso-permissionset-inlinepolicy)" : String,
      "[InstanceArn](#cfn-sso-permissionset-instancearn)" : String,
      "[ManagedPolicies](#cfn-sso-permissionset-managedpolicies)" : [ String, ... ],
      "[Name](#cfn-sso-permissionset-name)" : String,
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
  [Description](#cfn-sso-permissionset-description): String
  [InlinePolicy](#cfn-sso-permissionset-inlinepolicy): String
  [InstanceArn](#cfn-sso-permissionset-instancearn): String
  [ManagedPolicies](#cfn-sso-permissionset-managedpolicies): 
    - String
  [Name](#cfn-sso-permissionset-name): String
  [RelayStateType](#cfn-sso-permissionset-relaystatetype): String
  [SessionDuration](#cfn-sso-permissionset-sessionduration): String
  [Tags](#cfn-sso-permissionset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sso-permissionset-properties"></a>

`Description`  <a name="cfn-sso-permissionset-description"></a>
The description of the [AWS::SSO::PermissionSet](#aws-resource-sso-permissionset)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `700`  
*Pattern*: `[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InlinePolicy`  <a name="cfn-sso-permissionset-inlinepolicy"></a>
The IAM inline policy that is attached to the permission set\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `10240`  
*Pattern*: `[\u0009\u000A\u000D\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-sso-permissionset-instancearn"></a>
The ARN of the SSO instance under which the operation will be executed\. For more information about ARNs, see [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `1224`  
*Pattern*: `arn:aws:sso:::instance/(sso)?ins-[a-zA-Z0-9-.]{16}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ManagedPolicies`  <a name="cfn-sso-permissionset-managedpolicies"></a>
A structure that stores the details of the IAM managed policy\.  
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



### Creating a new custom permission set for AWS SSO<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for_AWS_SSO"></a>

The following example creates a custom permission set `“PermissionSet”` with a managed policies attachment and inline policy\.

#### JSON<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for_AWS_SSO--json"></a>

```
{
   "PermissionSet": {
      "Type": "AWS::SSO::PermissionSet",
      "Properties": {
         "InstanceArn": "arn:aws:sso:::instance/ssoins-instanceId",
         "Name": "PermissionSet",
         "Description": "This is a sample permission set.",
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

#### YAML<a name="aws-resource-sso-permissionset--examples--Creating_a_new_custom_permission_set_for_AWS_SSO--yaml"></a>

```
PermissionSet:
    Type: AWS::SSO::PermissionSet
    Properties:
      InstanceArn: 'arn:aws:sso:::instance/ssoins-instanceId'
      Name: 'PermissionSet'
      Description: 'This is a sample permission set.'
      ManagedPolicies:
        - 'arn:aws:iam::aws:policy/AdministratorAccess'
      InlinePolicy: 'Inline policy json string'
      Tags:
        - Key: tagKey
          Value: tagValue
```