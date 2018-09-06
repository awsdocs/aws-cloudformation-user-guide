# AWS::Glue::Trigger<a name="aws-resource-glue-trigger"></a>

The `AWS::Glue::Trigger` resource specifies triggers that run AWS Glue jobs\. For more information, see [Triggering Jobs in AWS Glue](http://docs.aws.amazon.com/glue/latest/dg/trigger-job.html) and [Trigger Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Trigger) in the *AWS Glue Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-glue-trigger-syntax)
+ [Properties](#aws-resource-glue-trigger-properties)
+ [Return Values](#aws-resource-glue-trigger-returnvalues)
+ [Examples](#aws-resource-glue-trigger-examples)

## Syntax<a name="aws-resource-glue-trigger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-trigger-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Trigger",
  "Properties" : {
    "[Type](#cfn-glue-trigger-type)" : String,
    "[Description](#cfn-glue-trigger-description)" : String,
    "[Actions](#cfn-glue-trigger-actions)" : [ [*Action*](aws-properties-glue-trigger-action.md), ... ],
    "[Schedule](#cfn-glue-trigger-schedule)" : String,
    "[Name](#cfn-glue-trigger-name)" : String,
    "[Predicate](#cfn-glue-trigger-predicate)" : [*Predicate*](aws-properties-glue-trigger-predicate.md)
  }
}
```

### YAML<a name="aws-resource-glue-trigger-syntax.yaml"></a>

```
Type: "AWS::Glue::Trigger"
Properties:
  [Type](#cfn-glue-trigger-type): String
  [Description](#cfn-glue-trigger-description): String
  [Actions](#cfn-glue-trigger-actions): 
    - [*Action*](aws-properties-glue-trigger-action.md) 
  [Schedule](#cfn-glue-trigger-schedule): String
  [Name](#cfn-glue-trigger-name): String
  [Predicate](#cfn-glue-trigger-predicate): 
    [*Predicate*](aws-properties-glue-trigger-predicate.md)
```

## Properties<a name="aws-resource-glue-trigger-properties"></a>

`Type`  <a name="cfn-glue-trigger-type"></a>
The type of job trigger\. Valid values are `SCHEDULED`, `CONDITIONAL`, or `ON_DEMAND`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-glue-trigger-description"></a>
The description of the job trigger\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Actions`  <a name="cfn-glue-trigger-actions"></a>
The actions that the job trigger initiates when it fires\.  
 *Required*: Yes  
 *Type*: List of [AWS Glue Trigger Action](aws-properties-glue-trigger-action.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Schedule`  <a name="cfn-glue-trigger-schedule"></a>
The `cron` schedule expression for the job trigger\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-trigger-name"></a>
The name of the job trigger\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Predicate`  <a name="cfn-glue-trigger-predicate"></a>
The predicate of the job trigger, which determines when the trigger fires\.  
 *Required*: No  
 *Type*: [AWS Glue Trigger Predicate](aws-properties-glue-trigger-predicate.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-glue-trigger-returnvalues"></a>

### Ref<a name="w3ab2c21c10d722c10b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-glue-trigger-examples"></a>

### On\-Demand Trigger<a name="aws-resource-glue-trigger-example1"></a>

The following example creates an on\-demand trigger that triggers one job\.

#### JSON<a name="aws-resource-glue-trigger-example1.json"></a>

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

#### YAML<a name="aws-resource-glue-trigger-example1.yaml"></a>

```
Resources:
  OnDemandJobTrigger:
    Type: 'AWS::Glue::Trigger'
    Properties:
      Type: ON_DEMAND
      Description: DESCRIPTION_ON_DEMAND
      Actions:
        - JobName: prod-job2
      Name: prod-trigger1-ondemand
```

### Scheduled Trigger<a name="aws-resource-glue-trigger-example2"></a>

The following example creates a scheduled trigger that runs every two hours and triggers two jobs\. Note that it declares an argument for `prod-job3`\.

#### JSON<a name="aws-resource-glue-trigger-example2.json"></a>

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

#### YAML<a name="aws-resource-glue-trigger-example2.yaml"></a>

```
Resources:
  ScheduledJobTrigger:
    Type: 'AWS::Glue::Trigger'
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

### Conditional Trigger<a name="aws-resource-glue-trigger-example3"></a>

The following example creates a conditional trigger that starts a job based on the successful completion of the job run\.

#### JSON<a name="aws-resource-glue-trigger-example3.json"></a>

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
          "--continuation-option": "continuation-enabled"
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

#### YAML<a name="aws-resource-glue-trigger-example3.yaml"></a>

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
        "--continuation-option": "continuation-enabled"
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