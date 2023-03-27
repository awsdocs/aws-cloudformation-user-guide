# AWS::Grafana::Workspace<a name="aws-resource-grafana-workspace"></a>

Specifies a *workspace*\. In a workspace, you can create Grafana dashboards and visualizations to analyze your metrics, logs, and traces\. You don't have to build, package, or deploy any hardware to run the Grafana server\.

## Syntax<a name="aws-resource-grafana-workspace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-grafana-workspace-syntax.json"></a>

```
{
  "Type" : "AWS::Grafana::Workspace",
  "Properties" : {
      "[AccountAccessType](#cfn-grafana-workspace-accountaccesstype)" : String,
      "[AuthenticationProviders](#cfn-grafana-workspace-authenticationproviders)" : [ String, ... ],
      "[ClientToken](#cfn-grafana-workspace-clienttoken)" : String,
      "[DataSources](#cfn-grafana-workspace-datasources)" : [ String, ... ],
      "[Description](#cfn-grafana-workspace-description)" : String,
      "[Name](#cfn-grafana-workspace-name)" : String,
      "[NotificationDestinations](#cfn-grafana-workspace-notificationdestinations)" : [ String, ... ],
      "[OrganizationalUnits](#cfn-grafana-workspace-organizationalunits)" : [ String, ... ],
      "[OrganizationRoleName](#cfn-grafana-workspace-organizationrolename)" : String,
      "[PermissionType](#cfn-grafana-workspace-permissiontype)" : String,
      "[RoleArn](#cfn-grafana-workspace-rolearn)" : String,
      "[SamlConfiguration](#cfn-grafana-workspace-samlconfiguration)" : SamlConfiguration,
      "[StackSetName](#cfn-grafana-workspace-stacksetname)" : String,
      "[VpcConfiguration](#cfn-grafana-workspace-vpcconfiguration)" : VpcConfiguration
    }
}
```

### YAML<a name="aws-resource-grafana-workspace-syntax.yaml"></a>

```
Type: AWS::Grafana::Workspace
Properties: 
  [AccountAccessType](#cfn-grafana-workspace-accountaccesstype): String
  [AuthenticationProviders](#cfn-grafana-workspace-authenticationproviders): 
    - String
  [ClientToken](#cfn-grafana-workspace-clienttoken): String
  [DataSources](#cfn-grafana-workspace-datasources): 
    - String
  [Description](#cfn-grafana-workspace-description): String
  [Name](#cfn-grafana-workspace-name): String
  [NotificationDestinations](#cfn-grafana-workspace-notificationdestinations): 
    - String
  [OrganizationalUnits](#cfn-grafana-workspace-organizationalunits): 
    - String
  [OrganizationRoleName](#cfn-grafana-workspace-organizationrolename): String
  [PermissionType](#cfn-grafana-workspace-permissiontype): String
  [RoleArn](#cfn-grafana-workspace-rolearn): String
  [SamlConfiguration](#cfn-grafana-workspace-samlconfiguration): 
    SamlConfiguration
  [StackSetName](#cfn-grafana-workspace-stacksetname): String
  [VpcConfiguration](#cfn-grafana-workspace-vpcconfiguration): 
    VpcConfiguration
```

## Properties<a name="aws-resource-grafana-workspace-properties"></a>

