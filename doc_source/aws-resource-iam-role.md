# AWS::IAM::Role<a name="aws-resource-iam-role"></a>

Creates a new role for your AWS account\. For more information about roles, go to [IAM Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/WorkingWithRoles.html)\. For information about limitations on role names and the number of roles you can create, go to [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-role-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-role-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::Role",
  "Properties" : {
      "[AssumeRolePolicyDocument](#cfn-iam-role-assumerolepolicydocument)" : Json,
      "[Description](#cfn-iam-role-description)" : String,
      "[ManagedPolicyArns](#cfn-iam-role-managepolicyarns)" : [ String, ... ],
      "[MaxSessionDuration](#cfn-iam-role-maxsessionduration)" : Integer,
      "[Path](#cfn-iam-role-path)" : String,
      "[PermissionsBoundary](#cfn-iam-role-permissionsboundary)" : String,
      "[Policies](#cfn-iam-role-policies)" : [ Policy, ... ],
      "[RoleName](#cfn-iam-role-rolename)" : String,
      "[Tags](#cfn-iam-role-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iam-role-syntax.yaml"></a>

```
Type: AWS::IAM::Role
Properties: 
  [AssumeRolePolicyDocument](#cfn-iam-role-assumerolepolicydocument): Json
  [Description](#cfn-iam-role-description): String
  [ManagedPolicyArns](#cfn-iam-role-managepolicyarns): 
    - String
  [MaxSessionDuration](#cfn-iam-role-maxsessionduration): Integer
  [Path](#cfn-iam-role-path): String
  [PermissionsBoundary](#cfn-iam-role-permissionsboundary): String
  [Policies](#cfn-iam-role-policies): 
    - Policy
  [RoleName](#cfn-iam-role-rolename): String
  [Tags](#cfn-iam-role-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iam-role-properties"></a>

`AssumeRolePolicyDocument`  <a name="cfn-iam-role-assumerolepolicydocument"></a>
The trust policy that is associated with this role\. Trust policies define which entities can assume the role\. You can associate only one trust policy with a role\. For an example of a policy that can be used to assume a role, see [Template Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html#aws-resource-iam-role--examples)\. For more information about the elements that you can use in an IAM policy, see [IAM Policy Elements Reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html) in the *IAM User Guide*\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iam-role-description"></a>
A description of the role that you provide\.  
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Pattern*: `[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedPolicyArns`  <a name="cfn-iam-role-managepolicyarns"></a>
A list of Amazon Resource Names \(ARNs\) of the IAM managed policies that you want to attach to the user\.  
For more information about ARNs, see [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSessionDuration`  <a name="cfn-iam-role-maxsessionduration"></a>
The maximum session duration \(in seconds\) that you want to set for the specified role\. If you do not specify a value for this setting, the default maximum of one hour is applied\. This setting can have a value from 1 hour to 12 hours\.  
Anyone who assumes the role from the AWS CLI or API can use the `DurationSeconds` API parameter or the `duration-seconds` CLI parameter to request a longer session\. The `MaxSessionDuration` setting determines the maximum duration that can be requested using the `DurationSeconds` parameter\. If users don't specify a value for the `DurationSeconds` parameter, their security credentials are valid for one hour by default\. This applies when you use the `AssumeRole*` API operations or the `assume-role*` CLI operations but does not apply when you use those operations to create a console URL\. For more information, see [Using IAM Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `3600`  
*Maximum*: `43200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-iam-role-path"></a>
 The path to the role\. For more information about paths, see [IAM Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html) in the *IAM User Guide*\.  
This parameter is optional\. If it is not included, it defaults to a slash \(/\)\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of either a forward slash \(/\) by itself or a string that must begin and end with forward slashes\. In addition, it can contain any ASCII character from the \! \(`\u0021`\) through the DEL character \(`\u007F`\), including most punctuation characters, digits, and upper and lowercased letters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `(\u002F)|(\u002F[\u0021-\u007F]+\u002F)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PermissionsBoundary`  <a name="cfn-iam-role-permissionsboundary"></a>
The ARN of the policy used to set the permissions boundary for the role\.  
For more information about permissions boundaries, see [Permissions Boundaries for IAM Identities ](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policies`  <a name="cfn-iam-role-policies"></a>
Adds or updates an inline policy document that is embedded in the specified IAM role\.  
When you embed an inline policy in a role, the inline policy is used as part of the role's access \(permissions\) policy\. The role's trust policy is created at the same time as the role\. You can update a role's trust policy later\. For more information about IAM roles, go to [Using Roles to Delegate Permissions and Federate Identities](https://docs.aws.amazon.com/IAM/latest/UserGuide/roles-toplevel.html)\.  
A role can also have an attached managed policy\. For information about policies, see [Managed Policies and Inline Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/policies-managed-vs-inline.html) in the *IAM User Guide*\.  
For information about limits on the number of inline policies that you can embed with a role, see [Limitations on IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/LimitationsOnEntities.html) in the *IAM User Guide*\.  
If an external policy \(such as `AWS::IAM::Policy` or `AWS::IAM::ManagedPolicy`\) has a `Ref` to a role and if a resource \(such as `AWS::ECS::Service`\) also has a `Ref` to the same role, add a `DependsOn` attribute to the resource to make the resource depend on the external policy\. This dependency ensures that the role's policy is available throughout the resource's lifecycle\. For example, when you delete a stack with an `AWS::ECS::Service` resource, the `DependsOn` attribute ensures that AWS CloudFormation deletes the `AWS::ECS::Service` resource before deleting its role's policy\.
*Required*: No  
*Type*: List of [Policy](aws-properties-iam-policy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleName`  <a name="cfn-iam-role-rolename"></a>
A name for the IAM role\. For valid values, see the `RoleName` parameter for the [ `CreateRole` ](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateRole.html) action in the *IAM User Guide*\.  
This parameter allows \(per its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-\. The role name must be unique within the account\. Role names are not distinguished by case\. For example, you cannot create roles named both "Role1" and "role1"\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the role name\.  
If you specify a name, you must specify the `CAPABILITY_NAMED_IAM` value to acknowledge your template's capabilities\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities)\.  
Naming an IAM resource can cause an unrecoverable error if you reuse the same template in multiple Regions\. To prevent this, we recommend using `Fn::Join` and `AWS::Region` to create a Region\-specific name, as in the following example: `{"Fn::Join": ["", [{"Ref": "AWS::Region"}, {"Ref": "MyResourceName"}]]}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iam-role-tags"></a>
A list of tags that are attached to the specified role\. For more information about tagging, see [Tagging IAM Identities](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html) in the *IAM User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iam-role-return-values"></a>

### Ref<a name="aws-resource-iam-role-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For example:

 `{ "Ref": "RootRole" }` 

For the `AWS::IAM::Role` resource with the logical ID `RootRole`, `Ref` will return the role name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iam-role-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iam-role-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the role\. For example:  
 `{"Fn::GetAtt" : ["MyRole", "Arn"] }`   
This will return a value such as `arn:aws:iam::1234567890:role/MyRole-AJJHDSKSDF`\.

`RoleId`  <a name="RoleId-fn::getatt"></a>
Returns the stable and unique string identifying the role\. For example, `AIDAJQABLZS4A3QDU576Q`\.  
For more information about IDs, see [IAM Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_identifiers.html) in the *IAM User Guide*\.

## Examples<a name="aws-resource-iam-role--examples"></a>



### IAM Role with Embedded Policy and Instance Profiles<a name="aws-resource-iam-role--examples--IAM_Role_with_Embedded_Policy_and_Instance_Profiles"></a>

This example shows an embedded policy in the `AWS::IAM::Role`\. The policy is specified inline in the `Policies` property of the `AWS::IAM::Role`\.

#### <a name="aws-resource-iam-role--examples--IAM_Role_with_Embedded_Policy_and_Instance_Profiles--language_sc3_fgs_qjb"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "RootRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "ec2.amazonaws.com"
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "Path": "/",
                "Policies": [
                    {
                        "PolicyName": "root",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": "*",
                                    "Resource": "*"
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "RootInstanceProfile": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "Path": "/",
                "Roles": [
                    {
                        "Ref": "RootRole"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iam-role--examples--IAM_Role_with_Embedded_Policy_and_Instance_Profiles--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  RootRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
              - ec2.amazonaws.com
            Action:
              - 'sts:AssumeRole'
      Path: /
      Policies:
        - PolicyName: root
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action: '*'
                Resource: '*'
  RootInstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      Path: /
      Roles:
        - !Ref RootRole
```

### IAM Role with External Policy and Instance Profiles<a name="aws-resource-iam-role--examples--IAM_Role_with_External_Policy_and_Instance_Profiles"></a>

In this example, the Policy and InstanceProfile resources are specified externally to the IAM Role\. They refer to the role by specifying its name, "RootRole", in their respective `Roles` properties\.

#### JSON<a name="aws-resource-iam-role--examples--IAM_Role_with_External_Policy_and_Instance_Profiles--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "RootRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Principal": {
                     "Service": [ "ec2.amazonaws.com" ]
                  },
                  "Action": [ "sts:AssumeRole" ]
               } ]
            },
            "Path": "/"
         }
      },
      "RolePolicies": {
         "Type": "AWS::IAM::Policy",
         "Properties": {
            "PolicyName": "root",
            "PolicyDocument": {
               "Version" : "2012-10-17",
               "Statement": [ {
                  "Effect": "Allow",
                  "Action": "*",
                  "Resource": "*"
               } ]
            },
            "Roles": [ {
               "Ref": "RootRole"
            } ]
         }
      },
      "RootInstanceProfile": {
         "Type": "AWS::IAM::InstanceProfile",
         "Properties": {
            "Path": "/",
            "Roles": [ {
               "Ref": "RootRole"
            } ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-iam-role--examples--IAM_Role_with_External_Policy_and_Instance_Profiles--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  RootRole: 
    Type: "AWS::IAM::Role"
    Properties: 
      AssumeRolePolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Principal: 
              Service: 
                - "ec2.amazonaws.com"
            Action: 
              - "sts:AssumeRole"
      Path: "/"
  RolePolicies: 
    Type: "AWS::IAM::Policy"
    Properties: 
      PolicyName: "root"
      PolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Action: "*"
            Resource: "*"
      Roles: 
        - 
          Ref: "RootRole"
  RootInstanceProfile: 
    Type: "AWS::IAM::InstanceProfile"
    Properties: 
      Path: "/"
      Roles: 
        - 
          Ref: "RootRole"
```

## See also<a name="aws-resource-iam-role--seealso"></a>
+  [CreateRole](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateRole.html) in the *AWS Identity and Access Management API Reference* 
+  [AWS Identity and Access Management Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-iam.html) 
+  [AWS::IAM::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html) 

