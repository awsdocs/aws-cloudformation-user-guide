# AWS::SSM::Association<a name="aws-resource-ssm-association"></a>

The `AWS::SSM::Association` resource associates an SSM document in AWS Systems Manager with managed instances that contain a configuration agent to process the document\.

## Syntax<a name="aws-resource-ssm-association-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-association-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Association",
  "Properties" : {
      "[AssociationName](#cfn-ssm-association-associationname)" : String,
      "[AutomationTargetParameterName](#cfn-ssm-association-automationtargetparametername)" : String,
      "[ComplianceSeverity](#cfn-ssm-association-complianceseverity)" : String,
      "[DocumentVersion](#cfn-ssm-association-documentversion)" : String,
      "[InstanceId](#cfn-ssm-association-instanceid)" : String,
      "[MaxConcurrency](#cfn-ssm-association-maxconcurrency)" : String,
      "[MaxErrors](#cfn-ssm-association-maxerrors)" : String,
      "[Name](#cfn-ssm-association-name)" : String,
      "[OutputLocation](#cfn-ssm-association-outputlocation)" : [InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md),
      "[Parameters](#cfn-ssm-association-parameters)" : {Key : Value, ...},
      "[ScheduleExpression](#cfn-ssm-association-scheduleexpression)" : String,
      "[SyncCompliance](#cfn-ssm-association-synccompliance)" : String,
      "[Targets](#cfn-ssm-association-targets)" : [ [Target](aws-properties-ssm-association-target.md), ... ],
      "[WaitForSuccessTimeoutSeconds](#cfn-ssm-association-waitforsuccesstimeoutseconds)" : Integer
    }
}
```

### YAML<a name="aws-resource-ssm-association-syntax.yaml"></a>

```
Type: AWS::SSM::Association
Properties: 
  [AssociationName](#cfn-ssm-association-associationname): String
  [AutomationTargetParameterName](#cfn-ssm-association-automationtargetparametername): String
  [ComplianceSeverity](#cfn-ssm-association-complianceseverity): String
  [DocumentVersion](#cfn-ssm-association-documentversion): String
  [InstanceId](#cfn-ssm-association-instanceid): String
  [MaxConcurrency](#cfn-ssm-association-maxconcurrency): String
  [MaxErrors](#cfn-ssm-association-maxerrors): String
  [Name](#cfn-ssm-association-name): String
  [OutputLocation](#cfn-ssm-association-outputlocation): 
    [InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md)
  [Parameters](#cfn-ssm-association-parameters): 
    Key : Value
  [ScheduleExpression](#cfn-ssm-association-scheduleexpression): String
  [SyncCompliance](#cfn-ssm-association-synccompliance): String
  [Targets](#cfn-ssm-association-targets): 
    - [Target](aws-properties-ssm-association-target.md)
  [WaitForSuccessTimeoutSeconds](#cfn-ssm-association-waitforsuccesstimeoutseconds): Integer
```

## Properties<a name="aws-resource-ssm-association-properties"></a>

`AssociationName`  <a name="cfn-ssm-association-associationname"></a>
The name of the association\.  
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
*Allowed Values*: `CRITICAL | HIGH | LOW | MEDIUM | UNSPECIFIED`  
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
The name of the Systems Manager document\.  
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
*Allowed Values*: `AUTO | MANUAL`  
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

## Return Values<a name="aws-resource-ssm-association-return-values"></a>

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
          ],
        "WaitForSuccessTimeoutSeconds": 300
        }
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

### Create an association for all managed instances in your AWS account<a name="aws-resource-ssm-association--examples--Create_an_association_for_all_managed_instances_in_your_AWS_account"></a>

The following example creates an association that uses the AWS\-UpdateSSMAgent SSM document\. The association updates SSM Agent on all managed instances \(instances configured for Systems Manager\) in the user's AWS account according to the specified CRON schedule\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_for_all_managed_instances_in_your_AWS_account--json"></a>

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
            ],
        "WaitForSuccessTimeoutSeconds": 300
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_for_all_managed_instances_in_your_AWS_account--yaml"></a>

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

### Associate an automation document with an instance<a name="aws-resource-ssm-association--examples--Associate_an_automation_document_with_an_instance"></a>

The following example creates an association that assigns the AWS\-StopEC2Instance automation document to a specific instance\. 

**Note**  
This example specifies the following Amazon Resource Name \(ARN\): `arn:${AWS::Partition}:iam::aws:policy/AmazonEC2FullAccess`\. This policy provides more than the required permissions to stop the instance\. We recommend that you use a policy with more restrictive permissions\.

#### JSON<a name="aws-resource-ssm-association--examples--Associate_an_automation_document_with_an_instance--json"></a>

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

#### YAML<a name="aws-resource-ssm-association--examples--Associate_an_automation_document_with_an_instance--yaml"></a>

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

### Create an association that uses rate controls and logs output to Amazon S3<a name="aws-resource-ssm-association--examples--Create_an_association_that_uses_rate_controls_and_logs_output_to_Amazon_S3"></a>

The following example creates an association that uses rate controls\. The association attempts to update SSM Agent on only 20% of instances at one time\. Systems Manager stops the association from running on any additional instances if the execution fails on 5% of the total number of instances\. System Manager also logs the association output to Amazon S3\.

#### JSON<a name="aws-resource-ssm-association--examples--Create_an_association_that_uses_rate_controls_and_logs_output_to_Amazon_S3--json"></a>

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

#### YAML<a name="aws-resource-ssm-association--examples--Create_an_association_that_uses_rate_controls_and_logs_output_to_Amazon_S3--yaml"></a>

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

## See Also<a name="aws-resource-ssm-association--seealso"></a>
+  [Reference: Cron and Rate Expressions for Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/reference-cron-and-rate-expressions.html) 