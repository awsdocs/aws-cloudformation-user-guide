# AWS::SSM::Document<a name="aws-resource-ssm-document"></a>

The `AWS::SSM::Document` resource creates a Systems Manager \(SSM\) document in AWS Systems Manager\. This document defines the actions that Systems Manager performs on your AWS resources\.

**Note**  
This resource does not support CloudFormation drift detection\.

## Syntax<a name="aws-resource-ssm-document-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-document-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Document",
  "Properties" : {
      "[Attachments](#cfn-ssm-document-attachments)" : [ AttachmentsSource, ... ],
      "[Content](#cfn-ssm-document-content)" : Json,
      "[DocumentFormat](#cfn-ssm-document-documentformat)" : String,
      "[DocumentType](#cfn-ssm-document-documenttype)" : String,
      "[Name](#cfn-ssm-document-name)" : String,
      "[Requires](#cfn-ssm-document-requires)" : [ DocumentRequires, ... ],
      "[Tags](#cfn-ssm-document-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetType](#cfn-ssm-document-targettype)" : String,
      "[UpdateMethod](#cfn-ssm-document-updatemethod)" : String,
      "[VersionName](#cfn-ssm-document-versionname)" : String
    }
}
```

### YAML<a name="aws-resource-ssm-document-syntax.yaml"></a>

```
Type: AWS::SSM::Document
Properties: 
  [Attachments](#cfn-ssm-document-attachments): 
    - AttachmentsSource
  [Content](#cfn-ssm-document-content): Json
  [DocumentFormat](#cfn-ssm-document-documentformat): String
  [DocumentType](#cfn-ssm-document-documenttype): String
  [Name](#cfn-ssm-document-name): String
  [Requires](#cfn-ssm-document-requires): 
    - DocumentRequires
  [Tags](#cfn-ssm-document-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetType](#cfn-ssm-document-targettype): String
  [UpdateMethod](#cfn-ssm-document-updatemethod): String
  [VersionName](#cfn-ssm-document-versionname): String
```

## Properties<a name="aws-resource-ssm-document-properties"></a>

`Attachments`  <a name="cfn-ssm-document-attachments"></a>
A list of key\-value pairs that describe attachments to a version of a document\.  
*Required*: No  
*Type*: List of [AttachmentsSource](aws-properties-ssm-document-attachmentssource.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Content`  <a name="cfn-ssm-document-content"></a>
The content for the new SSM document in JSON or YAML\. For more information about the schemas for SSM document content, see [SSM document schema features and examples](https://docs.aws.amazon.com/systems-manager/latest/userguide/document-schemas-features.html) in the *AWS Systems Manager User Guide*\.  
This parameter also supports `String` data types\.
*Required*: Yes  
*Type*: Json  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentFormat`  <a name="cfn-ssm-document-documentformat"></a>
Specify the document format for the request\. JSON is the default format\.  
*Required*: No  
*Type*: String  
*Allowed values*: `JSON | TEXT | YAML`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentType`  <a name="cfn-ssm-document-documenttype"></a>
The type of document to create\.  
*Allowed Values*: `ApplicationConfigurationSchema` \| `Automation` \| `Automation.ChangeTemplate` \| `Command` \| `DeploymentStrategy` \| `Package` \| `Policy` \| `Session`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-ssm-document-name"></a>
A name for the SSM document\.  
You can't use the following strings as document name prefixes\. These are reserved by AWS for use as document name prefixes:  
+  `aws` 
+  `amazon` 
+  `amzn` 
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Requires`  <a name="cfn-ssm-document-requires"></a>
A list of SSM documents required by a document\. This parameter is used exclusively by AWS AppConfig\. When a user creates an AWS AppConfig configuration in an SSM document, the user must also specify a required document for validation purposes\. In this case, an `ApplicationConfiguration` document requires an `ApplicationConfigurationSchema` document for validation purposes\. For more information, see [What is AWS AppConfig?](https://docs.aws.amazon.com/appconfig/latest/userguide/what-is-appconfig.html) in the * AWS AppConfig User Guide*\.  
*Required*: No  
*Type*: List of [DocumentRequires](aws-properties-ssm-document-documentrequires.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssm-document-tags"></a>
AWS CloudFormation resource tags to apply to the document\. Use tags to help you identify and categorize resources\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetType`  <a name="cfn-ssm-document-targettype"></a>
Specify a target type to define the kinds of resources the document can run on\. For example, to run a document on EC2 instances, specify the following value: `/AWS::EC2::Instance`\. If you specify a value of '/' the document can run on all types of resources\. If you don't specify a value, the document can't run on any resources\. For a list of valid resource types, see [AWS resource and property types reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html) in the *AWS CloudFormation User Guide*\.   
*Required*: No  
*Type*: String  
*Maximum*: `200`  
*Pattern*: `^\/[\w\.\-\:\/]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateMethod`  <a name="cfn-ssm-document-updatemethod"></a>
If the document resource you specify in your template already exists, this parameter determines whether a new version of the existing document is created, or the existing document is replaced\. `Replace` is the default method\. If you specify `NewVersion` for the `UpdateMethod` parameter, and the `Name` of the document does not match an existing resource, a new document is created\. When you specify `NewVersion`, the default version of the document is changed to the newly created version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionName`  <a name="cfn-ssm-document-versionname"></a>
An optional field specifying the version of the artifact you are creating with the document\. For example, `Release12.1`\. This value is unique across all versions of a document, and can't be changed\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_\-.]{1,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ssm-document-return-values"></a>

### Ref<a name="aws-resource-ssm-document-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Systems Manager document name, such as `MyNewSSMDocument`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ssm-document--examples"></a>

### Create an Automation runbook that runs commands on an EC2 Linux instance<a name="aws-resource-ssm-document--examples--Create_an_Automation_runbook_that_runs_commands_on_an_EC2_Linux_instance"></a>

The following runbook runs the commands you specify on your target Amazon EC2 Linux instance\. You specify the commands parameter value when starting the runbook\.

#### YAML<a name="aws-resource-ssm-document--examples--Create_an_Automation_runbook_that_runs_commands_on_an_EC2_Linux_instance--yaml"></a>

```
document: 
    Type: AWS::SSM::Document
    Properties:
      Content:
        schemaVersion: '0.3'
        description: 'Run a script on Linux instances.'
        parameters:
          AutomationAssumeRole:
            type: String
            description: (Optional) The ARN of the role that allows Automation to perform the actions on your behalf.
            default: ''
          commands:
            type: String
            description: "(Required) The commands to run or the path to an existing script on the instance."
            default: 'echo Hello World'
          InstanceId:
            type: String
            description: "(Required) The instance ID you want to run commands on."
            default: ''
        mainSteps:
        - name: sayHello
          action: 'aws:runCommand'
          inputs:
            DocumentName: AWS-RunShellScript
            Parameters:
              InstanceIds:
              - '{{InstanceId}}'
              commands:
              - "{{ commands }}"
      DocumentFormat: YAML
      DocumentType: Automation
      Name: 'CFN_runbook_example'
```

#### JSON<a name="aws-resource-ssm-document--examples--Create_an_Automation_runbook_that_runs_commands_on_an_EC2_Linux_instance--json"></a>

```
"document": {
         "Type": "AWS::SSM::Document",
         "Properties": {
            "Content": {
               "schemaVersion": "0.3",
               "description": "Run a script on Linux instances.",
               "parameters": {
                  "AutomationAssumeRole": {
                     "type": "String",
                     "description": "(Optional) The ARN of the role that allows Automation to perform the actions on your behalf.",
                     "default": ""
                  },
                  "commands": {
                     "type": "String",
                     "description": "(Required) The commands to run or the path to an existing script on the instance.",
                     "default": "echo Hello World"
                  },
                  "InstanceId": {
                     "type": "String",
                     "description": "(Required) The instance ID you want to run commands on.",
                     "default": ""
                  }
               },
               "mainSteps": [
                  {
                     "name": "sayHello",
                     "action": "aws:runCommand",
                     "inputs": {
                        "DocumentName": "AWS-RunShellScript",
                        "Parameters": {
                           "InstanceIds": [
                              "{{InstanceId}}"
                           ],
                           "commands": [
                              "{{ commands }}"
                           ]
                        }
                     }
                  }
               ]
            },
            "DocumentType": "Automation",
            "Name": "CFN_runbook_example"
         }
      }
```

### Create a document that runs commands on an EC2 Linux instance<a name="aws-resource-ssm-document--examples--Create_a_document_that_runs_commands_on_an_EC2_Linux_instance"></a>

The following SSM document runs the commands you specify on your target Amazon EC2 Linux instance\. You specify the commands parameter value when you run the document using Run Command\.

#### YAML<a name="aws-resource-ssm-document--examples--Create_a_document_that_runs_commands_on_an_EC2_Linux_instance--yaml"></a>

```
document: 
  Type: AWS::SSM::Document
  Properties:
    Content:
      schemaVersion: '2.2'
      description: 'Run a script on Linux instances.'
      parameters:
        commands:
          type: String
          description: "(Required) The commands to run or the path to an existing script
        on the instance."
          default: 'echo Hello World'
      mainSteps:
      - action: aws:runShellScript
        name: runCommands
        inputs:
          timeoutSeconds: '60'
          runCommand:
          - "{{ commands }}"
    DocumentFormat: YAML
    DocumentType: Command
    Name: 'CFN_2.2_command_example'
```

#### JSON<a name="aws-resource-ssm-document--examples--Create_a_document_that_runs_commands_on_an_EC2_Linux_instance--json"></a>

```
"document": {
  "Type": "AWS::SSM::Document",
  "Properties": {
    "Content": {
      "schemaVersion": "2.2",
      "description": "Run a script on Linux instances.",
      "parameters": {
        "commands": {
          "type": "String",
          "description": "(Required) The commands to run or the path to an existing script on the instance.",
          "default": "echo Hello World"
        }
      },
      "mainSteps": [
        {
          "action": "aws:runShellScript",
          "name": "runCommands",
          "inputs": {
            "timeoutSeconds": "60",
            "runCommand": [
              "{{ commands }}"
            ]
          }
        }
      ]
    },
    "DocumentType": "Command",
    "Name": "CFN_2.2_command_ex"
  }
}
```

### Join a managed instance to a directory in AWS Directory Service<a name="aws-resource-ssm-document--examples--Join_a_managed_instance_to_a_directory_in_"></a>

The following SSM document joins instances to a directory in AWS Directory Service\. The three runtime configuration parameters specify which directory the instance joins\. You specify these parameter values when you associate the document with an instance\.

#### YAML<a name="aws-resource-ssm-document--examples--Join_a_managed_instance_to_a_directory_in_--yaml"></a>

```
document: 
  Type: AWS::SSM::Document
  Properties:
    Content:
      schemaVersion: '1.2'
      description: Join instances to an AWS Directory Service domain.
      parameters:
        directoryId:
          type: String
          description: "(Required) The ID of the AWS Directory Service directory."
        directoryName:
          type: String
          description: "(Required) The name of the directory. For example, test.example.com"
        dnsIpAddresses:
          type: StringList
          default: []
          description: "(Optional) The IP addresses of the DNS servers in the directory.
            Required when DHCP is not configured. For more information, see https://docs.aws.amazon.com/directoryservice/latest/admin-guide/simple_ad_dns.html"
          allowedPattern: "((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)"
      runtimeConfig:
        aws:domainJoin:
          properties:
            directoryId: "{{ directoryId}}"
            directoryName: "{{ directoryName }}"
            dnsIpAddresses: "{{ dnsIpAddresses }}"
```

#### JSON<a name="aws-resource-ssm-document--examples--Join_a_managed_instance_to_a_directory_in_--json"></a>

```
"document" : {
    "Type": "AWS::SSM::Document",
    "Properties": {
        "Content": {
            "schemaVersion": "1.2",
            "description": "Join instances to an AWS Directory Service domain.",
            "parameters": {
                "directoryId": {
                    "type": "String",
                    "description": "(Required) The ID of the AWS Directory Service directory."
                },
                "directoryName": {
                    "type": "String",
                    "description": "(Required) The name of the directory. For example, test.example.com"
                },
                "dnsIpAddresses": {
                    "type": "StringList",
                    "default": [],
                    "description": "(Optional) The IP addresses of the DNS servers in the directory. Required when DHCP is not configured. For more information, see https://docs.aws.amazon.com/directoryservice/latest/admin-guide/simple_ad_dns.html",
                    "allowedPattern": "((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)"
                }
            },
            "runtimeConfig": {
                "aws:domainJoin": {
                    "properties": {
                        "directoryId": "{{ directoryId}}",
                        "directoryName": "{{ directoryName }}",
                        "dnsIpAddresses": "{{ dnsIpAddresses }}"
                    }
                }
            }
        }
    }
}
```

### Associate an SSM document with an instance<a name="aws-resource-ssm-document--examples--Associate_an_SSM_document_with_an_instance"></a>

The following example shows how to associate an SSM document with an instance\. The `DocumentName` property specifies the SSM document and the `AssociationParameters` property specifies values for the runtime configuration parameters\.

#### YAML<a name="aws-resource-ssm-document--examples--Associate_an_SSM_document_with_an_instance--yaml"></a>

```
myEC2:
  Type: AWS::EC2::Instance
  Properties:
    ImageId:
      Ref: myImageId
    InstanceType: t2.micro
    SsmAssociations:
    - DocumentName:
        Ref: document
      AssociationParameters:
      - Key: directoryId
        Value:
        - Ref: myDirectory
      - Key: directoryName
        Value:
        - testDirectory.example.com
      - Key: dnsIpAddresses
        Value:
          Fn::GetAtt:
          - myDirectory
          - DnsIpAddresses
    IamInstanceProfile:
      Ref: myInstanceProfile
    NetworkInterfaces:
    - DeviceIndex: '0'
      AssociatePublicIpAddress: 'true'
      SubnetId:
        Ref: mySubnet
    KeyName:
      Ref: myKeyName
```

#### JSON<a name="aws-resource-ssm-document--examples--Associate_an_SSM_document_with_an_instance--json"></a>

```
"myEC2" : {
    "Type": "AWS::EC2::Instance",
    "Properties": {
        "ImageId": {
            "Ref": "myImageId"
        },
        "InstanceType": "t2.micro",
        "SsmAssociations": [
            {
                "DocumentName": {
                    "Ref": "document"
                },
                "AssociationParameters": [
                    {
                        "Key": "directoryId",
                        "Value": [
                            {
                                "Ref": "myDirectory"
                            }
                        ]
                    },
                    {
                        "Key": "directoryName",
                        "Value": [
                            "testDirectory.example.com"
                        ]
                    },
                    {
                        "Key": "dnsIpAddresses",
                        "Value": {
                            "Fn::GetAtt": [
                                "myDirectory",
                                "DnsIpAddresses"
                            ]
                        }
                    }
                ]
            }
        ],
        "IamInstanceProfile": {
            "Ref": "myInstanceProfile"
        },
        "NetworkInterfaces": [
            {
                "DeviceIndex": "0",
                "AssociatePublicIpAddress": "true",
                "SubnetId": {
                    "Ref": "mySubnet"
                }
            }
        ],
        "KeyName": {
            "Ref": "myKeyName"
        }
    }
}
```

### Create a Systems Manager document for Session Manager preferences<a name="aws-resource-ssm-document--examples--Create_a__document_for_Session_Manager_preferences"></a>

The following example creates a Systems Manager `Session` type document for Session Manager preferences\. Before using this example template replace the placeholder values\.

#### JSON<a name="aws-resource-ssm-document--examples--Create_a__document_for_Session_Manager_preferences--json"></a>

```
{
   "Resources":{
      "SessionPreferencesDocument":{
         "Type":"AWS::SSM::Document",
         "Properties":{
            "Name":"SSM-SessionManagerRunShell",
            "Content":{
               "schemaVersion":"1.0",
               "description":"Document to hold regional settings for Session Manager",
               "sessionType":"Standard_Stream",
               "inputs":{
                  "s3BucketName":"DOC-EXAMPLE-BUCKET",
                  "s3KeyPrefix":"MyBucketPrefix",
                  "s3EncryptionEnabled":true,
                  "cloudWatchLogGroupName":"MyLogGroupName",
                  "cloudWatchEncryptionEnabled":true,
                  "cloudWatchStreamingEnabled":false,
                  "kmsKeyId":"MyKMSKeyID",
                  "runAsEnabled":false,
                  "runAsDefaultUser":"MyDefaultRunAsUser",
                  "idleSessionTimeout":"20",
                  "shellProfile":{
                     "windows":"example commands",
                     "linux":"example commands"
                  }
               }
            },
            "DocumentType":"Session"
         }
      }
   },
   "Outputs":{
      "DocumentName":{
         "Description":"Session Manager preferences document",
         "Value":"SSM-SessionManagerRunShell"
      }
   }
}
```

#### YAML<a name="aws-resource-ssm-document--examples--Create_a__document_for_Session_Manager_preferences--yaml"></a>

```
Resources:
  SessionPreferencesDocument:
    Type: AWS::SSM::Document
    Properties:
      Name: SSM-SessionManagerRunShell
      Content:
        schemaVersion: '1.0'
        description: Document to hold regional settings for Session Manager
        sessionType: Standard_Stream
        inputs:
          s3BucketName: 'DOC-EXAMPLE-BUCKET'
          s3KeyPrefix: 'MyBucketPrefix'
          s3EncryptionEnabled: true
          cloudWatchLogGroupName: 'MyLogGroupName'
          cloudWatchEncryptionEnabled: true
          cloudWatchStreamingEnabled: false
          kmsKeyId: 'MyKMSKeyID'
          runAsEnabled: false
          runAsDefaultUser: 'MyDefaultRunAsUser'
          idleSessionTimeout: '20'
          shellProfile:
            windows: example commands
            linux: example commands
      DocumentFormat: YAML
      DocumentType: Session
Outputs:
  DocumentName:
    Description: "Session Manager preferences document"
    Value: SSM-SessionManagerRunShell
```

### Create a Systems Manager document with JSON content<a name="aws-resource-ssm-document--examples--Create_a__document_with_JSON_content"></a>

The following example creates a new Systems Manager command document with JSON content\.

#### JSON<a name="aws-resource-ssm-document--examples--Create_a__document_with_JSON_content--json"></a>

```
{
   "Type":"AWS::SSM::Document",
   "Properties":{
      "Content":"{\"schemaVersion\": \"2.2\",  \"description\": \"Command Document Example JSON\nTemplate\",  \"parameters\": {    \"Message\": {      \"type\": \"String\", \"description\":\n\"Example\",      \"default\": \"Hello World\"    }  },  \"mainSteps\": [    { \"action\":\n\"aws:runPowerShellScript\",      \"name\": \"example\",      \"inputs\": {        \"runCommand\":\n[ \"Write-Output {{Message}}\" ]      }    }  ]}",
      "DocumentType":"Command",
      "DocumentFormat":"JSON"
   }
}
```

#### YAML<a name="aws-resource-ssm-document--examples--Create_a__document_with_JSON_content--yaml"></a>

```
--- 
Type: "AWS::SSM::Document"
Properties: 
  Content: "{\"schemaVersion\": \"2.2\",  \"description\": \"Command Document Example JSON Template\",  \"parameters\": {    \"Message\": {      \"type\": \"String\", \"description\": \"Example\",      \"default\": \"Hello World\"    }  },  \"mainSteps\": [    { \"action\": \"aws:runPowerShellScript\",      \"name\": \"example\",      \"inputs\": {        \"runCommand\": [ \"Write-Output {{Message}}\" ]      }    }  ]}"
  DocumentFormat: JSON
  DocumentType: Command
```

### Create a Systems Manager Distributor package<a name="aws-resource-ssm-document--examples--Create_a__Distributor_package"></a>

The following example creates a new Systems Manager Distributor package\.

#### JSON<a name="aws-resource-ssm-document--examples--Create_a__Distributor_package--json"></a>

```
{
        "Resources": {
        "ExamplePackageDocument": {
            "Type": "AWS::SSM::Document",
            "Properties": {
                "Content": "{\"files\": {\"NewPackage_WINDOWS.zip\": {\"checksums\": {\"sha256\": \"36aeb0ec2c706013cf8c68163459678f7f6daa9489cd3f91d52799331EXAMPLE\"}}}, \"publisher\": \"publisherName\", \"schemaVersion\": \"2.0\", \"packages\": {\"_any\": {\"_any\": {\"x86_64\": {\"file\": \"NewPackage_WINDOWS.zip\"}}}}, \"version\": \"1.0\"}",
                "DocumentType": "Package",
                "Attachments": [
                    {
                        "Key": "SourceUrl",
                        "Values": [
                            "s3://example-package-path/valid-package"
                        ]
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-document--examples--Create_a__Distributor_package--yaml"></a>

```
Resources:
  ExamplePackageDocument:
    Type: AWS::SSM::Document
    Properties:
      Content: '{\"files\": {\"NewPackage_WINDOWS.zip\": {\"checksums\":
        {\"sha256\": \"36aeb0ec2c706013cf8c68163459678f7f6daa9489cd3f91d52799331EXAMPLE\"}}},
        \"publisher\": \"publisherName\", \"schemaVersion\":
        \"2.0\", \"packages\": {\"_any\": {\"_any\": {\"x86_64\": {\"file\": \"NewPackage_WINDOWS.zip\"}}}},
        \"version\": \"1.0\"}'
      DocumentType: Package
      Attachments:
      - Key: SourceUrl
        Values:
        - "s3://example-package-path/valid-package"
```

### Create a Systems Manager Change Calendar document<a name="aws-resource-ssm-document--examples--Create_a__Change_Calendar_document"></a>

The following example creates a new Systems Manager Change Calendar document\.

#### JSON<a name="aws-resource-ssm-document--examples--Create_a__Change_Calendar_document--json"></a>

```
{
   "Resources":{
      "ExampleChangeCalendarDocument":{
         "Type":"AWS::SSM::Document",
         "Properties":{
            "Content":"BEGIN:VCALENDAR\r\nPRODID:-//AWS//Change Calendar 1.0//EN\r\nVERSION:2.0\r\nX-CALENDAR-TYPE:DEFAULT_OPEN\r\nX-WR-CALDESC:test\r\nBEGIN:VTODO\r\nDTSTAMP:20200320T004207Z\r\nUID:3b5af39a-d0b3-4049-a839-d7bb8af01f92\r\nSUMMARY:Add events to this calendar.\r\nEND:VTODO\r\nEND:VCALENDAR\r\n",
            "DocumentType":"ChangeCalendar",
            "DocumentFormat":"TEXT"
         }
      }
   }
}
```

#### YAML<a name="aws-resource-ssm-document--examples--Create_a__Change_Calendar_document--yaml"></a>

```
Resources:
  ExampleChangeCalendarDocument:
    Type: 'AWS::SSM::Document'
    Properties:
      Content: "BEGIN:VCALENDAR\r\nPRODID:-//AWS//Change Calendar 1.0//EN\r\nVERSION:2.0\r\nX-CALENDAR-TYPE:DEFAULT_OPEN\r\nX-WR-CALDESC:test\r\nBEGIN:VTODO\r\nDTSTAMP:20200320T004207Z\r\nUID:3b5af39a-d0b3-4049-a839-d7bb8af01f92\r\nSUMMARY:Add events to this calendar.\r\nEND:VTODO\r\nEND:VCALENDAR\r\n"
      DocumentType: ChangeCalendar
      DocumentFormat: TEXT
```

## See also<a name="aws-resource-ssm-document--seealso"></a>
+  [AWS Systems Manager Documents](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-ssm-docs.html) 