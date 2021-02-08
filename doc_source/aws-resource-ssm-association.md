# AWS::SSM::Association<a name="aws-resource-ssm-association"></a>

The `AWS::SSM::Association` resource creates a State Manager association for your managed instances\. A State Manager association defines the state that you want to maintain on your instances\. For example, an association can specify that anti\-virus software must be installed and running on your instances, or that certain ports must be closed\. For static targets, the association specifies a schedule for when the configuration is reapplied\. For dynamic targets, such as an AWS Resource Group or an AWS Autoscaling Group, State Manager applies the configuration when new instances are added to the group\. The association also specifies actions to take when applying the configuration\. For example, an association for anti\-virus software might run once a day\. If the software is not installed, then State Manager installs it\. If the software is installed, but the service is not running, then the association might instruct State Manager to start the service\. 

## Syntax<a name="aws-resource-ssm-association-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-association-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Association",
  "Properties" : {
      "[ApplyOnlyAtCronInterval](#cfn-ssm-association-applyonlyatcroninterval)" : Boolean,
      "[AssociationName](#cfn-ssm-association-associationname)" : String,
      "[AutomationTargetParameterName](#cfn-ssm-association-automationtargetparametername)" : String,
      "[ComplianceSeverity](#cfn-ssm-association-complianceseverity)" : String,
      "[DocumentVersion](#cfn-ssm-association-documentversion)" : String,
      "[InstanceId](#cfn-ssm-association-instanceid)" : String,
      "[MaxConcurrency](#cfn-ssm-association-maxconcurrency)" : String,
      "[MaxErrors](#cfn-ssm-association-maxerrors)" : String,
      "[Name](#cfn-ssm-association-name)" : String,
      "[OutputLocation](#cfn-ssm-association-outputlocation)" : InstanceAssociationOutputLocation,
      "[Parameters](#cfn-ssm-association-parameters)" : {Key : Value, ...},
      "[ScheduleExpression](#cfn-ssm-association-scheduleexpression)" : String,
      "[SyncCompliance](#cfn-ssm-association-synccompliance)" : String,
      "[Targets](#cfn-ssm-association-targets)" : [ Target, ... ],
      "[WaitForSuccessTimeoutSeconds](#cfn-ssm-association-waitforsuccesstimeoutseconds)" : Integer
    }
}
```

### YAML<a name="aws-resource-ssm-association-syntax.yaml"></a>

```
Type: AWS::SSM::Association
Properties: 
  [ApplyOnlyAtCronInterval](#cfn-ssm-association-applyonlyatcroninterval): Boolean
  [AssociationName](#cfn-ssm-association-associationname): String
  [AutomationTargetParameterName](#cfn-ssm-association-automationtargetparametername): String
  [ComplianceSeverity](#cfn-ssm-association-complianceseverity): String
  [DocumentVersion](#cfn-ssm-association-documentversion): String
  [InstanceId](#cfn-ssm-association-instanceid): String
  [MaxConcurrency](#cfn-ssm-association-maxconcurrency): String
  [MaxErrors](#cfn-ssm-association-maxerrors): String
  [Name](#cfn-ssm-association-name): String
  [OutputLocation](#cfn-ssm-association-outputlocation): 
    InstanceAssociationOutputLocation
  [Parameters](#cfn-ssm-association-parameters): 
    Key : Value
  [ScheduleExpression](#cfn-ssm-association-scheduleexpression): String
  [SyncCompliance](#cfn-ssm-association-synccompliance): String
  [Targets](#cfn-ssm-association-targets): 
    - Target
  [WaitForSuccessTimeoutSeconds](#cfn-ssm-association-waitforsuccesstimeoutseconds): Integer
```

## Properties<a name="aws-resource-ssm-association-properties"></a>

`ApplyOnlyAtCronInterval`  <a name="cfn-ssm-association-applyonlyatcroninterval"></a>
By default, when you create a new associations, the system runs it immediately after it is created and then according to the schedule you specified\. Specify this option if you don't want an association to run immediately after you create it\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssociationName`  <a name="cfn-ssm-association-associationname"></a>
Specify a descriptive name for the association\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutomationTargetParameterName`  <a name="cfn-ssm-association-automationtargetparametername"></a>
Specify the target for the association\. This target is required for associations that use an Automation document and target resources by using rate controls\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComplianceSeverity`  <a name="cfn-ssm-association-complianceseverity"></a>
The severity level that is assigned to the association\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CRITICAL | HIGH | LOW | MEDIUM | UNSPECIFIED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentVersion`  <a name="cfn-ssm-association-documentversion"></a>
The version of the SSM document to associate with the target\.  
*Required*: No  
*Type*: String  
*Pattern*: `([$]LATEST|[$]DEFAULT|^[1-9][0-9]*$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-ssm-association-instanceid"></a>
The ID of the instance that the SSM document is associated with\. You must specify the `InstanceId` or `Targets` property\.  
`InstanceId` has been deprecated\. To specify an instance ID for an association, use the `Targets` parameter\. If you use the parameter `InstanceId`, you cannot use the parameters `AssociationName`, `DocumentVersion`, `MaxErrors`, `MaxConcurrency`, `OutputLocation`, or `ScheduleExpression`\. To use these parameters, you must use the `Targets` parameter\.
*Required*: Conditional  
*Type*: String  
*Pattern*: `(^i-(\w{8}|\w{17})$)|(^mi-\w{17}$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxConcurrency`  <a name="cfn-ssm-association-maxconcurrency"></a>
The maximum number of targets allowed to run the association at the same time\. You can specify a number, for example 10, or a percentage of the target set, for example 10%\. The default value is 100%, which means all targets run the association at the same time\.  
If a new instance starts and attempts to run an association while Systems Manager is running MaxConcurrency associations, the association is allowed to run\. During the next association interval, the new instance will process its association within the limit specified for MaxConcurrency\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `7`  
*Pattern*: `^([1-9][0-9]*|[1-9][0-9]%|[1-9]%|100%)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxErrors`  <a name="cfn-ssm-association-maxerrors"></a>
The number of errors that are allowed before the system stops sending requests to run the association on additional targets\. You can specify either an absolute number of errors, for example 10, or a percentage of the target set, for example 10%\. If you specify 3, for example, the system stops sending requests when the fourth error is received\. If you specify 0, then the system stops sending requests after the first error is returned\. If you run an association on 50 instances and set MaxError to 10%, then the system stops sending the request when the sixth error is received\.  
Executions that are already running an association when MaxErrors is reached are allowed to complete, but some of these executions may fail as well\. If you need to ensure that there won't be more than max\-errors failed executions, set MaxConcurrency to 1 so that executions proceed one at a time\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `7`  
*Pattern*: `^([1-9][0-9]*|[0]|[1-9][0-9]%|[0-9]%|100%)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-association-name"></a>
The name of the SSM document that contains the configuration information for the instance\. You can specify `Command` or `Automation` documents\. The documents can be AWS\-predefined documents, documents you created, or a document that is shared with you from another account\. For SSM documents that are shared with you from other AWS accounts, you must specify the complete SSM document ARN, in the following format:  
`arn:partition:ssm:region:account-id:document/document-name`  
For example: `arn:aws:ssm:us-east-2:12345678912:document/My-Shared-Document`  
For AWS\-predefined documents and SSM documents you created in your account, you only need to specify the document name\. For example, AWS\-ApplyPatchBaseline or My\-Document\.   
*Required*: Yes  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_\-.:/]{3,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputLocation`  <a name="cfn-ssm-association-outputlocation"></a>
An S3 bucket where you want to store the output details of the request\.  
*Required*: No  
*Type*: [InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-ssm-association-parameters"></a>
The parameters for the runtime configuration of the document\.  
*Required*: No  
*Type*: Map of [ParameterValues](aws-properties-ssm-association-parametervalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-ssm-association-scheduleexpression"></a>
A cron expression that specifies a schedule when the association runs\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SyncCompliance`  <a name="cfn-ssm-association-synccompliance"></a>
The mode for generating association compliance\. You can specify `AUTO` or `MANUAL`\. In `AUTO` mode, the system uses the status of the association execution to determine the compliance status\. If the association execution runs successfully, then the association is `COMPLIANT`\. If the association execution doesn't run successfully, the association is `NON-COMPLIANT`\.  
In `MANUAL` mode, you must specify the `AssociationId` as a parameter for the PutComplianceItems API action\. In this case, compliance data is not managed by State Manager\. It is managed by your direct call to the PutComplianceItems API action\.  
By default, all associations use `AUTO` mode\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | MANUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-ssm-association-targets"></a>
The targets for the association\. You must specify the `InstanceId` or `Targets` property\.  
*Required*: Conditional  
*Type*: List of [Target](aws-properties-ssm-association-target.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitForSuccessTimeoutSeconds`  <a name="cfn-ssm-association-waitforsuccesstimeoutseconds"></a>
The number of seconds the service should wait for the association status to show "Success" before proceeding with the stack execution\. If the association status doesn't show "Success" after the specified number of seconds, then stack creation fails\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ssm-association-return-values"></a>

### Fn::GetAtt<a name="aws-resource-ssm-association-return-values-fn--getatt"></a>

#### <a name="aws-resource-ssm-association-return-values-fn--getatt-fn--getatt"></a>

`AssociationId`  <a name="AssociationId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Examples<a name="aws-resource-ssm-association--examples"></a>

### Create an association for a specific instance<a name="aws-resource-ssm-association--examples--Create_an_association_for_a_specific_instance"></a>

The following example creates an association that uses the AWS\-RunShellScript SSM document\. The association runs a simple command on a specific instance\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_for_a_specific_instance--json"></a>

```
{
  "Resources": {
    "SpecificInstanceIdAssociation": {
      "Type": "AWS::SSM::Association",
      "Properties": {
        "Name": "AWS-RunShellScript",
        "Targets": [
          {
            "Key": "InstanceIds",
            "Values": [
              "i-1234567890abcdef0"
            ]
          }
        ],
        "Parameters": {
          "commands": [
            "ls"
          ],
          "workingDirectory": [
            "/"
          ]
        },
        "WaitForSuccessTimeoutSeconds": 300
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_for_a_specific_instance--yaml"></a>

```
---
Resources:
  SpecificInstanceIdAssociation:
    Type: AWS::SSM::Association
    Properties:
      Name: AWS-RunShellScript
      Targets:
      - Key: InstanceIds
        Values:
        - i-1234567890abcdef0
      Parameters:
        commands:
        - ls
        workingDirectory:
        - "/"
      WaitForSuccessTimeoutSeconds: 300
```

### Create an association for all managed instances in an AWS account<a name="aws-resource-ssm-association--examples--Create_an_association_for_all_managed_instances_in_an_AWS_account"></a>

The following example creates an association that uses the AWS\-UpdateSSMAgent SSM document\. The association updates SSM Agent on all managed instances \(instances configured for Systems Manager\) in the user's AWS account according to the specified CRON schedule\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_for_all_managed_instances_in_an_AWS_account--json"></a>

```
{
  "Resources": {
    "AllInstanceIdsAssociation": {
      "Type": "AWS::SSM::Association",
      "Properties": {
        "AssociationName": "UpdateSSMAgent",
        "Name": "AWS-UpdateSSMAgent",
        "ScheduleExpression": "cron(0 2 ? * SUN *)",
        "Targets": [
          {
            "Key": "InstanceIds",
            "Values": [
              "*"
            ]
          }
        ],
        "WaitForSuccessTimeoutSeconds": 300
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_for_all_managed_instances_in_an_AWS_account--yaml"></a>

```
---
Resources:
  AllInstanceIdsAssociation:
    Type: AWS::SSM::Association
    Properties:
      AssociationName: UpdateSSMAgent
      Name: AWS-UpdateSSMAgent
      ScheduleExpression: cron(0 2 ? * SUN *)
      Targets:
      - Key: InstanceIds
        Values:
        - "*"
      WaitForSuccessTimeoutSeconds: 300
```

### Create an association for a specific tag<a name="aws-resource-ssm-association--examples--Create_an_association_for_a_specific_tag"></a>

The following example creates an association that uses the AWS\-UpdateSSMAgent SSM document\. The association updates SSM Agent on all managed instances that are assigned a tag key of `Environment` and value of `Production`\. The association runs every seven days according to the specified rate expression\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_for_a_specific_tag--json"></a>

```
{
  "Resources": {
    "TaggedInstancesAssociation": {
      "Type": "AWS::SSM::Association",
      "Properties": {
        "AssociationName": "UpdateSSMAgent",
        "Name": "AWS-UpdateSSMAgent",
        "ScheduleExpression": "rate(7 days)",
        "Targets": [
          {
            "Key": "tag:Environment",
            "Values": [
              "Production"
            ]
          }
        ],
        "WaitForSuccessTimeoutSeconds": 300
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_for_a_specific_tag--yaml"></a>

```
---
Resources:
  TaggedInstancesAssociation:
    Type: AWS::SSM::Association
    Properties:
      AssociationName: UpdateSSMAgent
      Name: AWS-UpdateSSMAgent
      ScheduleExpression: rate(7 days)
      Targets:
      - Key: tag:Environment
        Values:
        - Production
      WaitForSuccessTimeoutSeconds: 300
```

### Create an association that associates an automation document with an instance<a name="aws-resource-ssm-association--examples--Create_an_association_that_associates_an_automation_document_with_an_instance"></a>

The following example creates an association that assigns the AWS\-StopEC2Instance automation document to a specific instance\. 

**Note**  
This example specifies the following Amazon Resource Name \(ARN\): `arn:${AWS::Partition}:iam::aws:policy/AmazonEC2FullAccess`\. This policy provides more than the required permissions to stop the instance\. We recommend that you use a policy with more restrictive permissions\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_associates_an_automation_document_with_an_instance--json"></a>

```
{
  "Resources": {
    "AutomationExecutionRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": "ssm.amazonaws.com"
              },
              "Action": [
                "sts:AssumeRole"
              ]
            }
          ]
        },
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/AmazonEC2FullAccess"
        ]
      }
    },
    "AutomationAssociation": {
      "Type": "AWS::SSM::Association",
      "Properties": {
        "Name": "AWS-StopEC2Instance",
        "Parameters": {
          "AutomationAssumeRole": [
            "AutomationExecutionRole.Arn"
          ]
        },
        "Targets": [
          {
            "Key": "ParameterValues",
            "Values": [
              "i-1234567890abcdef0"
            ]
          }
        ],
        "AutomationTargetParameterName": "InstanceId"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_associates_an_automation_document_with_an_instance--yaml"></a>

```
---
Resources:
  AutomationExecutionRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service: ssm.amazonaws.com
            Action:
              - sts:AssumeRole
      Path: /
      ManagedPolicyArns:
        - !Sub arn:${AWS::Partition}:iam::aws:policy/AmazonEC2FullAccess
  AutomationAssociation:
    Type: AWS::SSM::Association
    Properties:
      Name: AWS-StopEC2Instance
      Parameters:
        AutomationAssumeRole:
          - !GetAtt AutomationExecutionRole.Arn
      Targets:
        - Key: ParameterValues
          Values:
            - i-1234567890abcdef0
      AutomationTargetParameterName: InstanceId
```

### Create an association that uses rate controls and sends log output to Amazon S3<a name="aws-resource-ssm-association--examples--Create_an_association_that_uses_rate_controls_and_sends_log_output_to_Amazon_S3"></a>

The following example creates an association that uses rate controls\. The association attempts to update SSM Agent on only 20% of instances at one time\. Systems Manager stops the association from running on any additional instances if the execution fails on 5% of the total number of instances\. System Manager also logs the association output to Amazon S3\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_uses_rate_controls_and_sends_log_output_to_Amazon_S3--json"></a>

```
{
  "Resources": {
    "RateControlAssociation": {
      "Type": "AWS::SSM::Association",
      "Properties": {
        "Name": "AWS-UpdateSSMAgent",
        "Targets": [
          {
            "Key": "InstanceIds",
            "Values": [
              "*"
            ]
          }
        ],
        "MaxConcurrency": "20%",
        "MaxErrors": "5%"
      },
      "OutputLocation": {
        "S3Location": {
          "OutputS3BucketName": "MyAssociationOutputBucket",
          "OutputS3KeyPrefix": "my-agent-update-output"
        }
      },
      "WaitForSuccessTimeoutSeconds": 300
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_uses_rate_controls_and_sends_log_output_to_Amazon_S3--yaml"></a>

```
---
Resources:
  RateControlAssociation:
    Type: AWS::SSM::Association
    Properties:
      Name: AWS-UpdateSSMAgent
      Targets:
        - Key: InstanceIds
          Values:
            - "*"
      MaxConcurrency: 20%
      MaxErrors: 5%
	  OutputLocation:
        S3Location:
          OutputS3BucketName: MyAssociationOutputBucket
          OutputS3KeyPrefix: my-agent-update-output
		WaitForSuccessTimeoutSeconds: 300
```

### Create an association that works with Ansible<a name="aws-resource-ssm-association--examples--Create_an_association_that_works_with_Ansible"></a>

The following example creates an association that uses Ansible and Systems Manager to deploy Nginx\. This template copies the Ansible Playbook from a Github repo\. The target is based on instance ID\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_works_with_Ansible--json"></a>

```
{
  "Description": "Deploy Single EC2 Linux Instance",
  "Parameters": {
    "LatestAmiId": {
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
    },
    "GitHubOwner": {
      "Type": "String"
    },
    "GitHubRepo": {
      "Type": "String"
    },
    "GitHubBranch": {
      "Type": "String"
    }
  },
  "Resources": {
    "SSMAssocLogs": {
      "Type": "AWS::S3::Bucket"
    },
    "SSMInstanceRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject"
                  ],
                  "Resource": [
                    "arn:aws:s3:::aws-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*",
                    "arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*",
                    "arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "ssm-custom-s3-policy"
          },
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject",
                    "s3:PutObject",
                    "s3:PutObjectAcl",
                    "s3:ListBucket"
                  ],
                  "Resource": [
                    "arn:${AWS::Partition}:s3:::${SSMAssocLogs}/*",
                    "arn:${AWS::Partition}:s3:::${SSMAssocLogs}"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "s3-instance-bucket-policy"
          }
        ],
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore"
        ],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "ec2.amazonaws.com",
                  "ssm.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        }
      }
    },
    "SSMInstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Roles": [
          "SSMInstanceRole"
        ]
      }
    },
    "EC2Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "ImageId": "LatestAmiId",
        "InstanceType": "t3.small",
        "IamInstanceProfile": "SSMInstanceProfile"
      }
    },
    "AnsibleAssociation": {
      "Type": "AWS::SSM::Association",
      "Properties": {
        "Name": "AWS-ApplyAnsiblePlaybooks",
        "WaitForSuccessTimeoutSeconds": 300,
        "Targets": [
          {
            "Key": "InstanceIds",
            "Values": [
              "EC2Instance"
            ]
          }
        ],
        "OutputLocation": {
          "S3Location": {
            "OutputS3BucketName": "SSMAssocLogs",
            "OutputS3KeyPrefix": "logs/"
          }
        },
        "Parameters": {
          "SourceType": [
            "GitHub"
          ],
          "SourceInfo": [
            "{\"owner\":\"${GitHubOwner}\",\n\"repository\":\"${GitHubRepo}\",\n\"path\":\"\",\n\"getOptions\":\"branch:${GitHubBranch}\"}\n"
          ],
          "InstallDependencies": [
            "True"
          ],
          "PlaybookFile": [
            "playbook.yml"
          ],
          "ExtraVariables": [
            "SSM=True"
          ],
          "Check": [
            "False"
          ],
          "Verbose": [
            "-v"
          ]
        }
      }
    }
  },
  "Outputs": {
    "WebServerPublic": {
      "Value": "EC2Instance.PublicDnsName",
      "Description": "Public DNS for WebServer"
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_works_with_Ansible--yaml"></a>

```
---
Description: "Deploy Single EC2 Linux Instance"
Parameters:
  # Using SSM Parameter Store to fetch the Latest AMI for Amazon Linux, eliminates the need for AMI Mappings
  LatestAmiId:
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
  GitHubOwner:
    Type: 'String'
  GitHubRepo:
    Type: 'String'
  GitHubBranch:
    Type: 'String'
Resources:
  SSMAssocLogs:
    Type: AWS::S3::Bucket
  SSMInstanceRole: 
    Type : AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                Resource: 
                  - !Sub 'arn:aws:s3:::aws-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*'
                  - !Sub 'arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*'
                Effect: Allow
          PolicyName: ssm-custom-s3-policy
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                  - s3:PutObject
                  - s3:PutObjectAcl
                  - s3:ListBucket
                Resource: 
                  - !Sub 'arn:${AWS::Partition}:s3:::${SSMAssocLogs}/*'
                  - !Sub 'arn:${AWS::Partition}:s3:::${SSMAssocLogs}'
                Effect: Allow
          PolicyName: s3-instance-bucket-policy
      Path: /
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
        - Effect: "Allow"
          Principal:
            Service:
            - "ec2.amazonaws.com"
            - "ssm.amazonaws.com"
          Action: "sts:AssumeRole"
  SSMInstanceProfile:
    Type: "AWS::IAM::InstanceProfile"
    Properties:
      Roles:
      - !Ref SSMInstanceRole
  EC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: !Ref LatestAmiId
      InstanceType: "t3.small"
      IamInstanceProfile: !Ref SSMInstanceProfile
  AnsibleAssociation:
    Type: AWS::SSM::Association
    Properties:
      # Here using the AWS-ApplyAnsiblePlaybooks
      Name: AWS-ApplyAnsiblePlaybooks
      WaitForSuccessTimeoutSeconds: 300
      # Targeting Instance by InstanceId passed from the Logical ID of Instance being created 
      # in CloudFormation
      Targets:
        - Key: InstanceIds
          Values: [ !Ref EC2Instance ]
      OutputLocation:
        S3Location: 
          OutputS3BucketName: !Ref SSMAssocLogs
          OutputS3KeyPrefix: 'logs/'
      Parameters:
        # Getting an Ansible Playbook from a GitHub Location
        SourceType:
          - 'GitHub'
        # At a minimum must include the following GitHub repo information, if using a private repo 
        # would want to include the GitHub Token option
        SourceInfo:
          -  !Sub |
              {"owner":"${GitHubOwner}",
              "repository":"${GitHubRepo}",
              "path":"",
              "getOptions":"branch:${GitHubBranch}"}
        # Installing Ansible and its dependencies
        InstallDependencies:
          - 'True'
        # Playbook file we want to run
        PlaybookFile:
          - 'playbook.yml'
        ExtraVariables:
          - 'SSM=True'
        Check:
          - 'False'
        Verbose:
          - '-v'
Outputs:
  WebServerPublic:
    Value: !GetAtt 'EC2Instance.PublicDnsName'
    Description: Public DNS for WebServer
```

### Create an association that runs a bash script<a name="aws-resource-ssm-association--examples--Create_an_association_that_runs_a_bash_script"></a>

The following example creates an association that runs a bash script\. Target is based on tags\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_runs_a_bash_script--json"></a>

```
{
  "Description": "Deploy Single EC2 Linux Instance Install and Install Nginx by a State Manager Association",
  "Parameters": {
    "LatestAmiId": {
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
    }
  },
  "Resources": {
    "SSMAssocLogs": {
      "Type": "AWS::S3::Bucket"
    },
    "SSMInstanceRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject"
                  ],
                  "Resource": [
                    "arn:aws:s3:::aws-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*",
                    "arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*",
                    "arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "ssm-custom-s3-policy"
          },
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject",
                    "s3:PutObject",
                    "s3:PutObjectAcl",
                    "s3:ListBucket"
                  ],
                  "Resource": [
                    "arn:${AWS::Partition}:s3:::${SSMAssocLogs}/*",
                    "arn:${AWS::Partition}:s3:::${SSMAssocLogs}"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "s3-instance-bucket-policy"
          }
        ],
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore",
          "arn:${AWS::Partition}:iam::aws:policy/CloudWatchAgentServerPolicy"
        ],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "ec2.amazonaws.com",
                  "ssm.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        }
      }
    },
    "SSMInstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Roles": [
          "SSMInstanceRole"
        ]
      }
    },
    "EC2Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "ImageId": "LatestAmiId",
        "InstanceType": "t3.medium",
        "IamInstanceProfile": "SSMInstanceProfile",
        "Tags": [
          {
            "Key": "nginx",
            "Value": "yes"
          }
        ]
      }
    },
    "NginxAssociation": {
      "DependsOn": "EC2Instance",
      "Type": "AWS::SSM::Association",
      "Properties": {
        "Name": "AWS-RunShellScript",
        "WaitForSuccessTimeoutSeconds": 300,
        "Targets": [
          {
            "Key": "tag:nginx",
            "Values": [
              "yes"
            ]
          }
        ],
        "OutputLocation": {
          "S3Location": {
            "OutputS3BucketName": "SSMAssocLogs",
            "OutputS3KeyPrefix": "logs/"
          }
        },
        "Parameters": {
          "commands": [
            "sudo amazon-linux-extras install nginx1 -y\nsudo service nginx start\n"
          ]
        }
      }
    }
  },
  "Outputs": {
    "WebServerPublic": {
      "Value": "EC2Instance.PublicDnsName",
      "Description": "Public DNS for WebServer"
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_runs_a_bash_script--yaml"></a>

```
---
Description: "Deploy Single EC2 Linux Instance Install and Install Nginx by a State Manager Association"
Parameters:
  LatestAmiId:
    Type: 'AWS::SSM::Parameter::Value*<AWS::EC2::Image::Id>'
    Default: "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
Resources:
  SSMAssocLogs:
    Type: AWS::S3::Bucket
  # Role that allows SSM Agent to communicate with SSM and allows use of all features of SSM
  SSMInstanceRole: 
    Type : AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                Resource: 
                  - !Sub 'arn:aws:s3:::aws-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*'
                  - !Sub 'arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*'
                Effect: Allow
          PolicyName: ssm-custom-s3-policy
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                  - s3:PutObject
                  - s3:PutObjectAcl
                  - s3:ListBucket
                Resource: 
                  - !Sub 'arn:${AWS::Partition}:s3:::${SSMAssocLogs}/*'
                  - !Sub 'arn:${AWS::Partition}:s3:::${SSMAssocLogs}'
                Effect: Allow
          PolicyName: s3-instance-bucket-policy
      Path: /
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore'
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/CloudWatchAgentServerPolicy'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
        - Effect: "Allow"
          Principal:
            Service:
            - "ec2.amazonaws.com"
            - "ssm.amazonaws.com"
          Action: "sts:AssumeRole"
  SSMInstanceProfile:
    Type: "AWS::IAM::InstanceProfile"
    Properties:
      Roles:
      - !Ref SSMInstanceRole
  EC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: !Ref LatestAmiId
      InstanceType: "t3.medium"
      IamInstanceProfile: !Ref SSMInstanceProfile
      Tags:
      - Key: 'nginx'
        Value: 'yes'
  NginxAssociation:
    DependsOn: EC2Instance
    # CloudFormation Resource Type that creates State Manager Associations
    Type: AWS::SSM::Association
    Properties:
      # Command Document that this Association will run
      Name: AWS-RunShellScript
      WaitForSuccessTimeoutSeconds: 300
      # Targeting Instance by Tags
      Targets:
        - Key: tag:nginx
          Values:
            - 'yes'
      # The passing in the S3 Bucket that is created in the template that logs will be sent to
      OutputLocation:
        S3Location: 
          OutputS3BucketName: !Ref SSMAssocLogs
          OutputS3KeyPrefix: 'logs/'
      # Parameters for the AWS-RunShellScript, in this case commands to install nginx
      Parameters:
        commands: 
          - |
              sudo amazon-linux-extras install nginx1 -y
              sudo service nginx start
Outputs:
  WebServerPublic:
    Value: !GetAtt 'EC2Instance.PublicDnsName'
    Description: Public DNS for WebServer
```

### Create an association that runs a bash script with Systems Manager Automation<a name="aws-resource-ssm-association--examples--Create_an_association_that_runs_a_bash_script_with_Systems_Manager_Automation"></a>

The following example creates an assocation that runs a bash script using State Manager and Automation with multiple steps\. Target is based on tags\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_runs_a_bash_script_with_Systems_Manager_Automation--json"></a>

```
{
  "Description": "Deploy Single EC2 Linux Instance",
  "Parameters": {
    "LatestAmiId": {
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
    }
  },
  "Resources": {
    "SSMAssocLogs": {
      "Type": "AWS::S3::Bucket"
    },
    "nginxInstallAutomation": {
      "Type": "AWS::SSM::Document",
      "Properties": {
        "DocumentType": "Automation",
        "Content": {
          "schemaVersion": "0.3",
          "description": "Updates AMI with Linux distribution packages and installs Nginx software",
          "assumeRole": "{{AutomationAssumeRole}}",
          "parameters": {
            "InstanceId": {
              "description": "ID of the Instance.",
              "type": "String"
            },
            "AutomationAssumeRole": {
              "default": "",
              "description": "(Optional) The ARN of the role that allows Automation to perform the actions on your behalf.",
              "type": "String"
            }
          },
          "mainSteps": [
            {
              "name": "updateOSSoftware",
              "action": "aws:runCommand",
              "maxAttempts": 3,
              "timeoutSeconds": 3600,
              "inputs": {
                "DocumentName": "AWS-RunShellScript",
                "InstanceIds": [
                  "{{InstanceId}}"
                ],
                "CloudWatchOutputConfig": {
                  "CloudWatchOutputEnabled": "true"
                },
                "Parameters": {
                  "commands": [
                    "#!/bin/bash\nsudo yum update -y\nneeds-restarting -r\nif [ $? -eq 1 ]\nthen\n        exit 194\nelse\n        exit 0\nfi\n"
                  ]
                }
              }
            },
            {
              "name": "InstallNginx",
              "action": "aws:runCommand",
              "inputs": {
                "DocumentName": "AWS-RunShellScript",
                "InstanceIds": [
                  "{{InstanceId}}"
                ],
                "CloudWatchOutputConfig": {
                  "CloudWatchOutputEnabled": "true"
                },
                "Parameters": {
                  "commands": [
                    "sudo amazon-linux-extras install nginx1 -y\nsudo service nginx start\n"
                  ]
                }
              }
            },
            {
              "name": "TestInstall",
              "action": "aws:runCommand",
              "maxAttempts": 3,
              "timeoutSeconds": 3600,
              "onFailure": "Abort",
              "inputs": {
                "DocumentName": "AWS-RunShellScript",
                "InstanceIds": [
                  "{{InstanceId}}"
                ],
                "Parameters": {
                  "commands": [
                    "curl localhost\n"
                  ]
                }
              }
            }
          ]
        }
      }
    },
    "SSMExecutionRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "ssm:StartAssociationsOnce",
                    "ssm:CreateAssociation",
                    "ssm:CreateAssociationBatch",
                    "ssm:UpdateAssociation"
                  ],
                  "Resource": "*",
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "ssm-association"
          }
        ],
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/service-role/AmazonSSMAutomationRole"
        ],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "ec2.amazonaws.com",
                  "ssm.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        }
      }
    },
    "SSMInstanceRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject"
                  ],
                  "Resource": [
                    "arn:aws:s3:::aws-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*",
                    "arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*",
                    "arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "ssm-custom-s3-policy"
          },
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject",
                    "s3:PutObject",
                    "s3:PutObjectAcl",
                    "s3:ListBucket"
                  ],
                  "Resource": [
                    "arn:${AWS::Partition}:s3:::${SSMAssocLogs}/*",
                    "arn:${AWS::Partition}:s3:::${SSMAssocLogs}"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "s3-instance-bucket-policy"
          }
        ],
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore",
          "arn:${AWS::Partition}:iam::aws:policy/CloudWatchAgentServerPolicy"
        ],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "ec2.amazonaws.com",
                  "ssm.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        }
      }
    },
    "SSMInstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Roles": [
          "SSMInstanceRole"
        ]
      }
    },
    "EC2Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "ImageId": "LatestAmiId",
        "InstanceType": "t3.medium",
        "IamInstanceProfile": "SSMInstanceProfile",
        "Tags": [
          {
            "Key": "nginx",
            "Value": true
          }
        ]
      }
    },
    "NginxAssociation": {
      "DependsOn": "EC2Instance",
      "Type": "AWS::SSM::Association",
      "Properties": {
        "Name": "nginxInstallAutomation",
        "WaitForSuccessTimeoutSeconds": 300,
        "OutputLocation": {
          "S3Location": {
            "OutputS3BucketName": "SSMAssocLogs",
            "OutputS3KeyPrefix": "logs/"
          }
        },
        "AutomationTargetParameterName": "InstanceId",
        "Parameters": {
          "AutomationAssumeRole": [
            "SSMExecutionRole.Arn"
          ]
        },
        "Targets": [
          {
            "Key": "tag:nginx",
            "Values": [
              true
            ]
          }
        ]
      }
    }
  },
  "Outputs": {
    "WebServerPublic": {
      "Value": "EC2Instance.PublicDnsName",
      "Description": "Public DNS for WebServer"
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_runs_a_bash_script_with_Systems_Manager_Automation--yaml"></a>

```
---
Description: "Deploy Single EC2 Linux Instance"
Parameters:
  LatestAmiId:
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: "/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
Resources:
  SSMAssocLogs:
    Type: AWS::S3::Bucket
  nginxInstallAutomation:
    Type: AWS::SSM::Document
    Properties:
      DocumentType: Automation
      Content:
        schemaVersion: "0.3"
        description: "Updates AMI with Linux distribution packages and installs Nginx software"
        assumeRole: "{{AutomationAssumeRole}}"
        parameters:
          InstanceId:
            description: "ID of the Instance."
            type: "String" 
          AutomationAssumeRole:
            default: ""
            description: "(Optional) The ARN of the role that allows Automation to perform the actions on your behalf."
            type: "String" 
        mainSteps:
        - name: "updateOSSoftware"
          action: "aws:runCommand"
          maxAttempts: 3
          timeoutSeconds: 3600
          inputs:
            DocumentName: "AWS-RunShellScript"
            InstanceIds:
            - "{{InstanceId}}"
            CloudWatchOutputConfig:
              CloudWatchOutputEnabled: "true"
            Parameters:
              commands: 
                - |
                   #!/bin/bash
                   sudo yum update -y
                   needs-restarting -r
                   if [ $? -eq 1 ]
                   then
                           exit 194
                   else
                           exit 0
                   fi
        - name: "InstallNginx"
          action: "aws:runCommand"
          inputs:
            DocumentName: "AWS-RunShellScript"
            InstanceIds:
            - "{{InstanceId}}"
            CloudWatchOutputConfig:
              CloudWatchOutputEnabled: "true"
            Parameters:
              commands:
                - |
                    sudo amazon-linux-extras install nginx1 -y
                    sudo service nginx start
        - name: "TestInstall"
          action: "aws:runCommand"
          maxAttempts: 3
          timeoutSeconds: 3600
          onFailure: "Abort"
          inputs:
           DocumentName: "AWS-RunShellScript"
           InstanceIds:
            - "{{InstanceId}}"
           Parameters: 
            commands:
                - |
                   curl localhost
  SSMExecutionRole: 
    Type : AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - ssm:StartAssociationsOnce
                  - ssm:CreateAssociation
                  - ssm:CreateAssociationBatch
                  - ssm:UpdateAssociation
                Resource: '*'
                Effect: Allow
          PolicyName: ssm-association
      Path: /
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/service-role/AmazonSSMAutomationRole'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
        - Effect: "Allow"
          Principal:
            Service:
            - "ec2.amazonaws.com"
            - "ssm.amazonaws.com"
          Action: "sts:AssumeRole"
  SSMInstanceRole: 
    Type : AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                Resource: 
                  - !Sub 'arn:aws:s3:::aws-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*'
                  - !Sub 'arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*'
                Effect: Allow
          PolicyName: ssm-custom-s3-policy
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                  - s3:PutObject
                  - s3:PutObjectAcl
                  - s3:ListBucket
                Resource: 
                  - !Sub 'arn:${AWS::Partition}:s3:::${SSMAssocLogs}/*'
                  - !Sub 'arn:${AWS::Partition}:s3:::${SSMAssocLogs}'
                Effect: Allow
          PolicyName: s3-instance-bucket-policy
      Path: /
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore'
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/CloudWatchAgentServerPolicy'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
        - Effect: "Allow"
          Principal:
            Service:
            - "ec2.amazonaws.com"
            - "ssm.amazonaws.com"
          Action: "sts:AssumeRole"
  SSMInstanceProfile:
    Type: "AWS::IAM::InstanceProfile"
    Properties:
      Roles:
      - !Ref SSMInstanceRole
  EC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: !Ref LatestAmiId
      InstanceType: "t3.medium"
      IamInstanceProfile: !Ref SSMInstanceProfile
      Tags:
       - Key: nginx
         Value: Yes
  NginxAssociation:
    DependsOn: EC2Instance
    Type: AWS::SSM::Association
    Properties:
      Name: !Ref nginxInstallAutomation
      WaitForSuccessTimeoutSeconds: 300
      OutputLocation:
        S3Location: 
          OutputS3BucketName: !Ref SSMAssocLogs
          OutputS3KeyPrefix: 'logs/'
      AutomationTargetParameterName: InstanceId
      Parameters:
        AutomationAssumeRole:
          - !GetAtt 'SSMExecutionRole.Arn'
      Targets:
        - Key: tag:nginx
          Values:
            - Yes     
Outputs:
  WebServerPublic:
    Value: !GetAtt 'EC2Instance.PublicDnsName'
    Description: Public DNS for WebServer
```

### Create an association that joins targets to a Windows Active Directory domain<a name="aws-resource-ssm-association--examples--Create_an_association_that_joins_targets_to_a_Windows_Active_Directory_domain"></a>

The following example creates an association that joins targets to a Windows Active Directory domain by using State Manager\. Target is based on tags\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_joins_targets_to_a_Windows_Active_Directory_domain--json"></a>

```
{
  "Description": "Deploy single windows EC2 Instance and join domain with SSM Association",
  "Parameters": {
    "DomainAdminPassword": {
      "AllowedPattern": "(?=^.{6,255}$)((?=.*\\d)(?=.*[A-Z])(?=.*[a-z])|(?=.*\\d)(?=.*[^A-Za-z0-9])(?=.*[a-z])|(?=.*[^A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z])|(?=.*\\d)(?=.*[A-Z])(?=.*[^A-Za-z0-9]))^.*",
      "Description": "Password for the domain admin user. Must be at least 8 characters, containing letters, numbers, and symbols.",
      "MaxLength": "32",
      "MinLength": "8",
      "NoEcho": "true",
      "Type": "String"
    },
    "DomainAdminUser": {
      "AllowedPattern": "[a-zA-Z0-9]*",
      "Default": "Admin",
      "Description": "User name for the account that will be used as domain administrator. This is separate from the default \"Administrator\" account.",
      "MaxLength": "25",
      "MinLength": "5",
      "Type": "String"
    },
    "DomainDNSName": {
      "AllowedPattern": "[a-zA-Z0-9\\-]+\\..+",
      "Default": "example.com",
      "Description": "Fully qualified domain name (FQDN).",
      "MaxLength": "255",
      "MinLength": "2",
      "Type": "String"
    },
    "DomainMemberSGID": {
      "Description": "ID of the domain member security group (e.g., sg-7f16e910).",
      "Type": "AWS::EC2::SecurityGroup::Id"
    },
    "DomainNetBIOSName": {
      "AllowedPattern": "[a-zA-Z0-9\\-]+",
      "Default": "EXAMPLE",
      "Description": "NetBIOS name of the domain (up to 15 characters) for users of earlier versions of Windows.",
      "MaxLength": "15",
      "MinLength": "1",
      "Type": "String"
    },
    "EC2InstanceType": {
      "AllowedValues": [
        "t3.nano",
        "t3.micro",
        "t3.small",
        "t3.medium",
        "t3.large",
        "t3.xlarge",
        "t3.2xlarge",
        "m5.large",
        "m5.xlarge",
        "m5.2xlarge"
      ],
      "Default": "m5.large",
      "Description": "Amazon EC2 instance type",
      "Type": "String"
    },
    "LatestAmiId": {
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-windows-latest/Windows_Server-2019-English-Full-Base"
    },
    "SubnetID": {
      "Description": "ID of a Subnet.",
      "Type": "AWS::EC2::Subnet::Id"
    }
  },
  "Resources": {
    "DSCBucket": {
      "Type": "AWS::S3::Bucket",
      "Properties": {
        "LifecycleConfiguration": {
          "Rules": [
            {
              "Id": "DeleteAfter30Days",
              "ExpirationInDays": 30,
              "Status": "Enabled",
              "Prefix": "logs/"
            }
          ]
        }
      }
    },
    "DomainJoinSecrets": {
      "Type": "AWS::SecretsManager::Secret",
      "Properties": {
        "Name": "DomainJoinSecrets-${AWS::StackName}",
        "Description": "Secrets to join AD domain",
        "SecretString": "{\"username\":\"${DomainNetBIOSName}\\\\${DomainAdminUser}\",\"password\":\"${DomainAdminPassword}\"}"
      }
    },
    "LambdaSSMRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": [
                    "s3:PutObject"
                  ],
                  "Resource": [
                    "${DSCBucket.Arn}",
                    "${DSCBucket.Arn}/*"
                  ]
                }
              ]
            },
            "PolicyName": "write-mof-s3"
          }
        ],
        "Path": "/",
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "lambda.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        },
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/service-role/AWSLambdaBasicExecutionRole"
        ]
      }
    },
    "WriteMOFFunction": {
      "Type": "AWS::Lambda::Function",
      "Properties": {
        "Code": {
          "ZipFile": "var AWS = require('aws-sdk'), s3 = new AWS.S3(); const response = require(\"cfn-response\"); exports.handler = async (event, context) => {\n  console.log(JSON.stringify(event));\n  if (event.RequestType === 'Delete') {\n      await postResponse(event, context, response.SUCCESS, {})\n      return;\n  }\n  function postResponse(event, context, status, data){\n      return new Promise((resolve, reject) => {\n          setTimeout(() => response.send(event, context, status, data), 5000)\n      });\n  }\n  await s3.putObject({\n    Body: event.ResourceProperties.Body,\n    Bucket: event.ResourceProperties.Bucket,\n    Key: event.ResourceProperties.Key\n  }).promise();\n  await postResponse(event, context, response.SUCCESS, {});\n};\n"
        },
        "Handler": "index.handler",
        "Role": "LambdaSSMRole.Arn",
        "Runtime": "nodejs10.x",
        "Timeout": 10
      }
    },
    "WriteDomainJoinMOF": {
      "Type": "Custom::WriteMOFFile",
      "Properties": {
        "ServiceToken": "WriteMOFFunction.Arn",
        "Bucket": "DSCBucket",
        "Key": "DomainJoin-${AWS::StackName}.mof",
        "Body": "/*\n@TargetNode='localhost'\n*/\ninstance of MSFT_Credential as $MSFT_Credential1ref\n{\nPassword = \"managementgovernancesample\";\n UserName = \"${DomainJoinSecrets}\";\n\n};\ninstance of DSC_Computer as $DSC_Computer1ref\n{\nResourceID = \"[Computer]JoinDomain\";\n Credential = $MSFT_Credential1ref;\n DomainName = \"{tag:DomainToJoin}\";\n Name = \"{tag:Name}\";\n ModuleName = \"ComputerManagementDsc\";\n ModuleVersion = \"8.0.0\";\n ConfigurationName = \"DomainJoin\";\n};\ninstance of OMI_ConfigurationDocument\n                    {\n Version=\"2.0.0\";\n                        MinimumCompatibleVersion = \"1.0.0\";\n                        CompatibleVersionAdditionalProperties= {\"Omi_BaseResource:ConfigurationName\"};\n                        Name=\"DomainJoin\";\n                    };      \n"
      }
    },
    "SSMInstanceRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject"
                  ],
                  "Resource": [
                    "arn:aws:s3:::aws-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*",
                    "arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*",
                    "arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "ssm-custom-s3-policy"
          },
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": [
                    "secretsmanager:GetSecretValue",
                    "secretsmanager:DescribeSecret"
                  ],
                  "Resource": [
                    "DomainJoinSecrets"
                  ]
                }
              ]
            },
            "PolicyName": "ssm-secrets-policy"
          },
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject",
                    "s3:PutObject",
                    "s3:PutObjectAcl",
                    "s3:ListBucket"
                  ],
                  "Resource": [
                    "arn:${AWS::Partition}:s3:::${DSCBucket}/*",
                    "arn:${AWS::Partition}:s3:::${DSCBucket}"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "s3-instance-bucket-policy"
          }
        ],
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore",
          "arn:${AWS::Partition}:iam::aws:policy/AmazonEC2ReadOnlyAccess"
        ],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "ec2.amazonaws.com",
                  "ssm.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        }
      }
    },
    "SSMInstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Roles": [
          "SSMInstanceRole"
        ]
      }
    },
    "WINEC2Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "ImageId": "LatestAmiId",
        "InstanceType": "EC2InstanceType",
        "IamInstanceProfile": "SSMInstanceProfile",
        "NetworkInterfaces": [
          {
            "DeleteOnTermination": true,
            "DeviceIndex": "0",
            "SubnetId": "SubnetID",
            "GroupSet": [
              "DomainMemberSGID"
            ]
          }
        ],
        "Tags": [
          {
            "Key": "Name",
            "Value": "WindowsBox0"
          },
          {
            "Key": "DomainToJoin",
            "Value": "DomainDNSName"
          }
        ]
      }
    },
    "JoinDomainAssociation": {
      "DependsOn": [
        "WINEC2Instance",
        "WriteDomainJoinMOF"
      ],
      "Type": "AWS::SSM::Association",
      "Properties": {
        "WaitForSuccessTimeoutSeconds": 300,
        "Name": "AWS-ApplyDSCMofs",
        "Targets": [
          {
            "Key": "tag:DomainToJoin",
            "Values": [
              "DomainDNSName"
            ]
          }
        ],
        "OutputLocation": {
          "S3Location": {
            "OutputS3BucketName": "DSCBucket",
            "OutputS3KeyPrefix": "logs/"
          }
        },
        "ScheduleExpression": "cron(30 23 * * ? *)",
        "MaxErrors": 1,
        "MaxConcurrency": 1,
        "Parameters": {
          "MofsToApply": [
            "s3:${DSCBucket}:DomainJoin-${AWS::StackName}.mof"
          ],
          "ServicePath": [
            "default"
          ],
          "MofOperationMode": [
            "Apply"
          ],
          "ComplianceType": [
            "Custom:DomainJoinSample"
          ],
          "ModuleSourceBucketName": [
            "NONE"
          ],
          "AllowPSGalleryModuleSource": [
            "True"
          ],
          "RebootBehavior": [
            "AfterMof"
          ],
          "UseComputerNameForReporting": [
            "False"
          ],
          "EnableVerboseLogging": [
            "False"
          ],
          "EnableDebugLogging": [
            "False"
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_joins_targets_to_a_Windows_Active_Directory_domain--yaml"></a>

```
---
Description: "Deploy single windows EC2 Instance and join domain with SSM Association"
Parameters:
  DomainAdminPassword:
    AllowedPattern: (?=^.{6,255}$)((?=.*\d)(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[^A-Za-z0-9])(?=.*[a-z])|(?=.*[^A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[A-Z])(?=.*[^A-Za-z0-9]))^.*
    Description: Password for the domain admin user. Must be at least 8 characters,
      containing letters, numbers, and symbols.
    MaxLength: '32'
    MinLength: '8'
    NoEcho: 'true'
    Type: String
  DomainAdminUser:
    AllowedPattern: '[a-zA-Z0-9]*'
    Default: Admin
    Description: User name for the account that will be used as domain administrator. This is separate from the default "Administrator" account.
    MaxLength: '25'
    MinLength: '5'
    Type: String
  DomainDNSName:
    AllowedPattern: '[a-zA-Z0-9\-]+\..+'
    Default: example.com
    Description: Fully qualified domain name (FQDN).
    MaxLength: '255'
    MinLength: '2'
    Type: String
  DomainMemberSGID:
    Description: ID of the domain member security group (e.g., sg-7f16e910).
    Type: AWS::EC2::SecurityGroup::Id
  DomainNetBIOSName:
    AllowedPattern: '[a-zA-Z0-9\-]+'
    Default: EXAMPLE
    Description: NetBIOS name of the domain (up to 15 characters) for users of earlier
      versions of Windows.
    MaxLength: '15'
    MinLength: '1'
    Type: String
  EC2InstanceType:
    AllowedValues:
      - t3.nano
      - t3.micro
      - t3.small
      - t3.medium
      - t3.large
      - t3.xlarge
      - t3.2xlarge
      - m5.large
      - m5.xlarge
      - m5.2xlarge
    Default: m5.large
    Description: Amazon EC2 instance type
    Type: String
  LatestAmiId:
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: "/aws/service/ami-windows-latest/Windows_Server-2019-English-Full-Base"
  SubnetID:
    Description: ID of a Subnet.
    Type: AWS::EC2::Subnet::Id
Resources:
  DSCBucket:
    Type: AWS::S3::Bucket
    Properties:
      LifecycleConfiguration:
        Rules:
          - Id: DeleteAfter30Days
            ExpirationInDays: 30
            Status: Enabled
            Prefix: 'logs/'
  DomainJoinSecrets:
    Type: AWS::SecretsManager::Secret
    Properties:
      Name: !Sub 'DomainJoinSecrets-${AWS::StackName}'
      Description: Secrets to join AD domain
      SecretString: !Sub '{"username":"${DomainNetBIOSName}\\${DomainAdminUser}","password":"${DomainAdminPassword}"}'
  LambdaSSMRole:
    Type: AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
            - Effect: Allow
              Action:
              - s3:PutObject
              Resource:
                - !Sub "${DSCBucket.Arn}"
                - !Sub "${DSCBucket.Arn}/*"
          PolicyName: write-mof-s3
      Path: /
      AssumeRolePolicyDocument:
        Version: '2012-10-17'
        Statement:
          - Effect: Allow
            Principal:
              Service: 
                - lambda.amazonaws.com
            Action: sts:AssumeRole
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/service-role/AWSLambdaBasicExecutionRole'
  WriteMOFFunction:
    Type: AWS::Lambda::Function
    Properties:
      Code:
        ZipFile: >
          var AWS = require('aws-sdk'), s3 = new AWS.S3();
          const response = require("cfn-response");
          exports.handler = async (event, context) => {
            console.log(JSON.stringify(event));
            if (event.RequestType === 'Delete') {
                await postResponse(event, context, response.SUCCESS, {})
                return;
            }
            function postResponse(event, context, status, data){
                return new Promise((resolve, reject) => {
                    setTimeout(() => response.send(event, context, status, data), 5000)
                });
            }
            await s3.putObject({
              Body: event.ResourceProperties.Body,
              Bucket: event.ResourceProperties.Bucket,
              Key: event.ResourceProperties.Key
            }).promise();
            await postResponse(event, context, response.SUCCESS, {});
          };
      Handler: index.handler
      Role: !GetAtt LambdaSSMRole.Arn
      Runtime: nodejs10.x
      Timeout: 10
  WriteDomainJoinMOF:
    Type: Custom::WriteMOFFile
    Properties:
      ServiceToken: !GetAtt WriteMOFFunction.Arn
      Bucket: !Ref DSCBucket
      Key: !Sub "DomainJoin-${AWS::StackName}.mof"
      Body: !Sub |
        /*
        @TargetNode='localhost'
        */
        instance of MSFT_Credential as $MSFT_Credential1ref
        {
        Password = "managementgovernancesample";
         UserName = "${DomainJoinSecrets}";
        
        };
        instance of DSC_Computer as $DSC_Computer1ref
        {
        ResourceID = "[Computer]JoinDomain";
         Credential = $MSFT_Credential1ref;
         DomainName = "{tag:DomainToJoin}";
         Name = "{tag:Name}";
         ModuleName = "ComputerManagementDsc";
         ModuleVersion = "8.0.0";
         ConfigurationName = "DomainJoin";
        };
        instance of OMI_ConfigurationDocument
                            {
         Version="2.0.0";
                                MinimumCompatibleVersion = "1.0.0";
                                CompatibleVersionAdditionalProperties= {"Omi_BaseResource:ConfigurationName"};
                                Name="DomainJoin";
                            };      
  SSMInstanceRole: 
    Type : AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                Resource: 
                  - !Sub 'arn:aws:s3:::aws-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*'
                  - !Sub 'arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*'
                Effect: Allow
          PolicyName: ssm-custom-s3-policy
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Effect: Allow
                Action:
                  - secretsmanager:GetSecretValue
                  - secretsmanager:DescribeSecret
                Resource: 
                  - !Ref 'DomainJoinSecrets'
          PolicyName: ssm-secrets-policy
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                  - s3:PutObject
                  - s3:PutObjectAcl
                  - s3:ListBucket
                Resource: 
                  - !Sub 'arn:${AWS::Partition}:s3:::${DSCBucket}/*'
                  - !Sub 'arn:${AWS::Partition}:s3:::${DSCBucket}'
                Effect: Allow
          PolicyName: s3-instance-bucket-policy
      Path: /
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore'
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/AmazonEC2ReadOnlyAccess'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
        - Effect: "Allow"
          Principal:
            Service:
            - "ec2.amazonaws.com"
            - "ssm.amazonaws.com"
          Action: "sts:AssumeRole"
  SSMInstanceProfile:
    Type: "AWS::IAM::InstanceProfile"
    Properties:
      Roles:
      - !Ref SSMInstanceRole
  WINEC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: !Ref LatestAmiId
      InstanceType: !Ref EC2InstanceType
      IamInstanceProfile: !Ref SSMInstanceProfile
      NetworkInterfaces:
        - DeleteOnTermination: true
          DeviceIndex: '0'
          SubnetId: !Ref 'SubnetID'
          GroupSet:
            - !Ref DomainMemberSGID
      Tags:
      - Key: "Name"
        Value: "WindowsBox0"
      - Key: "DomainToJoin"
        Value: !Ref "DomainDNSName"
  JoinDomainAssociation:
    DependsOn: 
      - WINEC2Instance
      - WriteDomainJoinMOF
    Type: AWS::SSM::Association
    Properties:
      WaitForSuccessTimeoutSeconds: 300
      Name: AWS-ApplyDSCMofs
      Targets:
        - Key: "tag:DomainToJoin"
          Values:
           - !Ref "DomainDNSName"
      OutputLocation:
        S3Location: 
          OutputS3BucketName: !Ref DSCBucket
          OutputS3KeyPrefix: 'logs/'
      ScheduleExpression: "cron(30 23 * * ? *)"
      MaxErrors: 1
      MaxConcurrency: 1
      Parameters:
        MofsToApply:
          - !Sub "s3:${DSCBucket}:DomainJoin-${AWS::StackName}.mof"
        ServicePath:
          - default
        MofOperationMode:
          - Apply
        ComplianceType:
          - Custom:DomainJoinSample
        ModuleSourceBucketName:
          - "NONE"
        AllowPSGalleryModuleSource:
          - "True"
        RebootBehavior:
          - "AfterMof"
        UseComputerNameForReporting:
          - "False"
        EnableVerboseLogging:
          - "False"
        EnableDebugLogging:
          - "False"
```

### Create an association that joins targets to a Windows Active Directory domain and uses Systems Manager Automation<a name="aws-resource-ssm-association--examples--Create_an_association_that_joins_targets_to_a_Windows_Active_Directory_domain_and_uses_Systems_Manager_Automation"></a>

The following example creates an association that joins targets to a Windows Active Directory domain by using State Manager and Automation\. Target is based on tags\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_joins_targets_to_a_Windows_Active_Directory_domain_and_uses_Systems_Manager_Automation--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Deploy single windows EC2 Instance and join domain with SSM Association",
  "Parameters": {
    "DomainAdminPassword": {
      "AllowedPattern": "(?=^.{6,255}$)((?=.*\\d)(?=.*[A-Z])(?=.*[a-z])|(?=.*\\d)(?=.*[^A-Za-z0-9])(?=.*[a-z])|(?=.*[^A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z])|(?=.*\\d)(?=.*[A-Z])(?=.*[^A-Za-z0-9]))^.*",
      "Description": "Password for the domain admin user. Must be at least 8 characters, containing letters, numbers, and symbols.",
      "MaxLength": "32",
      "MinLength": "8",
      "NoEcho": "true",
      "Type": "String"
    },
    "DomainAdminUser": {
      "AllowedPattern": "[a-zA-Z0-9]*",
      "Default": "Admin",
      "Description": "User name for the account that will be used as domain administrator. This is separate from the default \"Administrator\" account.",
      "MaxLength": "25",
      "MinLength": "5",
      "Type": "String"
    },
    "DomainDNSName": {
      "AllowedPattern": "[a-zA-Z0-9\\-]+\\..+",
      "Default": "example.com",
      "Description": "Fully qualified domain name (FQDN).",
      "MaxLength": "255",
      "MinLength": "2",
      "Type": "String"
    },
    "DomainMemberSGID": {
      "Description": "ID of the domain member security group (e.g., sg-7f16e910).",
      "Type": "AWS::EC2::SecurityGroup::Id"
    },
    "DomainNetBIOSName": {
      "AllowedPattern": "[a-zA-Z0-9\\-]+",
      "Default": "EXAMPLE",
      "Description": "NetBIOS name of the domain (up to 15 characters) for users of earlier versions of Windows.",
      "MaxLength": "15",
      "MinLength": "1",
      "Type": "String"
    },
    "EC2InstanceType": {
      "AllowedValues": [
        "t3.nano",
        "t3.micro",
        "t3.small",
        "t3.medium",
        "t3.large",
        "t3.xlarge",
        "t3.2xlarge",
        "m5.large",
        "m5.xlarge",
        "m5.2xlarge"
      ],
      "Default": "m5.large",
      "Description": "Amazon EC2 instance type",
      "Type": "String"
    },
    "LatestAmiId": {
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default": "/aws/service/ami-windows-latest/Windows_Server-2019-English-Full-Base"
    },
    "SubnetID": {
      "Description": "ID of a Subnet.",
      "Type": "AWS::EC2::Subnet::Id"
    }
  },
  "Resources": {
    "DSCBucket": {
      "Type": "AWS::S3::Bucket",
      "Properties": {
        "LifecycleConfiguration": {
          "Rules": [
            {
              "Id": "DeleteAfter30Days",
              "ExpirationInDays": 30,
              "Status": "Enabled",
              "Prefix": "logs/"
            }
          ]
        }
      }
    },
    "DomainJoinSecrets": {
      "Type": "AWS::SecretsManager::Secret",
      "Properties": {
        "Name": "DomainJoinSecrets-${AWS::StackName}",
        "Description": "Secrets to join AD domain",
        "SecretString": "{\"username\":\"${DomainAdminUser}\",\"password\":\"${DomainAdminPassword}\"}"
      }
    },
    "LambdaSSMRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": [
                    "s3:PutObject"
                  ],
                  "Resource": [
                    "${DSCBucket.Arn}",
                    "${DSCBucket.Arn}/*"
                  ]
                }
              ]
            },
            "PolicyName": "write-mof-s3"
          }
        ],
        "Path": "/",
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "lambda.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        },
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/service-role/AWSLambdaBasicExecutionRole"
        ]
      }
    },
    "WriteScriptFunction": {
      "Type": "AWS::Lambda::Function",
      "Properties": {
        "Code": {
          "ZipFile": "var AWS = require('aws-sdk'), s3 = new AWS.S3(); const response = require(\"cfn-response\"); exports.handler = async (event, context) => {\n  console.log(JSON.stringify(event));\n  if (event.RequestType === 'Delete') {\n      await postResponse(event, context, response.SUCCESS, {})\n      return;\n  }\n  function postResponse(event, context, status, data){\n      return new Promise((resolve, reject) => {\n          setTimeout(() => response.send(event, context, status, data), 5000)\n      });\n  }\n  await s3.putObject({\n    Body: event.ResourceProperties.Body,\n    Bucket: event.ResourceProperties.Bucket,\n    Key: event.ResourceProperties.Key\n  }).promise();\n  await postResponse(event, context, response.SUCCESS, {});\n};\n"
        },
        "Handler": "index.handler",
        "Role": "LambdaSSMRole.Arn",
        "Runtime": "nodejs10.x",
        "Timeout": 10
      }
    },
    "WriteDomainJoinScript": {
      "Type": "Custom::WriteScript",
      "Properties": {
        "ServiceToken": "WriteScriptFunction.Arn",
        "Bucket": "DSCBucket",
        "Key": "DomainJoin.ps1",
        "Body": "[CmdletBinding()]\n# Incoming Parameters for Script, CloudFormation\\SSM Parameters being passed in\nparam(\n    [Parameter(Mandatory=$true)]\n    [string]$DomainNetBIOSName,\n\n    [Parameter(Mandatory=$true)]\n    [string]$DomainDNSName,\n\n    [Parameter(Mandatory=$true)]\n    [string]$AdminSecret\n)\n\n# Formatting AD Admin User to proper format for JoinDomain DSC Resources in this Script\n$DomainAdmin = 'Domain\\User' -replace 'Domain',$DomainNetBIOSName -replace 'User',$UserName\n$Admin = ConvertFrom-Json -InputObject (Get-SECSecretValue -SecretId $AdminSecret).SecretString\n$AdminUser = $DomainNetBIOSName + '\\' + $Admin.UserName\n# Creating Credential Object for Administrator\n$Credentials = (New-Object PSCredential($AdminUser,(ConvertTo-SecureString $Admin.Password -AsPlainText -Force)))\n# Getting the DSC Cert Encryption Thumbprint to Secure the MOF File\n$DscCertThumbprint = (get-childitem -path cert:\\LocalMachine\\My | where { $_.subject -eq \"CN=SampleDscEncryptCert\" }).Thumbprint\n# Getting the Name Tag of the Instance\n$NameTag = (Get-EC2Tag -Filter @{ Name=\"resource-id\";Values=(Invoke-RestMethod -Method Get -Uri http://169.254.169.254/latest/meta-data/instance-id)}| Where-Object { $_.Key -eq \"Name\" })\n$NewName = $NameTag.Value\n\n# Creating Configuration Data Block that has the Certificate Information for DSC Configuration Processing\n$ConfigurationData = @{\n    AllNodes = @(\n        @{\n            NodeName=\"*\"\n            CertificateFile = \"C:\\awssample\\publickeys\\SamplePublicKey.cer\"\n            Thumbprint = $DscCertThumbprint\n            PSDscAllowDomainUser = $true\n        },\n        @{\n            NodeName = 'localhost'\n        }\n    )\n}\n\nConfiguration DomainJoin {\n    param(\n        [PSCredential] $Credentials\n    )\n\n    Import-Module -Name PSDesiredStateConfiguration\n    Import-Module -Name ComputerManagementDsc\n    \n    Import-DscResource -Module PSDesiredStateConfiguration\n    Import-DscResource -Module ComputerManagementDsc\n\n    Node 'localhost' {\n\n        Computer JoinDomain {\n            Name = $NewName\n            DomainName = $DomainDNSName\n            Credential = $Credentials\n        }\n    }\n}\n\nDomainJoin -OutputPath 'C:\\awssample\\DomainJoin' -ConfigurationData $ConfigurationData -Credentials $Credentials\n"
      }
    },
    "WriteInstallModuleScript": {
      "Type": "Custom::WriteScript",
      "Properties": {
        "ServiceToken": "WriteScriptFunction.Arn",
        "Bucket": "DSCBucket",
        "Key": "install-modules.ps1",
        "Body": "[CmdletBinding()]\nparam()\n\n\"Setting up Powershell Gallery to Install DSC Modules\"\nInstall-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force\nSet-PSRepository -Name PSGallery -InstallationPolicy Trusted\n\n\"Installing the needed Powershell DSC modules for this Quick Start\"\nInstall-Module -Name ComputerManagementDsc\nInstall-Module -Name PSDscResources\n\n\"Creating Directory for DSC Public Cert\"\nNew-Item -Path C:\\awssample\\publickeys -ItemType directory -Force\n\n\"Setting up DSC Certificate to Encrypt Credentials in MOF File\"\n$cert = New-SelfSignedCertificate -Type DocumentEncryptionCertLegacyCsp -DnsName 'SampleDscEncryptCert' -HashAlgorithm SHA256\n# Exporting the public key certificate\n$cert | Export-Certificate -FilePath \"C:\\awssample\\publickeys\\SamplePublicKey.cer\" -Force\n"
      }
    },
    "WriteLCMConfigScript": {
      "Type": "Custom::WriteScript",
      "Properties": {
        "ServiceToken": "WriteScriptFunction.Arn",
        "Bucket": "DSCBucket",
        "Key": "LCM-Config.ps1",
        "Body": "# This block sets the LCM configuration to what we need for QS\n[DSCLocalConfigurationManager()]\nconfiguration LCMConfig\n{\n    Node 'localhost' {\n        Settings {\n            RefreshMode = 'Push'\n            ActionAfterReboot = 'StopConfiguration'                      \n            RebootNodeIfNeeded = $false\n            CertificateId = $DscCertThumbprint  \n        }\n    }\n}\n\n$DscCertThumbprint = [string](get-childitem -path cert:\\LocalMachine\\My | where { $_.subject -eq \"CN=SampleDscEncryptCert\" }).Thumbprint\n    \n#Generates MOF File for LCM\nLCMConfig -OutputPath 'C:\\awssample\\LCMConfig'\n    \n# Sets LCM Configuration to MOF generated in previous command\nSet-DscLocalConfigurationManager -Path 'C:\\awssample\\LCMConfig' \n"
      }
    },
    "DomainJoinAutomation": {
      "Type": "AWS::SSM::Document",
      "Properties": {
        "DocumentType": "Automation",
        "Content": {
          "schemaVersion": "0.3",
          "description": "Join a Windows Domain",
          "assumeRole": "{{AutomationAssumeRole}}",
          "parameters": {
            "InstanceId": {
              "description": "ID of the Instance.",
              "type": "StringList"
            },
            "DomainDNSName": {
              "default": "example.com",
              "description": "Fully qualified domain name (FQDN) of the forest root domain e.g. example.com",
              "type": "String"
            },
            "DomainNetBIOSName": {
              "default": "example",
              "description": "NetBIOS name of the domain (up to 15 characters) for users of earlier versions of Windows e.g. EXAMPLE",
              "type": "String"
            },
            "AdminSecrets": {
              "description": "AWS Secrets Parameter Name that has Password and User name for a domain administrator.",
              "type": "String"
            },
            "S3BucketName": {
              "description": "S3 bucket name for the Quick Start assets. Quick Start bucket name can include numbers, lowercase letters, uppercase letters, and hyphens (-). It cannot start or end with a hyphen (-).",
              "type": "String"
            },
            "AutomationAssumeRole": {
              "default": "",
              "description": "(Optional) The ARN of the role that allows Automation to perform the actions on your behalf.",
              "type": "String"
            }
          },
          "mainSteps": [
            {
              "name": "InstallDSCModules",
              "action": "aws:runCommand",
              "inputs": {
                "DocumentName": "AWS-RunRemoteScript",
                "InstanceIds": [
                  "{{InstanceId}}"
                ],
                "CloudWatchOutputConfig": {
                  "CloudWatchOutputEnabled": "true",
                  "CloudWatchLogGroupName": "/ssm/${AWS::StackName}"
                },
                "Parameters": {
                  "sourceType": "S3",
                  "sourceInfo": "{\"path\": \"https://{{S3BucketName}}.s3.amazonaws.com/install-modules.ps1\"}",
                  "commandLine": "./install-modules.ps1"
                }
              }
            },
            {
              "name": "ConfigureLCM",
              "action": "aws:runCommand",
              "inputs": {
                "DocumentName": "AWS-RunRemoteScript",
                "InstanceIds": [
                  "{{InstanceId}}"
                ],
                "CloudWatchOutputConfig": {
                  "CloudWatchOutputEnabled": "true",
                  "CloudWatchLogGroupName": "/ssm/${AWS::StackName}"
                },
                "Parameters": {
                  "sourceType": "S3",
                  "sourceInfo": "{\"path\": \"https://{{S3BucketName}}.s3.amazonaws.com/LCM-Config.ps1\"}",
                  "commandLine": "./LCM-Config.ps1"
                }
              }
            },
            {
              "name": "GenerateDomainJoinMof",
              "action": "aws:runCommand",
              "inputs": {
                "DocumentName": "AWS-RunRemoteScript",
                "InstanceIds": [
                  "{{InstanceId}}"
                ],
                "CloudWatchOutputConfig": {
                  "CloudWatchOutputEnabled": "true",
                  "CloudWatchLogGroupName": "/ssm/${AWS::StackName}"
                },
                "Parameters": {
                  "sourceType": "S3",
                  "sourceInfo": "{\"path\": \"https://{{S3BucketName}}.s3.amazonaws.com/DomainJoin.ps1\"}",
                  "commandLine": "./DomainJoin.ps1 -DomainNetBIOSName {{DomainNetBIOSName}} -DomainDNSName {{DomainDNSName}} -AdminSecret {{AdminSecrets}}"
                }
              }
            },
            {
              "name": "DomainJoin",
              "action": "aws:runCommand",
              "inputs": {
                "DocumentName": "AWS-RunPowerShellScript",
                "InstanceIds": [
                  "{{InstanceId}}"
                ],
                "CloudWatchOutputConfig": {
                  "CloudWatchOutputEnabled": "true",
                  "CloudWatchLogGroupName": "/ssm/${AWS::StackName}"
                },
                "Parameters": {
                  "commands": [
                    "function DscStatusCheck () {\n    $LCMState = (Get-DscLocalConfigurationManager).LCMState\n    if ($LCMState -eq 'PendingConfiguration' -Or $LCMState -eq 'PendingReboot') {\n        'returning 3010, should continue after reboot'\n        exit 3010\n    } else {\n      'Completed'\n    }\n}\n\nStart-DscConfiguration 'C:\\awssample\\DomainJoin' -Wait -Verbose -Force\n\nDscStatusCheck\n"
                  ]
                }
              }
            }
          ]
        }
      }
    },
    "SSMExecutionRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "ssm:StartAssociationsOnce",
                    "ssm:CreateAssociation",
                    "ssm:CreateAssociationBatch",
                    "ssm:UpdateAssociation"
                  ],
                  "Resource": "*",
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "ssm-association"
          }
        ],
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/service-role/AmazonSSMAutomationRole"
        ],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "ec2.amazonaws.com",
                  "ssm.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        }
      }
    },
    "SSMInstanceRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "Policies": [
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject"
                  ],
                  "Resource": [
                    "arn:aws:s3:::aws-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-${AWS::Region}/*",
                    "arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*",
                    "arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*",
                    "arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "ssm-custom-s3-policy"
          },
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": [
                    "secretsmanager:GetSecretValue",
                    "secretsmanager:DescribeSecret"
                  ],
                  "Resource": [
                    "DomainJoinSecrets"
                  ]
                }
              ]
            },
            "PolicyName": "ssm-secrets-policy"
          },
          {
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "s3:GetObject",
                    "s3:PutObject",
                    "s3:PutObjectAcl",
                    "s3:ListBucket"
                  ],
                  "Resource": [
                    "arn:${AWS::Partition}:s3:::${DSCBucket}/*",
                    "arn:${AWS::Partition}:s3:::${DSCBucket}"
                  ],
                  "Effect": "Allow"
                }
              ]
            },
            "PolicyName": "s3-instance-bucket-policy"
          }
        ],
        "Path": "/",
        "ManagedPolicyArns": [
          "arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore",
          "arn:${AWS::Partition}:iam::aws:policy/CloudWatchAgentServerPolicy"
        ],
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "ec2.amazonaws.com",
                  "ssm.amazonaws.com"
                ]
              },
              "Action": "sts:AssumeRole"
            }
          ]
        }
      }
    },
    "SSMInstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Roles": [
          "SSMInstanceRole"
        ]
      }
    },
    "WINEC2Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "ImageId": "LatestAmiId",
        "InstanceType": "EC2InstanceType",
        "IamInstanceProfile": "SSMInstanceProfile",
        "NetworkInterfaces": [
          {
            "DeleteOnTermination": true,
            "DeviceIndex": "0",
            "SubnetId": "SubnetID",
            "GroupSet": [
              "DomainMemberSGID"
            ]
          }
        ],
        "Tags": [
          {
            "Key": "Name",
            "Value": "WindowsBox1"
          }
        ]
      }
    },
    "DomainAssociation": {
      "Type": "AWS::SSM::Association",
      "Properties": {
        "AssociationName": "DomainJoin",
        "Name": "DomainJoinAutomation",
        "WaitForSuccessTimeoutSeconds": 600,
        "AutomationTargetParameterName": "InstanceId",
        "Targets": [
          {
            "Key": "ParameterValues",
            "Values": [
              "WINEC2Instance"
            ]
          }
        ],
        "OutputLocation": {
          "S3Location": {
            "OutputS3BucketName": "DSCBucket",
            "OutputS3KeyPrefix": "logs/"
          }
        },
        "Parameters": {
          "DomainDNSName": [
            "DomainDNSName"
          ],
          "DomainNetBIOSName": [
            "DomainNetBIOSName"
          ],
          "AdminSecrets": [
            "DomainJoinSecrets"
          ],
          "S3BucketName": [
            "DSCBucket"
          ],
          "AutomationAssumeRole": [
            "SSMExecutionRole.Arn"
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_joins_targets_to_a_Windows_Active_Directory_domain_and_uses_Systems_Manager_Automation--yaml"></a>

```
---
Description: "Deploy single windows EC2 Instance and join domain with SSM Association"
Parameters:
  DomainAdminPassword:
    AllowedPattern: (?=^.{6,255}$)((?=.*\d)(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[^A-Za-z0-9])(?=.*[a-z])|(?=.*[^A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[A-Z])(?=.*[^A-Za-z0-9]))^.*
    Description: Password for the domain admin user. Must be at least 8 characters,
      containing letters, numbers, and symbols.
    MaxLength: '32'
    MinLength: '8'
    NoEcho: 'true'
    Type: String
  DomainAdminUser:
    AllowedPattern: '[a-zA-Z0-9]*'
    Default: Admin
    Description: User name for the account that will be used as domain administrator. This is separate from the default "Administrator" account.
    MaxLength: '25'
    MinLength: '5'
    Type: String
  DomainDNSName:
    AllowedPattern: '[a-zA-Z0-9\-]+\..+'
    Default: example.com
    Description: Fully qualified domain name (FQDN).
    MaxLength: '255'
    MinLength: '2'
    Type: String
  DomainMemberSGID:
    Description: ID of the domain member security group (e.g., sg-7f16e910).
    Type: AWS::EC2::SecurityGroup::Id
  DomainNetBIOSName:
    AllowedPattern: '[a-zA-Z0-9\-]+'
    Default: EXAMPLE
    Description: NetBIOS name of the domain (up to 15 characters) for users of earlier
      versions of Windows.
    MaxLength: '15'
    MinLength: '1'
    Type: String
  EC2InstanceType:
    AllowedValues:
      - t3.nano
      - t3.micro
      - t3.small
      - t3.medium
      - t3.large
      - t3.xlarge
      - t3.2xlarge
      - m5.large
      - m5.xlarge
      - m5.2xlarge
    Default: m5.large
    Description: Amazon EC2 instance type
    Type: String
  LatestAmiId:
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: "/aws/service/ami-windows-latest/Windows_Server-2019-English-Full-Base"
  SubnetID:
    Description: ID of a Subnet.
    Type: AWS::EC2::Subnet::Id
Resources:
  DSCBucket:
    Type: AWS::S3::Bucket
    Properties:
      LifecycleConfiguration:
        Rules:
          - Id: DeleteAfter30Days
            ExpirationInDays: 30
            Status: Enabled
            Prefix: 'logs/'
  DomainJoinSecrets:
    Type: AWS::SecretsManager::Secret
    Properties:
      Name: !Sub 'DomainJoinSecrets-${AWS::StackName}'
      Description: Secrets to join AD domain
      SecretString: !Sub '{"username":"${DomainAdminUser}","password":"${DomainAdminPassword}"}'
  LambdaSSMRole:
    Type: AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
            - Effect: Allow
              Action:
              - s3:PutObject
              Resource:
                - !Sub "${DSCBucket.Arn}"
                - !Sub "${DSCBucket.Arn}/*"
          PolicyName: write-mof-s3
      Path: /
      AssumeRolePolicyDocument:
        Version: '2012-10-17'
        Statement:
          - Effect: Allow
            Principal:
              Service: 
                - lambda.amazonaws.com
            Action: sts:AssumeRole
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/service-role/AWSLambdaBasicExecutionRole'
  WriteScriptFunction:
    Type: AWS::Lambda::Function
    Properties:
      Code:
        ZipFile: >
          var AWS = require('aws-sdk'), s3 = new AWS.S3();
          const response = require("cfn-response");
          exports.handler = async (event, context) => {
            console.log(JSON.stringify(event));
            if (event.RequestType === 'Delete') {
                await postResponse(event, context, response.SUCCESS, {})
                return;
            }
            function postResponse(event, context, status, data){
                return new Promise((resolve, reject) => {
                    setTimeout(() => response.send(event, context, status, data), 5000)
                });
            }
            await s3.putObject({
              Body: event.ResourceProperties.Body,
              Bucket: event.ResourceProperties.Bucket,
              Key: event.ResourceProperties.Key
            }).promise();
            await postResponse(event, context, response.SUCCESS, {});
          };
      Handler: index.handler
      Role: !GetAtt LambdaSSMRole.Arn
      Runtime: nodejs10.x
      Timeout: 10
  WriteDomainJoinScript:
    Type: Custom::WriteScript
    Properties:
      ServiceToken: !GetAtt WriteScriptFunction.Arn
      Bucket: !Ref DSCBucket
      Key: "DomainJoin.ps1"
      Body: |
        [CmdletBinding()]
        # Incoming Parameters for Script, CloudFormation\SSM Parameters being passed in
        param(
            [Parameter(Mandatory=$true)]
            [string]$DomainNetBIOSName,
        
            [Parameter(Mandatory=$true)]
            [string]$DomainDNSName,
        
            [Parameter(Mandatory=$true)]
            [string]$AdminSecret
        )
        
        # Formatting AD Admin User to proper format for JoinDomain DSC Resources in this Script
        $DomainAdmin = 'Domain\User' -replace 'Domain',$DomainNetBIOSName -replace 'User',$UserName
        $Admin = ConvertFrom-Json -InputObject (Get-SECSecretValue -SecretId $AdminSecret).SecretString
        $AdminUser = $DomainNetBIOSName + '\' + $Admin.UserName
        # Creating Credential Object for Administrator
        $Credentials = (New-Object PSCredential($AdminUser,(ConvertTo-SecureString $Admin.Password -AsPlainText -Force)))
        # Getting the DSC Cert Encryption Thumbprint to Secure the MOF File
        $DscCertThumbprint = (get-childitem -path cert:\LocalMachine\My | where { $_.subject -eq "CN=SampleDscEncryptCert" }).Thumbprint
        # Getting the Name Tag of the Instance
        $NameTag = (Get-EC2Tag -Filter @{ Name="resource-id";Values=(Invoke-RestMethod -Method Get -Uri http://169.254.169.254/latest/meta-data/instance-id)}| Where-Object { $_.Key -eq "Name" })
        $NewName = $NameTag.Value
        
        # Creating Configuration Data Block that has the Certificate Information for DSC Configuration Processing
        $ConfigurationData = @{
            AllNodes = @(
                @{
                    NodeName="*"
                    CertificateFile = "C:\awssample\publickeys\SamplePublicKey.cer"
                    Thumbprint = $DscCertThumbprint
                    PSDscAllowDomainUser = $true
                },
                @{
                    NodeName = 'localhost'
                }
            )
        }
        
        Configuration DomainJoin {
            param(
                [PSCredential] $Credentials
            )
        
            Import-Module -Name PSDesiredStateConfiguration
            Import-Module -Name ComputerManagementDsc
            
            Import-DscResource -Module PSDesiredStateConfiguration
            Import-DscResource -Module ComputerManagementDsc
        
            Node 'localhost' {
        
                Computer JoinDomain {
                    Name = $NewName
                    DomainName = $DomainDNSName
                    Credential = $Credentials
                }
            }
        }
        
        DomainJoin -OutputPath 'C:\awssample\DomainJoin' -ConfigurationData $ConfigurationData -Credentials $Credentials
  WriteInstallModuleScript:
    Type: Custom::WriteScript
    Properties:
      ServiceToken: !GetAtt WriteScriptFunction.Arn
      Bucket: !Ref DSCBucket
      Key: "install-modules.ps1"
      Body: |
        [CmdletBinding()]
        param()
        
        "Setting up Powershell Gallery to Install DSC Modules"
        Install-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force
        Set-PSRepository -Name PSGallery -InstallationPolicy Trusted
        
        "Installing the needed Powershell DSC modules for this Quick Start"
        Install-Module -Name ComputerManagementDsc
        Install-Module -Name PSDscResources
        
        "Creating Directory for DSC Public Cert"
        New-Item -Path C:\awssample\publickeys -ItemType directory -Force
        
        "Setting up DSC Certificate to Encrypt Credentials in MOF File"
        $cert = New-SelfSignedCertificate -Type DocumentEncryptionCertLegacyCsp -DnsName 'SampleDscEncryptCert' -HashAlgorithm SHA256
        # Exporting the public key certificate
        $cert | Export-Certificate -FilePath "C:\awssample\publickeys\SamplePublicKey.cer" -Force
  WriteLCMConfigScript:
    Type: Custom::WriteScript
    Properties:
      ServiceToken: !GetAtt WriteScriptFunction.Arn
      Bucket: !Ref DSCBucket
      Key: "LCM-Config.ps1"
      Body: |
        # This block sets the LCM configuration to what we need for QS
        [DSCLocalConfigurationManager()]
        configuration LCMConfig
        {
            Node 'localhost' {
                Settings {
                    RefreshMode = 'Push'
                    ActionAfterReboot = 'StopConfiguration'                      
                    RebootNodeIfNeeded = $false
                    CertificateId = $DscCertThumbprint  
                }
            }
        }
        
        $DscCertThumbprint = [string](get-childitem -path cert:\LocalMachine\My | where { $_.subject -eq "CN=SampleDscEncryptCert" }).Thumbprint
            
        #Generates MOF File for LCM
        LCMConfig -OutputPath 'C:\awssample\LCMConfig'
            
        # Sets LCM Configuration to MOF generated in previous command
        Set-DscLocalConfigurationManager -Path 'C:\awssample\LCMConfig' 
  DomainJoinAutomation:
    Type: AWS::SSM::Document
    Properties:
      DocumentType: Automation
      Content:
          schemaVersion: "0.3"
          description: "Join a Windows Domain"
          # Role that is utilized to perform the steps within the Automation Document.
          assumeRole: "{{AutomationAssumeRole}}"
          # Gathering parameters needed to configure DCs in the Quick Start
          parameters:
            InstanceId:
              description: "ID of the Instance."
              type: "StringList" 
            DomainDNSName: 
              default: "example.com"
              description: "Fully qualified domain name (FQDN) of the forest root domain e.g. example.com"
              type: "String"
            DomainNetBIOSName: 
              default: "example"
              description: "NetBIOS name of the domain (up to 15 characters) for users of earlier versions of Windows e.g. EXAMPLE"
              type: "String"
            AdminSecrets:
              description: "AWS Secrets Parameter Name that has Password and User name for a domain administrator."
              type: "String"
            S3BucketName:
              description: "S3 bucket name for the Quick Start assets. Quick Start bucket name can include numbers, lowercase letters, uppercase letters, and hyphens (-). It cannot start or end with a hyphen (-)."
              type: "String"
            AutomationAssumeRole:
                default: ""
                description: "(Optional) The ARN of the role that allows Automation to perform the actions on your behalf."
                type: "String" 
          mainSteps:
          # This step Demonstrates how to run a local script on an Instance. It can be defined or pointed to a local script. 
          - name: "InstallDSCModules"
            action: "aws:runCommand"
            inputs:
              DocumentName: "AWS-RunRemoteScript"
              InstanceIds:
              - "{{InstanceId}}"
              CloudWatchOutputConfig:
                CloudWatchOutputEnabled: "true"
                CloudWatchLogGroupName:  !Sub '/ssm/${AWS::StackName}'
              Parameters:
                sourceType: "S3"
                sourceInfo: '{"path": "https://{{S3BucketName}}.s3.amazonaws.com/install-modules.ps1"}'
                commandLine: "./install-modules.ps1"
          - name: "ConfigureLCM"
            action: "aws:runCommand"
            inputs:
              DocumentName: "AWS-RunRemoteScript"
              InstanceIds:
              - "{{InstanceId}}"
              CloudWatchOutputConfig:
                CloudWatchOutputEnabled: "true"
                CloudWatchLogGroupName: !Sub '/ssm/${AWS::StackName}'
              Parameters:
                sourceType: "S3"
                sourceInfo: '{"path": "https://{{S3BucketName}}.s3.amazonaws.com/LCM-Config.ps1"}'
                commandLine: "./LCM-Config.ps1"
          - name: "GenerateDomainJoinMof"
            action: "aws:runCommand"
            inputs:
              DocumentName: "AWS-RunRemoteScript"
              InstanceIds:
                - "{{InstanceId}}"
              CloudWatchOutputConfig:
                CloudWatchOutputEnabled: "true"
                CloudWatchLogGroupName: !Sub '/ssm/${AWS::StackName}'
              Parameters:
                sourceType: "S3"
                sourceInfo: '{"path": "https://{{S3BucketName}}.s3.amazonaws.com/DomainJoin.ps1"}'
                commandLine: "./DomainJoin.ps1 -DomainNetBIOSName {{DomainNetBIOSName}} -DomainDNSName {{DomainDNSName}} -AdminSecret {{AdminSecrets}}"
          - name: "DomainJoin"
            action: aws:runCommand
            inputs:
              DocumentName: AWS-RunPowerShellScript
              InstanceIds: 
                - "{{InstanceId}}"
              CloudWatchOutputConfig:
                CloudWatchOutputEnabled: "true"
                CloudWatchLogGroupName: !Sub '/ssm/${AWS::StackName}'
              Parameters:
                commands: 
                  - |     
                     function DscStatusCheck () {
                         $LCMState = (Get-DscLocalConfigurationManager).LCMState
                         if ($LCMState -eq 'PendingConfiguration' -Or $LCMState -eq 'PendingReboot') {
                             'returning 3010, should continue after reboot'
                             exit 3010
                         } else {
                           'Completed'
                         }
                     }
                     
                     Start-DscConfiguration 'C:\awssample\DomainJoin' -Wait -Verbose -Force
                     
                     DscStatusCheck
  SSMExecutionRole: 
    Type : AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - ssm:StartAssociationsOnce
                  - ssm:CreateAssociation
                  - ssm:CreateAssociationBatch
                  - ssm:UpdateAssociation
                Resource: '*'
                Effect: Allow
          PolicyName: ssm-association
      Path: /
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/service-role/AmazonSSMAutomationRole'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
        - Effect: "Allow"
          Principal:
            Service:
            - "ec2.amazonaws.com"
            - "ssm.amazonaws.com"
          Action: "sts:AssumeRole"
  SSMInstanceRole: 
    Type : AWS::IAM::Role
    Properties:
      Policies:
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                Resource: 
                  - !Sub 'arn:aws:s3:::aws-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::aws-windows-downloads-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::amazon-ssm-packages-${AWS::Region}/*'
                  - !Sub 'arn:aws:s3:::${AWS::Region}-birdwatcher-prod/*'
                  - !Sub 'arn:aws:s3:::patch-baseline-snapshot-${AWS::Region}/*'
                Effect: Allow
          PolicyName: ssm-custom-s3-policy
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Effect: Allow
                Action:
                  - secretsmanager:GetSecretValue
                  - secretsmanager:DescribeSecret
                Resource: 
                  - !Ref 'DomainJoinSecrets'
          PolicyName: ssm-secrets-policy
        - PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                  - s3:GetObject
                  - s3:PutObject
                  - s3:PutObjectAcl
                  - s3:ListBucket
                Resource: 
                  - !Sub 'arn:${AWS::Partition}:s3:::${DSCBucket}/*'
                  - !Sub 'arn:${AWS::Partition}:s3:::${DSCBucket}'
                Effect: Allow
          PolicyName: s3-instance-bucket-policy
      Path: /
      ManagedPolicyArns:
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/AmazonSSMManagedInstanceCore'
        - !Sub 'arn:${AWS::Partition}:iam::aws:policy/CloudWatchAgentServerPolicy'
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
        - Effect: "Allow"
          Principal:
            Service:
            - "ec2.amazonaws.com"
            - "ssm.amazonaws.com"
          Action: "sts:AssumeRole"
  SSMInstanceProfile:
    Type: "AWS::IAM::InstanceProfile"
    Properties:
      Roles:
      - !Ref SSMInstanceRole
  WINEC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: !Ref LatestAmiId
      InstanceType: !Ref EC2InstanceType
      IamInstanceProfile: !Ref SSMInstanceProfile
      NetworkInterfaces:
        - DeleteOnTermination: true
          DeviceIndex: '0'
          SubnetId: !Ref 'SubnetID'
          GroupSet:
            - !Ref DomainMemberSGID
      Tags:
      - Key: "Name"
        Value: "WindowsBox1"
  DomainAssociation:
    Type: AWS::SSM::Association
    Properties:
      AssociationName: DomainJoin
      # We are using the AWS-ApplyDSCMofs Document
      Name: !Ref DomainJoinAutomation
      WaitForSuccessTimeoutSeconds: 600
      AutomationTargetParameterName: InstanceId
      Targets:
        - Key: ParameterValues
          Values:
            - !Ref WINEC2Instance
      OutputLocation:
        S3Location: 
          OutputS3BucketName: !Ref DSCBucket
          OutputS3KeyPrefix: 'logs/'
      Parameters:
        DomainDNSName: 
          - !Ref DomainDNSName
        DomainNetBIOSName: 
          - !Ref DomainNetBIOSName
        AdminSecrets:
          - !Ref DomainJoinSecrets
        S3BucketName:
          - !Ref DSCBucket
        AutomationAssumeRole:
          - !GetAtt 'SSMExecutionRole.Arn'
```

## See also<a name="aws-resource-ssm-association--seealso"></a>
+  [Reference: Cron and Rate Expressions for Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/reference-cron-and-rate-expressions.html) 