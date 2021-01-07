# cfn\-signal<a name="cfn-signal"></a>

## Description<a name="cfn-signal-Description"></a>

The cfn\-signal helper script signals AWS CloudFormation to indicate whether Amazon EC2 instances have been successfully created or updated\. If you install and configure software applications on instances, you can signal AWS CloudFormation when those software applications are ready\.

You use the cfn\-signal script in conjunction with a [CreationPolicy](aws-attribute-creationpolicy.md) or an Auto Scaling group with a [`WaitOnResourceSignals`](aws-attribute-updatepolicy.md) update policy\. When AWS CloudFormation creates or updates resources with those policies, it suspends work on the stack until the resource receives the requisite number of signals or until the timeout period is exceeded\. For each valid signal that AWS CloudFormation receives, AWS CloudFormation publishes the signals to the stack events so that you track each signal\. For a walkthrough that uses a creation policy and cfn\-signal, see [Deploying applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.

**Note**  
cfn\-signal does not require credentials, so you do not need to use the `--access-key`, `--secret-key`, `--role`, or `--credential-file` options\. However, if no credentials are specified, AWS CloudFormation checks for stack membership and limits the scope of the call to the stack that the instance belongs to\.

## Syntax for resource signaling \(recommended\)<a name="w7739ab1c33c42c31b5"></a>

If you want to signal AWS CloudFormation resources, use the following syntax\.

```
cfn-signal --success|-s signal.to.send \
        --access-key access.key \
        --credential-file|-f credential.file \
        --exit-code|-e exit.code \
        --http-proxy HTTP.proxy \
        --https-proxy HTTPS.proxy \
        --id|-i unique.id \
        --region AWS.region \
        --resource resource.logical.ID \
        --role IAM.role.name \
        --secret-key secret.key \
        --stack stack.name.or.stack.ID \
        --url AWS CloudFormation.endpoint
```

## Syntax for use with wait condition handle<a name="cfn-signal-Syntaxwaitcondition"></a>

If you want to signal a wait condition handle, use the following syntax\.

```
cfn-signal --success|-s signal.to.send \
        --reason|-r resource.status.reason \
        --data|-d data \
        --id|-i unique.id \
        --exit-code|-e exit.code \
        waitconditionhandle.url
```

## Options<a name="cfn-signal-options"></a>

The options that you can use depend on whether you're signaling a creation policy or a wait condition handle\. Some options that apply to a creation policy might not apply to a wait condition handle\.


| Name | Description | Required | 
| --- | --- | --- | 
|  `--access-key` \(resource signaling only\)  |  AWS access key for an account with permission to call the AWS CloudFormation `SignalResource `API\. The credential file parameter supersedes this parameter\. *Type*: String  |  No  | 
|  `-d, --data` \(wait condition handle only\)  |  Data to send back with the `waitConditionHandle`\. Defaults to blank\. *Type*: String *Default*: blank  |  No  | 
|  `-e, --exit-code`   |  The error code from a process that can be used to determine success or failure\. If specified, the `--success` option is ignored\. *Type*: String *Examples*: `-e $?` \(for Linux\), `-e %ERRORLEVEL%` \(for Windows cmd\.exe\), and `-e $lastexitcode` \(for Windows PowerShell\)\.  |  No  | 
|  `-f, --credential-file` \(resource signaling only\)  |  A file that contains both a secret access key and an access key\. The credential file parameter supersedes the \-\-role, \-\-access\-key, and \-\-secret\-key parameters\. *Type*: String  |  No  | 
|  `--http-proxy`  |  An HTTP proxy \(non\-SSL\)\. Use the following format: `http://user:password@host:port` *Type*: String  |  No  | 
|  `--https-proxy`  |  An HTTPS proxy\. Use the following format: `https://user:password@host:port` *Type*: String  |  No  | 
|  `-i, --id`  |  The unique ID to send\. *Type*: String *Default*: The ID of the Amazon EC2 instance\. If the ID cannot be resolved, the machine's Fully Qualified Domain Name \(FQDN\) is returned\.  |  No  | 
|  `-r, --reason ` \(wait condition handle only\)  |  A status reason for the resource event \(currently only used on failure\) \- defaults to 'Configuration failed' if success is false\. *Type*: String  |  No  | 
| \-\-region \(resource signaling only\) |  The AWS CloudFormation regional endpoint to use\. *Type*: String *Default*: `us-east-1`  |  No  | 
| \-\-resource \(resource signaling only\) |  The [logical ID](resources-section-structure.md) of the resource that contains the creations policy you want to signal\. *Type*: String  |  Yes  | 
|  `--role` \(resource signaling only\)  |  The name of an IAM role that is associated with the instance\. *Type*: String Condition: The credential file parameter supersedes this parameter\.  |  No  | 
|  `-s, --success`   |  if true, signal SUCCESS, else FAILURE\. *Type*: Boolean *Default*: `true`  |  No  | 
|  `--secret-key` \(resource signaling only\)  |  AWS secret access key that corresponds to the specified AWS access key\. *Type*: String  |  No  | 
|  `--stack` \(resource signaling only\)  |  The stack name or stack ID that contains the resource you want to signal\. *Type*: String  |  Yes  | 
| \-u, \-\-url \(resource signaling only\) |  The AWS CloudFormation endpoint to use\. *Type*: String  |  No  | 
|  `waitconditionhandle.url` \(wait condition handle only\)  |  A presigned URL that you can use to signal success or failure to an associated `WaitCondition` *Type*: String  |  Yes  | 

## Example<a name="cfn-signal-Examples"></a>

### Amazon Linux example<a name="w7739ab1c33c42c31c11b2"></a>

A common usage pattern is to use cfn\-init and cfn\-signal together\. The cfn\-signal call uses the return status of the call to cfn\-init \(using the $? shell construct\)\. If the application fails to install, the instance will fail to create and the stack will rollback\. For Windows stacks, see [Bootstrapping AWS CloudFormation Windows stacks](cfn-windows-stacks-bootstrapping.md)\.

#### JSON<a name="cfn-signal-example.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Simple EC2 instance",
    "Resources": {
        "MyInstance": {
            "Type": "AWS::EC2::Instance",
            "Metadata": {
                "AWS::CloudFormation::Init": {
                    "config": {
                        "files": {
                            "/tmp/test.txt": {
                                "content": "Hello world!",
                                "mode": "000755",
                                "owner": "root",
                                "group": "root"
                            }
                        }
                    }
                }
            },
            "Properties": {
                "ImageId": "ami-a4c7edb2",
                "InstanceType": "t2.micro",
                "UserData": {
                    "Fn::Base64": {
                        "Fn::Join": [
                            "",
                            [
                                "#!/bin/bash -x\n",
                                "# Install the files and packages from the metadata\n",
                                "/opt/aws/bin/cfn-init -v ",
                                "         --stack ",
                                {
                                    "Ref": "AWS::StackName"
                                },
                                "         --resource MyInstance ",
                                "         --region ",
                                {
                                    "Ref": "AWS::Region"
                                },
                                "\n",
                                "# Signal the status from cfn-init\n",
                                "/opt/aws/bin/cfn-signal -e $? ",
                                "         --stack ",
                                {
                                    "Ref": "AWS::StackName"
                                },
                                "         --resource MyInstance ",
                                "         --region ",
                                {
                                    "Ref": "AWS::Region"
                                },
                                "\n"
                            ]
                        ]
                    }
                }
            },
            "CreationPolicy": {
                "ResourceSignal": {
                    "Timeout": "PT5M"
                }
            }
        }
    }
}
```

#### YAML<a name="cfn-signal-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Simple EC2 instance
Resources:
  MyInstance:
    Type: AWS::EC2::Instance
    Metadata:
      'AWS::CloudFormation::Init':
        config:
          files:
            /tmp/test.txt:
              content: Hello world!
              mode: '000755'
              owner: root
              group: root
    Properties:
      ImageId: ami-a4c7edb2
      InstanceType: t2.micro
      UserData: !Base64
        'Fn::Join':
          - ''
          - - |
              #!/bin/bash -x
            - |
              # Install the files and packages from the metadata
            - '/opt/aws/bin/cfn-init -v '
            - '         --stack '
            - !Ref 'AWS::StackName'
            - '         --resource MyInstance '
            - '         --region '
            - !Ref 'AWS::Region'
            - |+

            - |
              # Signal the status from cfn-init
            - '/opt/aws/bin/cfn-signal -e $? '
            - '         --stack '
            - !Ref 'AWS::StackName'
            - '         --resource MyInstance '
            - '         --region '
            - !Ref 'AWS::Region'
            - |+

    CreationPolicy:
      ResourceSignal:
        Timeout: PT5M
```

#### Examples<a name="w7739ab1c33c42c31c11b2b8"></a>

Several AWS CloudFormation sample templates use cfn\-signal, including the following templates\.
+  [LAMP: Single EC2 instance with local MySQL database](https://s3.amazonaws.com/cloudformation-templates-us-east-1/LAMP_Single_Instance.template) 
+  [WordPress: Single EC2 instance with local MySQL database](https://s3.amazonaws.com/cloudformation-templates-us-east-1/WordPress_Single_Instance.template) 