`AccountAccessType`  <a name="cfn-grafana-workspace-accountaccesstype"></a>
Specifies whether the workspace can access AWS resources in this AWS account only, or whether it can also access AWS resources in other accounts in the same organization\. If this is `ORGANIZATION`, the `workspaceOrganizationalUnits` parameter specifies which organizational units the workspace can access\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CURRENT_ACCOUNT | ORGANIZATION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthenticationProviders`  <a name="cfn-grafana-workspace-authenticationproviders"></a>
Specifies whether this workspace uses SAML 2\.0, AWS IAM Identity Center \(successor to AWS Single Sign\-On\), or both to authenticate users for using the Grafana console within a workspace\. For more information, see [User authentication in Amazon Managed Grafana](https://docs.aws.amazon.com/grafana/latest/userguide/authentication-in-AMG.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientToken`  <a name="cfn-grafana-workspace-clienttoken"></a>
A unique, case\-sensitive, user\-provided identifier to ensure the idempotency of the request\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[!-~]{1,64}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSources`  <a name="cfn-grafana-workspace-datasources"></a>
Specifies the AWS data sources that have been configured to have IAM roles and permissions created to allow Amazon Managed Grafana to read data from these sources\.  
This list is only used when the workspace was created through the AWS console, and the `permissionType` is `SERVICE_MANAGED`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-grafana-workspace-description"></a>
The user\-defined description of the workspace\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-grafana-workspace-name"></a>
The name of the workspace\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9-._~]{1,255}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationDestinations`  <a name="cfn-grafana-workspace-notificationdestinations"></a>
The AWS notification channels that Amazon Managed Grafana can automatically create IAM roles and permissions for, to allow Amazon Managed Grafana to use these channels\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationalUnits`  <a name="cfn-grafana-workspace-organizationalunits"></a>
Specifies the organizational units that this workspace is allowed to use data sources from, if this workspace is in an account that is part of an organization\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationRoleName`  <a name="cfn-grafana-workspace-organizationrolename"></a>
The name of the IAM role that is used to access resources through Organizations\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PermissionType`  <a name="cfn-grafana-workspace-permissiontype"></a>
If this is `SERVICE_MANAGED`, and the workplace was created through the Amazon Managed Grafana console, then Amazon Managed Grafana automatically creates the IAM roles and provisions the permissions that the workspace needs to use AWS data sources and notification channels\.  
If this is `CUSTOMER_MANAGED`, you must manage those roles and permissions yourself\.  
If you are working with a workspace in a member account of an organization and that account is not a delegated administrator account, and you want the workspace to access data sources in other AWS accounts in the organization, this parameter must be set to `CUSTOMER_MANAGED`\.  
For more information about converting between customer and service managed, see [Managing permissions for data sources and notification channels](https://docs.aws.amazon.com/grafana/latest/userguide/AMG-datasource-and-notification.html)\. For more information about the roles and permissions that must be managed for customer managed workspaces, see [Amazon Managed Grafana permissions and policies for AWS data sources and notification channels](https://docs.aws.amazon.com/grafana/latest/userguide/AMG-manage-permissions.html)  
*Required*: No  
*Type*: String  
*Allowed values*: `CUSTOMER_MANAGED | SERVICE_MANAGED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-grafana-workspace-rolearn"></a>
The IAM role that grants permissions to the AWS resources that the workspace will view data from\. This role must already exist\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamlConfiguration`  <a name="cfn-grafana-workspace-samlconfiguration"></a>
If the workspace uses SAML, use this structure to map SAML assertion attributes to workspace user information and define which groups in the assertion attribute are to have the `Admin` and `Editor` roles in the workspace\.  
*Required*: No  
*Type*: [SamlConfiguration](aws-properties-grafana-workspace-samlconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetName`  <a name="cfn-grafana-workspace-stacksetname"></a>
The name of the AWS CloudFormation stack set that is used to generate IAM roles to be used for this workspace\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-grafana-workspace-vpcconfiguration"></a>
The configuration for connecting to data sources in a private VPC \(Amazon Virtual Private Cloud\)\.  
*Required*: No  
*Type*: [VpcConfiguration](aws-properties-grafana-workspace-vpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-grafana-workspace-return-values"></a>

### Ref<a name="aws-resource-grafana-workspace-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "Id" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-grafana-workspace-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-grafana-workspace-return-values-fn--getatt-fn--getatt"></a>

`CreationTimestamp`  <a name="CreationTimestamp-fn::getatt"></a>
The date that the workspace was created\.  
Type: Timestamp

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
The URL that users can use to access the Grafana console in the workspace\.  
Type: String

`GrafanaVersion`  <a name="GrafanaVersion-fn::getatt"></a>
The version of Grafana supported in this workspace\.  
Type: String

`Id`  <a name="Id-fn::getatt"></a>
The unique ID of this workspace\.  
Type: String

`ModificationTimestamp`  <a name="ModificationTimestamp-fn::getatt"></a>
The most recent date that the workspace was modified\.  
Type: Timestamp

`SamlConfigurationStatus`  <a name="SamlConfigurationStatus-fn::getatt"></a>
Specifies whether the workspace's SAML configuration is complete\.  
Valid values: `CONFIGURED | NOT_CONFIGURED`  
Type: String

`SsoClientId`  <a name="SsoClientId-fn::getatt"></a>
The ID of the IAM Identity Center\-managed application that is created by Amazon Managed Grafana\.  
Type: String

`Status`  <a name="Status-fn::getatt"></a>
The current status of the workspace\.  
Valid values: `ACTIVE | CREATING | DELETING | FAILED | UPDATING | UPGRADING | DELETION_FAILED | CREATION_FAILED | UPDATE_FAILED | UPGRADE_FAILED | LICENSE_REMOVAL_FAILED`  
Type: String

## Examples<a name="aws-resource-grafana-workspace--examples"></a>



### Create a workspace<a name="aws-resource-grafana-workspace--examples--Create_a_workspace"></a>

Create an Amazon Managed Grafana workspace using CloudFormation

#### JSON<a name="aws-resource-grafana-workspace--examples--Create_a_workspace--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Amazon Grafana workspace stack",
    "Resources": {
        "AmazonGrafanaWorkspaceIAMRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AmazonGrafanaAthenaAccess"],
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [{
                        "Effect": "Allow",
                        "Principal": {
                            "Service": [
                                "grafana.amazonaws.com"
                            ]
                        },
                        "Action": [
                            "sts:AssumeRole"
                        ]
                    }]
                }
            }
        },
        "AmazonGrafanaWorkspace": {
            "Type": "AWS::Grafana::Workspace",
            "Properties": {
                "AccountAccessType": "CURRENT_ACCOUNT",
                "Name": "AmazonGrafanaWorkspace",
                "Description": "Amazon Grafana Workspace",
                "AuthenticationProviders": ["SAML"],
                "PermissionType": "CUSTOMER_MANAGED",
                "RoleArn": {
                    "Fn::GetAtt": [
                        "AmazonGrafanaWorkspaceIAMRole",
                        "Arn"
                    ]
                },
                "SamlConfiguration": {
                    "IdpMetadata": {
                        "Xml": "<md:EntityDescriptor xmlns:md='urn:oasis:names:tc:SAML:2.0:metadata' entityID='entityId'>DATA</md:EntityDescriptor>"
                    },
                    "AssertionAttributes": {
                        "Name": "displayName",
                        "Login": "login",
                        "Email": "email",
                        "Groups": "group",
                        "Role": "role",
                        "Org": "org"
                    },
                    "RoleValues": {
                        "Editor": ["editor1"],
                        "Admin": ["admin1"]
                    },
                    "AllowedOrganizations": ["org1"],
                    "LoginValidityDuration": 60
                }
            }
        }
    },
    "Outputs": {
        "WorkspaceEndpoint": {
            "Value": {
                "Fn::GetAtt": [
                    "AmazonGrafanaWorkspace",
                    "Endpoint"
                ]
            }
        },
        "WorkspaceStatus": {
            "Value": {
                "Fn::GetAtt": [
                    "AmazonGrafanaWorkspace",
                    "Status"
                ]
            }
        },
        "WorkspaceId": {
            "Value": {
                "Ref": "AmazonGrafanaWorkspace"
            }
        },
        "GrafanaVersion": {
            "Value": {
                "Fn::GetAtt": [
                    "AmazonGrafanaWorkspace",
                    "GrafanaVersion"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-grafana-workspace--examples--Create_a_workspace--yaml"></a>

```
Description: Amazon Grafana workspace stack
Resources:
  AmazonGrafanaWorkspaceIAMRole:
    Type: 'AWS::IAM::Role'
    Properties:
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AmazonGrafanaAthenaAccess'
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - grafana.amazonaws.com
            Action:
              - 'sts:AssumeRole'

  AmazonGrafanaWorkspace:
    Type: 'AWS::Grafana::Workspace'
    Properties:
      AccountAccessType: CURRENT_ACCOUNT
      Name: AmazonGrafanaWorkspace
      Description: Amazon Grafana Workspace
      AuthenticationProviders:
        - SAML
      PermissionType: CUSTOMER_MANAGED
      RoleArn: !GetAtt 
        - AmazonGrafanaWorkspaceIAMRole
        - Arn
      SamlConfiguration:
        IdpMetadata:
          Xml: >-
            <md:EntityDescriptor xmlns:md='urn:oasis:names:tc:SAML:2.0:metadata'
            entityID='entityId'>DATA</md:EntityDescriptor>
        AssertionAttributes:
          Name: displayName
          Login: login
          Email: email
          Groups: group
          Role: role
          Org: org
        RoleValues:
          Editor:
            - editor1
          Admin:
            - admin1
        AllowedOrganizations:
          - org1
        LoginValidityDuration: 60

Outputs:
  WorkspaceEndpoint:
    Value: !GetAtt 
      - AmazonGrafanaWorkspace
      - Endpoint
  WorkspaceStatus:
    Value: !GetAtt 
      - AmazonGrafanaWorkspace
      - Status
  WorkspaceId:
    Value: !Ref AmazonGrafanaWorkspace
  GrafanaVersion:
    Value: !GetAtt 
      - AmazonGrafanaWorkspace
      - GrafanaVersion
```