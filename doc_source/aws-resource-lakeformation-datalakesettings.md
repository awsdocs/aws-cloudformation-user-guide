# AWS::LakeFormation::DataLakeSettings<a name="aws-resource-lakeformation-datalakesettings"></a>

The `AWS::LakeFormation::DataLakeSettings` resource is an AWS Lake Formation resource type that manages the data lake settings for your account\. Note that the CloudFormation template only supports updating the `Admins` list\. It does not support updating the [CreateDatabaseDefaultPermissions](https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-settings.html#aws-lake-formation-api-aws-lake-formation-api-settings-DataLakeSettings) or [CreateTableDefaultPermissions](https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-settings.html#aws-lake-formation-api-aws-lake-formation-api-settings-DataLakeSettings)\. Those permissions can only be edited in the DataLakeSettings resource via the API\.

## Syntax<a name="aws-resource-lakeformation-datalakesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datalakesettings-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::DataLakeSettings",
  "Properties" : {
        [
             "[Admins](#cfn-lakeformation-datalakesettings-admins)" : [Admins](aws-properties-lakeformation-datalakesettings-admins.md)
        ]
    }
}
```

### YAML<a name="aws-resource-lakeformation-datalakesettings-syntax.yaml"></a>

```
Type: AWS::LakeFormation::DataLakeSettings
Properties: 
  [Admins](#cfn-lakeformation-datalakesettings-admins): 
    - [Admins](aws-properties-lakeformation-datalakesettings-admins.md)
```

## Properties<a name="aws-resource-lakeformation-datalakesettings-properties"></a>

`Admins`  <a name="cfn-lakeformation-datalakesettings-admins"></a>
A list of AWS Lake Formation principals\.  
*Required*: No  
*Type*: [Admins](aws-properties-lakeformation-datalakesettings-admins.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-lakeformation-datalakesettings-return-values"></a>

### Ref<a name="aws-resource-lakeformation-datalakesettings-return-values-ref"></a>

### Example<a name="aws-resource-lakeformation-datalakesettings--examples--Example"></a>

The following example creates an Administrator user for Lake Formation and adds the user as an Administrator to Lake Formation\.

#### JSON<a name="aws-resource-lakeformation-datalakesettings--examples--Example--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters": {
    "LakeFormationAdministratorUsername": {
      "Description": "Username for AWS administrator",
      "Type": "String",
      "Default": "LakeFormationAdmin"
    }
  },
  "Resources": {
    "LakeFormationAdministratorPassword": {
      "Type": "AWS::SecretsManager::Secret",
      "Properties": {
        "Description": "Password for Lake Formation administrator",
        "GenerateSecretString": {
          "SecretStringTemplate": [
            "",
            [
              "{\"username\": \"",
              "LakeFormationAdministratorUsername",
              "\"}"
            ]
          ],
          "PasswordLength": 16,
          "GenerateStringKey": "password"
        },
        "Name": "LakeFormationAdministratorsPassword",
        "Tags": [
          {
            "Key": "ProjectName",
            "Value": "LakeFormationSetup"
          }
        ]
      }
    },
    "LakeFormationSAdministratorUser": {
      "Type": "AWS::IAM::User",
      "Properties": {
        "LoginProfile": {
          "Password": [
            "",
            [
              "{{resolve:secretsmanager:",
              "LakeFormationAdministratorPassword",
              ":SecretString:password}}"
            ]
          ],
          "PasswordResetRequired": false
        },
        "ManagedPolicyArns": [
          "arn:aws:iam::aws:policy/AWSGlueConsoleFullAccess",
          "arn:aws:iam::aws:policy/AmazonAthenaFullAccess"
        ],
        "Policies": [
          {
            "PolicyName": "LakeFormationAdministratorAccess",
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": [
                    "lakeformation:*",
                    "cloudtrail:DescribeTrails",
                    "cloudtrail:LookupEvents",
                    "iam:PutRolePolicy",
                    "iam:CreateServiceLinkedRole"
                  ],
                  "Resource": "*"
                },
                {
                  "Effect": "Deny",
                  "Action": [
                    "lakeformation:PutDataLakeSettings"
                  ],
                  "Resource": "*"
                }
              ]
            }
          },
          {
            "PolicyName": "LakeFormationPassRole",
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Sid": "PassRolePermissions",
                  "Effect": "Allow",
                  "Action": [
                    "iam:PassRole"
                  ],
                  "Resource": [
                    [
                      "",
                      [
                        "arn:aws:iam::",
                        "AWS::AccountId",
                        ":role/",
                        "LakeFormationWorkflowRole"
                      ]
                    ]
                  ]
                }
              ]
            }
          }
        ],
        "UserName": "LakeFormationAdministratorUsername"
      }
    },
    "LakeFormationWorkflowRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "glue.amazonaws.com"
                ]
              },
              "Action": [
                "sts:AssumeRole"
              ]
            }
          ]
        },
        "Path": "/"
      }
    },
    "LakeFormationDataAccessRole": {
      "Type": "AWS::IAM::Policy",
      "Properties": {
        "PolicyName": "LakeFormationDataAccessRole",
        "PolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "Lakeformation",
              "Effect": "Allow",
              "Action": [
                "lakeformation:GetDataAccess",
                "lakeformation:GrantPermissions"
              ],
              "Resource": "*"
            }
          ]
        },
        "Roles": [
          "LakeFormationWorkflowRole"
        ]
      }
    },
    "LakeFormationPassRole": {
      "Type": "AWS::IAM::Policy",
      "Properties": {
        "PolicyName": "LakeFormationPassRole",
        "PolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "PassRolePermissions",
              "Effect": "Allow",
              "Action": [
                "iam:PassRole"
              ],
              "Resource": [
                [
                  "",
                  [
                    "arn:aws:iam::",
                    "AWS::AccountId",
                    ":role/",
                    "LakeFormationWorkflowRole"
                  ]
                ]
              ]
            }
          ]
        },
        "Roles": [
          "LakeFormationWorkflowRole"
        ]
      }
    },
    "LakeFormationAdminSetup": {
      "Type": "AWS::LakeFormation::DataLakeSettings",
      "Properties": {
        "Admins": [
          {
            "DataLakePrincipalIdentifier": "LakeFormationSAdministratorUser.Arn"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-lakeformation-datalakesettings--examples--Example--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
  
Parameters:
  LakeFormationAdministratorUsername:
    Description: Username for AWS administrator
    Type: String
    Default: LakeFormationAdmin

Resources:
  LakeFormationAdministratorPassword:
    Type: AWS::SecretsManager::Secret
    Properties:
      Description: Password for Lake Formation administrator
      GenerateSecretString:
        SecretStringTemplate: !Join ['', ['{"username": "', !Ref LakeFormationAdministratorUsername, '"}' ]]
        PasswordLength: 16
        GenerateStringKey: "password"
      Name: LakeFormationAdministratorsPassword
      Tags:
        - Key: ProjectName
          Value: LakeFormationSetup

  LakeFormationSAdministratorUser:
    Type: AWS::IAM::User
    Properties:
      LoginProfile:
        Password: !Join ['', ['{{resolve:secretsmanager:', !Ref LakeFormationAdministratorPassword, ':SecretString:password}}' ]]
        PasswordResetRequired: No
      ManagedPolicyArns:
        - arn:aws:iam::aws:policy/AWSGlueConsoleFullAccess
        - arn:aws:iam::aws:policy/AmazonAthenaFullAccess
      Policies:
        -
          PolicyName: "LakeFormationAdministratorAccess"
          PolicyDocument:
            Version: '2012-10-17'
            Statement:
            - Effect: Allow
              Action:
              - lakeformation:*
              - cloudtrail:DescribeTrails
              - cloudtrail:LookupEvents
              - iam:PutRolePolicy
              - iam:CreateServiceLinkedRole
              Resource: "*"
            - Effect: Deny
              Action:
              - lakeformation:PutDataLakeSettings
              Resource: "*"
        -
          PolicyName: "LakeFormationPassRole"
          PolicyDocument:
            Version: '2012-10-17'
            Statement:
            - Sid: PassRolePermissions
              Effect: Allow
              Action:
              - iam:PassRole
              Resource:
              - !Join ['', ['arn:aws:iam::', !Ref "AWS::AccountId", ':role/', !Ref LakeFormationWorkflowRole ]]
      UserName: !Ref LakeFormationAdministratorUsername

  LakeFormationWorkflowRole: 
    Type: "AWS::IAM::Role"
    Properties: 
      AssumeRolePolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Principal: 
              Service: 
                - "glue.amazonaws.com"
            Action: 
              - "sts:AssumeRole"
      Path: "/"

  LakeFormationDataAccessRole: 
    Type: "AWS::IAM::Policy"
    Properties: 
      PolicyName: "LakeFormationDataAccessRole"
      PolicyDocument: 
        Version: '2012-10-17'
        Statement:
        - Sid: Lakeformation
          Effect: Allow
          Action:
          - lakeformation:GetDataAccess
          - lakeformation:GrantPermissions
          Resource: "*"
      Roles: 
        - !Ref LakeFormationWorkflowRole

  LakeFormationPassRole:
    Type: "AWS::IAM::Policy"
    Properties:
      PolicyName: "LakeFormationPassRole"
      PolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Sid: PassRolePermissions
          Effect: Allow
          Action:
          - iam:PassRole
          Resource:
          - !Join ['', ['arn:aws:iam::', !Ref "AWS::AccountId", ':role/', !Ref LakeFormationWorkflowRole ]]
      Roles:
        - !Ref LakeFormationWorkflowRole

  LakeFormationAdminSetup:
    Type: AWS::LakeFormation::DataLakeSettings
    Properties: 
      Admins:
        - DataLakePrincipalIdentifier: !GetAtt LakeFormationSAdministratorUser.Arn
```
