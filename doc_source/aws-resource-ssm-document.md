# AWS::SSM::Document<a name="aws-resource-ssm-document"></a>

The `AWS::SSM::Document` resource creates a Systems Manager \(SSM\) document in AWS Systems Manager\. This document defines the actions that Systems Manager performs on your AWS resources\.

## Syntax<a name="aws-resource-ssm-document-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-document-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Document",
  "Properties" : {
      "[Content](#cfn-ssm-document-content)" : Json,
      "[DocumentType](#cfn-ssm-document-documenttype)" : String,
      "[Name](#cfn-ssm-document-name)" : String,
      "[Tags](#cfn-ssm-document-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ssm-document-syntax.yaml"></a>

```
Type: AWS::SSM::Document
Properties: 
  [Content](#cfn-ssm-document-content): Json
  [DocumentType](#cfn-ssm-document-documenttype): String
  [Name](#cfn-ssm-document-name): String
  [Tags](#cfn-ssm-document-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ssm-document-properties"></a>

`Content`  <a name="cfn-ssm-document-content"></a>
The content for the new SSM document in JSON or YAML format\.  
*Required*: Yes  
*Type*: Json  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DocumentType`  <a name="cfn-ssm-document-documenttype"></a>
The type of document to create\.  
*Allowed Values*: `ApplicationConfigurationSchema` \| `Automation` \| `ChangeCalendar` \| `Command` \| `DeploymentStrategy` \| `Package` \| `Policy` \| `Session`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-ssm-document-name"></a>
A name for the Systems Manager document\.  
You can't use the following strings as document name prefixes\. These are reserved by AWS for use as document name prefixes:  
+  `aws-` 
+  `amazon` 
+  `amzn` 
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ssm-document-tags"></a>
AWS CloudFormation resource tags to apply to the document\. Use tags to help you identify and categorize resources\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ssm-document-return-values"></a>

### Ref<a name="aws-resource-ssm-document-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Systems Manager document name, such as `MyNewSSMDocument`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ssm-document--examples"></a>

### Create a document that runs commands on an EC2 Linux instance<a name="aws-resource-ssm-document--examples--Create_a_document_that_runs_commands_on_an_EC2_Linux_instance"></a>

The following SSM document runs the commands you specify on your target EC2 Linux instance\. You specify the commands parameter value when you run the document using Run Command\.

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

### Join a managed instance to a directory in AWS Directory Service<a name="aws-resource-ssm-document--examples--Join_a_managed_instance_to_a_directory_in_AWS_Directory_Service"></a>

The following SSM document joins instances to a directory in AWS Directory Service\. The three runtime configuration parameters specify which directory the instance joins\. You specify these parameter values when you associate the document with an instance\.

#### YAML<a name="aws-resource-ssm-document--examples--Join_a_managed_instance_to_a_directory_in_AWS_Directory_Service--yaml"></a>

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

#### JSON<a name="aws-resource-ssm-document--examples--Join_a_managed_instance_to_a_directory_in_AWS_Directory_Service--json"></a>

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

## See also<a name="aws-resource-ssm-document--seealso"></a>
+  [AWS Systems Manager Documents](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-ssm-docs.html) 