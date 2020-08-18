# AWS::CodeBuild::SourceCredential<a name="aws-resource-codebuild-sourcecredential"></a>

 Information about the credentials for a GitHub, GitHub Enterprise, or Bitbucket repository\. We strongly recommend that you use AWS Secrets Manager to store your credentials\. If you use Secrets Manager, you must have secrets in your secrets manager\. For more information, see [ Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager)\. 

**Important**  
 For security purposes, do not use plain text in your CloudFormation template to store your credentials\. 

## Syntax<a name="aws-resource-codebuild-sourcecredential-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codebuild-sourcecredential-syntax.json"></a>

```
{
  "Type" : "AWS::CodeBuild::SourceCredential",
  "Properties" : {
      "[AuthType](#cfn-codebuild-sourcecredential-authtype)" : String,
      "[ServerType](#cfn-codebuild-sourcecredential-servertype)" : String,
      "[Token](#cfn-codebuild-sourcecredential-token)" : String,
      "[Username](#cfn-codebuild-sourcecredential-username)" : String
    }
}
```

### YAML<a name="aws-resource-codebuild-sourcecredential-syntax.yaml"></a>

```
Type: AWS::CodeBuild::SourceCredential
Properties: 
  [AuthType](#cfn-codebuild-sourcecredential-authtype): String
  [ServerType](#cfn-codebuild-sourcecredential-servertype): String
  [Token](#cfn-codebuild-sourcecredential-token): String
  [Username](#cfn-codebuild-sourcecredential-username): String
```

## Properties<a name="aws-resource-codebuild-sourcecredential-properties"></a>

`AuthType`  <a name="cfn-codebuild-sourcecredential-authtype"></a>
 The type of authentication used by the credentials\. Valid options are OAUTH, BASIC\_AUTH, or PERSONAL\_ACCESS\_TOKEN\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `BASIC_AUTH | OAUTH | PERSONAL_ACCESS_TOKEN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerType`  <a name="cfn-codebuild-sourcecredential-servertype"></a>
 The type of source provider\. The valid options are GITHUB, GITHUB\_ENTERPRISE, or BITBUCKET\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `BITBUCKET | GITHUB | GITHUB_ENTERPRISE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Token`  <a name="cfn-codebuild-sourcecredential-token"></a>
 For GitHub or GitHub Enterprise, this is the personal access token\. For Bitbucket, this is the app password\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-codebuild-sourcecredential-username"></a>
 The Bitbucket username when the `authType` is BASIC\_AUTH\. This parameter is not valid for other types of source providers or connections\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-codebuild-sourcecredential--examples"></a>

### Create Bitbucket source credentials using AWS Secrets Manager<a name="aws-resource-codebuild-sourcecredential--examples--Create_Bitbucket_source_credentials_using_AWS_Secrets_Manager"></a>

#### YAML<a name="aws-resource-codebuild-sourcecredential--examples--Create_Bitbucket_source_credentials_using_AWS_Secrets_Manager--yaml"></a>

```
CodeBuildSourceCredential:
  Type: 'AWS::CodeBuild::SourceCredential'
  Properties:
    Token: '{{resolve:secretsmanager:bitbucket:SecretString:token}}'
    ServerType: BITBUCKET
    Username: '{{resolve:secretsmanager:bitbucket:SecretString:username}}'
    AuthType: BASIC_AUTH
```

#### JSON<a name="aws-resource-codebuild-sourcecredential--examples--Create_Bitbucket_source_credentials_using_AWS_Secrets_Manager--json"></a>

```
{
   "CodeBuildSourceCredential": {
      "Type": "AWS::CodeBuild::SourceCredential",
      "Properties": {
         "Token": "{{resolve:secretsmanager:bitbucket:SecretString:token}}",
         "ServerType": "BITBUCKET",
         "Username": "{{resolve:secretsmanager:bitbucket:SecretString:username}}",
         "AuthType": "BASIC_AUTH"
      }
   }
}
```

### Create GitHub Enterprise source credentials using AWS Secrets Manager<a name="aws-resource-codebuild-sourcecredential--examples--Create_GitHub_Enterprise_source_credentials_using_AWS_Secrets_Manager"></a>

#### YAML<a name="aws-resource-codebuild-sourcecredential--examples--Create_GitHub_Enterprise_source_credentials_using_AWS_Secrets_Manager--yaml"></a>

```
Resources:
  CodeBuildSourceCredential:
    Type: 'AWS::CodeBuild::SourceCredential'
    Properties:
      Token: '{{resolve:secretsmanager:github_enterprise:SecretString:token}}'
      ServerType: GITHUB_ENTERPRISE
      AuthType: PERSONAL_ACCESS_TOKEN
```

#### JSON<a name="aws-resource-codebuild-sourcecredential--examples--Create_GitHub_Enterprise_source_credentials_using_AWS_Secrets_Manager--json"></a>

```
{
   "Resources": {
      "CodeBuildSourceCredential": {
         "Type": "AWS::CodeBuild::SourceCredential",
         "Properties": {
            "Token": "{{resolve:secretsmanager:github_enterprise:SecretString:token}}",
            "ServerType": "GITHUB_ENTERPRISE",
            "AuthType": "PERSONAL_ACCESS_TOKEN"
         }
      }
   }
}
```

### Create GitHub source credentials using AWS Secrets Manager<a name="aws-resource-codebuild-sourcecredential--examples--Create_GitHub_source_credentials_using_AWS_Secrets_Manager"></a>

#### YAML<a name="aws-resource-codebuild-sourcecredential--examples--Create_GitHub_source_credentials_using_AWS_Secrets_Manager--yaml"></a>

