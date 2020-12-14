# AWS::Glue::Trigger<a name="aws-resource-glue-trigger"></a>

The `AWS::Glue::Trigger` resource specifies triggers that run AWS Glue jobs\. For more information, see [Triggering Jobs in AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/trigger-job.html) and [Trigger Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Trigger) in the *AWS Glue Developer Guide*\. 

## Syntax<a name="aws-resource-glue-trigger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-trigger-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Trigger",
  "Properties" : {
      "[Actions](#cfn-glue-trigger-actions)" : [ Action, ... ],
      "[Description](#cfn-glue-trigger-description)" : String,
      "[Name](#cfn-glue-trigger-name)" : String,
      "[Predicate](#cfn-glue-trigger-predicate)" : Predicate,
      "[Schedule](#cfn-glue-trigger-schedule)" : String,
      "[StartOnCreation](#cfn-glue-trigger-startoncreation)" : Boolean,
      "[Tags](#cfn-glue-trigger-tags)" : Json,
      "[Type](#cfn-glue-trigger-type)" : String,
      "[WorkflowName](#cfn-glue-trigger-workflowname)" : String
    }
}
```

### YAML<a name="aws-resource-glue-trigger-syntax.yaml"></a>

```
Type: AWS::Glue::Trigger
Properties: 
  [Actions](#cfn-glue-trigger-actions): 
    - Action
  [Description](#cfn-glue-trigger-description): String
  [Name](#cfn-glue-trigger-name): String
  [Predicate](#cfn-glue-trigger-predicate): 
    Predicate
  [Schedule](#cfn-glue-trigger-schedule): String
  [StartOnCreation](#cfn-glue-trigger-startoncreation): Boolean
  [Tags](#cfn-glue-trigger-tags): Json
  [Type](#cfn-glue-trigger-type): String
  [WorkflowName](#cfn-glue-trigger-workflowname): String
```

## Properties<a name="aws-resource-glue-trigger-properties"></a>

`Actions`  <a name="cfn-glue-trigger-actions"></a>
The actions initiated by this trigger\.  
*Required*: Yes  
*Type*: List of [Action](aws-properties-glue-trigger-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-glue-trigger-description"></a>
A description of this trigger\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-trigger-name"></a>
The name of the trigger\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Predicate`  <a name="cfn-glue-trigger-predicate"></a>
The predicate of this trigger, which defines when it will fire\.  
*Required*: No  
*Type*: [Predicate](aws-properties-glue-trigger-predicate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-glue-trigger-schedule"></a>
A `cron` expression used to specify the schedule\. For more information, see [Time\-Based Schedules for Jobs and Crawlers](https://docs.aws.amazon.com/glue/latest/dg/monitor-data-warehouse-schedule.html) in the *AWS Glue Developer Guide*\. For example, to run something every day at 12:15 UTC, specify `cron(15 12 * * ? *)`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartOnCreation`  <a name="cfn-glue-trigger-startoncreation"></a>
Set to true to start `SCHEDULED` and `CONDITIONAL` triggers when created\. True is not supported for `ON_DEMAND` triggers\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-glue-trigger-tags"></a>
The tags to use with this trigger\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-glue-trigger-type"></a>
The type of trigger that this is\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkflowName`  <a name="cfn-glue-trigger-workflowname"></a>
The name of the workflow associated with the trigger\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-glue-trigger-return-values"></a>

### Ref<a name="aws-resource-glue-trigger-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the trigger name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-glue-trigger--examples"></a>



### On\-Demand Trigger<a name="aws-resource-glue-trigger--examples--On-Demand_Trigger"></a>

The following example creates an on\-demand trigger that triggers one job\.

#### JSON<a name="aws-resource-glue-trigger--examples--On-Demand_Trigger--json"></a>

```
{
  "Resources": {
    "OnDemandJobTrigger": {
      "Type": "AWS::Glue::Trigger",
      "Properties": {
        "Type": "ON_DEMAND",
        "Description": "DESCRIPTION_ON_DEMAND",
        "Actions": [
          {
            "JobName": "prod-job2"
          }
        ],
        "Name": "prod-trigger1-ondemand"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-glue-trigger--examples--On-Demand_Trigger--yaml"></a>

```
Resources:
  OnDemandJobTrigger:
    Type: AWS::Glue::Trigger
    Properties:
      Type: ON_DEMAND
      Description: DESCRIPTION_ON_DEMAND
      Actions:
        - JobName: prod-job2
      Name: prod-trigger1-ondemand
```

### Scheduled Trigger<a name="aws-resource-glue-trigger--examples--Scheduled_Trigger"></a>

The following example creates a scheduled trigger that runs every two hours and triggers two jobs\. Note that it declares an argument for `prod-job3`\.

#### JSON<a name="aws-resource-glue-trigger--examples--Scheduled_Trigger--json"></a>

```
{
  "Resources": {
    "ScheduledJobTrigger": {
      "Type": "AWS::Glue::Trigger",
      "Properties": {
        "Type": "SCHEDULED",
        "Description": "DESCRIPTION_SCHEDULED",
        "Schedule": "cron(0 */2 * * ? *)",
        "Actions": [
          {
            "JobName": "prod-job2"
          },
          {
            "JobName": "prod-job3",
            "Arguments": {
              "--job-bookmark-option": "job-bookmark-enable"
            }
          }
        ],
        "Name": "prod-trigger1-scheduled"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-glue-trigger--examples--Scheduled_Trigger--yaml"></a>

```
Resources:
  ScheduledJobTrigger:
    Type: AWS::Glue::Trigger
    Properties:
      Type: SCHEDULED
      Description: DESCRIPTION_SCHEDULED
      Schedule: cron(0 */2 * * ? *)
      Actions:
        - JobName: prod-job2
        - JobName: prod-job3
          Arguments:
            '--job-bookmark-option': job-bookmark-enable
      Name: prod-trigger1-scheduled
```

### Conditional Trigger<a name="aws-resource-glue-trigger--examples--Conditional_Trigger"></a>

The following example creates a conditional trigger that starts a job based on the successful completion of the job run\.

#### JSON<a name="aws-resource-glue-trigger--examples--Conditional_Trigger--json"></a>

```
{
  "Description": "AWS Glue Trigger Test",
  "Resources": {
    "MyJobTriggerRole": {
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
    "MyJob": {
      "Type": "AWS::Glue::Job",
      "Properties": {
        "Name": "MyJobTriggerJob",
        "LogUri": "wikiData",
        "Role": {
          "Ref": "MyJobTriggerRole"
        },
        "Command": {
          "Name": "glueetl",
          "ScriptLocation": "s3://testdata-bucket/s3-target/create-delete-job-xtf-ETL-s3-json-to-csv.py"
        },
        "DefaultArguments": {
          "--job-bookmark-option": "job-bookmark-enable"
        },
        "MaxRetries": 0
      }
    },
    "MyJobTrigger": {
      "Type": "AWS::Glue::Trigger",
      "Properties": {
        "Name": "MyJobTrigger",
        "Type": "CONDITIONAL",
        "Description": "Description for a conditional job trigger",
        "Actions": [
          {
            "JobName": {
              "Ref": "MyJob"
            },
            "Arguments": {
              "--job-bookmark-option": "job-bookmark-enable"
            }
          }
        ],
        "Predicate": {
          "Conditions": [
            {
              "LogicalOperator": "EQUALS",
              "JobName": {
                "Ref": "MyJob"
              },
              "State": "SUCCEEDED"
            }
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-glue-trigger--examples--Conditional_Trigger--yaml"></a>

```
---
Description: "AWS Glue Trigger Test"
Resources:
  MyJobTriggerRole:
    Type: AWS::IAM::Role
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
      Policies:
        -
          PolicyName: "root"
          PolicyDocument:
            Version: "2012-10-17"
            Statement:
              -
                Effect: "Allow"
                Action: "*"
                Resource: "*"
  MyJob:
    Type: AWS::Glue::Job
    Properties:
      Name: "MyJobTriggerJob"
      LogUri: "wikiData"
      Role: !Ref MyJobTriggerRole
      Command:
        Name: "glueetl"
        ScriptLocation: "s3://testdata-bucket/s3-target/create-delete-job-xtf-ETL-s3-json-to-csv.py"
      DefaultArguments:
        "--job-bookmark-option": "job-bookmark-enable"
      MaxRetries: 0
  MyJobTrigger:
    Type: AWS::Glue::Trigger
    Properties:
      Name: "MyJobTrigger"
      Type: "CONDITIONAL"
      Description: "Description for a conditional job trigger"											
      Actions:
        - JobName: !Ref MyJob
          Arguments:
            "--job-bookmark-option": "job-bookmark-enable"
      Predicate:
        Conditions:
          - LogicalOperator: EQUALS
            JobName: !Ref MyJob
            State: SUCCEEDED
```