```
Resources:
  CodeBuildSourceCredential:
    Type: 'AWS::CodeBuild::SourceCredential'
    Properties:
      Token: '{{resolve:secretsmanager:github:SecretString:token}}'
      ServerType: GITHUB
      AuthType: PERSONAL_ACCESS_TOKEN
```

#### JSON<a name="aws-resource-codebuild-sourcecredential--examples--Create_GitHub_source_credentials_using_AWS_Secrets_Manager--json"></a>

```
{
   "Resources": {
      "CodeBuildSourceCredential": {
         "Type": "AWS::CodeBuild::SourceCredential",
         "Properties": {
            "Token": "{{resolve:secretsmanager:github:SecretString:token}}",
            "ServerType": "GITHUB",
            "AuthType": "PERSONAL_ACCESS_TOKEN"
         }
      }
   }
}
```

### Import source credentials for Bitbucket<a name="aws-resource-codebuild-sourcecredential--examples--Import_source_credentials_for_Bitbucket"></a>

#### YAML<a name="aws-resource-codebuild-sourcecredential--examples--Import_source_credentials_for_Bitbucket--yaml"></a>

```
Resources:
  MySourceCreds:
    Type: 'AWS::CodeBuild::SourceCredential'
    Properties:
      Token: '{{resolve:secretsmanager:bitbucket:SecretString:token}}'
      ServerType: BITBUCKET
      Username: '{{resolve:secretsmanager:bitbucket:SecretString:username}}'
      AuthType: BASIC_AUTH
  MyProject:
    Type: 'AWS::CodeBuild::Project'
    Properties:
      Name: myProjectName
      Description: A description about my project
      ServiceRole: testServiceRoleArn
      Artifacts:
        Type: NO_ARTIFACTS
      Environment:
        Type: LINUX_CONTAINER
        ComputeType: BUILD_GENERAL1_SMALL
        Image: 'aws/codebuild/standard:2.0'
      Source:
        Type: BITBUCKET
        Location: 'your-bitbucket-repo-url'
    DependsOn: MySourceCreds
```

#### JSON<a name="aws-resource-codebuild-sourcecredential--examples--Import_source_credentials_for_Bitbucket--json"></a>

```
{
    "Resources": {
        "MySourceCreds": {
            "Type": "AWS::CodeBuild::SourceCredential",
            "Properties": {
                "Token": "{{resolve:secretsmanager:bitbucket:SecretString:token}}",
                "ServerType": "BITBUCKET",
                "Username": "{{resolve:secretsmanager:bitbucket:SecretString:username}}",
                "AuthType": "BASIC_AUTH"
            }
        },
        "MyProject": {
            "Type": "AWS::CodeBuild::Project",
            "Properties": {
                "Name": "myProjectName",
                "Description": "A description about my project",
                "ServiceRole": "testServiceRoleAr",
                "Artifacts": {
                    "Type": "NO_ARTIFACTS"
                },
                "Environment": {
                    "Type": "LINUX_CONTAINER",
                    "ComputeType": "BUILD_GENERAL1_SMALL",
                    "Image": "aws/codebuild/standard:2.0"
                },
                "Source": {
                    "Type": "BITBUCKET",
                    "Location": "your-bitbucket-repo-url"
                }
            },
            "DependsOn": "MySourceCreds"
        }
    }
}
```

### Import source credentials for Github<a name="aws-resource-codebuild-sourcecredential--examples--Import_source_credentials_for_Github"></a>

#### YAML<a name="aws-resource-codebuild-sourcecredential--examples--Import_source_credentials_for_Github--yaml"></a>

```
Resources:
  MySourceCreds:
    Type: 'AWS::CodeBuild::SourceCredential'
    Properties: 
      Token: '{{resolve:secretsmanager:github:SecretString:token}}'
      ServerType: GITHUB
      AuthType: PERSONAL_ACCESS_TOKEN
  MyProject:
    Type: 'AWS::CodeBuild::Project'
    Properties: 
      Name: myProjectName
      Description: A description about my project
      ServiceRole: testServiceRoleArn
      Artifacts:
        Type: NO_ARTIFACTS
      Environment:
        Type: LINUX_CONTAINER
        ComputeType: BUILD_GENERAL1_SMALL
        Image: 'aws/codebuild/standard:2.0'
      Source:
        Type: GITHUB
        Location: 'your-github-repo-url'
    DependsOn: MySourceCreds
```

#### JSON<a name="aws-resource-codebuild-sourcecredential--examples--Import_source_credentials_for_Github--json"></a>

```
{
    "Resources": {
        "MySourceCreds": {
            "Type": "AWS::CodeBuild::SourceCredential",
            "Properties": {
                "Token": "{{resolve:secretsmanager:github:SecretString:token}}",
                "ServerType": "GITHUB",
                "AuthType": "PERSONAL_ACCESS_TOKEN"
            }
        },
        "MyProject": {
            "Type": "AWS::CodeBuild::Project",
            "Properties": {
                "Name": "myProjectName",
                "Description": "A description about my project",
                "ServiceRole": "testServiceRoleArn",
                "Artifacts": {
                    "Type": "NO_ARTIFACTS"
                },
                "Environment": {
                    "Type": "LINUX_CONTAINER",
                    "ComputeType": "BUILD_GENERAL1_SMALL",
                    "Image": "aws/codebuild/standard:2.0"
                },
                "Source": {
                    "Type": "GITHUB",
                    "Location": "your-github-repo-url"
                }
            },
            "DependsOn": "MySourceCreds"
        }
    }
}
```