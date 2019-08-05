# AWS::Glue::Job<a name="aws-resource-glue-job"></a>

The `AWS::Glue::Job` resource specifies an AWS Glue job in the data catalog\. For more information, see [Adding Jobs in AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/add-job.html) and [Job Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-job.html#aws-glue-api-jobs-job-Job) in the *AWS Glue Developer Guide\.*

## Syntax<a name="aws-resource-glue-job-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-job-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Job",
  "Properties" : {
      "[AllocatedCapacity](#cfn-glue-job-allocatedcapacity)" : Double,
      "[Command](#cfn-glue-job-command)" : [JobCommand](aws-properties-glue-job-jobcommand.md),
      "[Connections](#cfn-glue-job-connections)" : [ConnectionsList](aws-properties-glue-job-connectionslist.md),
      "[DefaultArguments](#cfn-glue-job-defaultarguments)" : Json,
      "[Description](#cfn-glue-job-description)" : String,
      "[ExecutionProperty](#cfn-glue-job-executionproperty)" : [ExecutionProperty](aws-properties-glue-job-executionproperty.md),
      "[LogUri](#cfn-glue-job-loguri)" : String,
      "[MaxRetries](#cfn-glue-job-maxretries)" : Double,
      "[Name](#cfn-glue-job-name)" : String,
      "[Role](#cfn-glue-job-role)" : String,
      "[SecurityConfiguration](#cfn-glue-job-securityconfiguration)" : String,
      "[Tags](#cfn-glue-job-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-glue-job-syntax.yaml"></a>

```
Type: AWS::Glue::Job
Properties:
  [AllocatedCapacity](#cfn-glue-job-allocatedcapacity): Double
  [Command](#cfn-glue-job-command):
    [JobCommand](aws-properties-glue-job-jobcommand.md)
  [Connections](#cfn-glue-job-connections):
    [ConnectionsList](aws-properties-glue-job-connectionslist.md)
  [DefaultArguments](#cfn-glue-job-defaultarguments): Json
  [Description](#cfn-glue-job-description): String
  [ExecutionProperty](#cfn-glue-job-executionproperty):
    [ExecutionProperty](aws-properties-glue-job-executionproperty.md)
  [LogUri](#cfn-glue-job-loguri): String
  [MaxRetries](#cfn-glue-job-maxretries): Double
  [Name](#cfn-glue-job-name): String
  [Role](#cfn-glue-job-role): String
  [SecurityConfiguration](#cfn-glue-job-securityconfiguration): String
  [Tags](#cfn-glue-job-tags): Json
```

## Properties<a name="aws-resource-glue-job-properties"></a>

`AllocatedCapacity`  <a name="cfn-glue-job-allocatedcapacity"></a>
The number of capacity units that are allocated to this job\.
*Required*: No
*Type*: Double
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Command`  <a name="cfn-glue-job-command"></a>
The code that executes a job\.
*Required*: Yes
*Type*: [JobCommand](aws-properties-glue-job-jobcommand.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Connections`  <a name="cfn-glue-job-connections"></a>
The connections used for this job\.
*Required*: No
*Type*: [ConnectionsList](aws-properties-glue-job-connectionslist.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultArguments`  <a name="cfn-glue-job-defaultarguments"></a>
The default arguments for this job, specified as name\-value pairs\.
You can specify arguments here that your own job\-execution script consumes, in addition to arguments that AWS Glue itself consumes\.
For information about how to specify and consume your own job arguments, see [Calling AWS Glue APIs in Python](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-programming-python-calling.html) in the *AWS Glue Developer Guide*\.
For information about the key\-value pairs that AWS Glue consumes to set up your job, see [Special Parameters Used by AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-programming-etl-glue-arguments.html) in the *AWS Glue Developer Guide*\.
*Required*: No
*Type*: Json
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-glue-job-description"></a>
A description of the job\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionProperty`  <a name="cfn-glue-job-executionproperty"></a>
The maximum number of concurrent runs that are allowed for this job\.
*Required*: No
*Type*: [ExecutionProperty](aws-properties-glue-job-executionproperty.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogUri`  <a name="cfn-glue-job-loguri"></a>
This field is reserved for future use\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRetries`  <a name="cfn-glue-job-maxretries"></a>
The maximum number of times to retry this job after a JobRun fails\.
*Required*: No
*Type*: Double
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-job-name"></a>
The name you assign to this job definition\.
*Required*: No
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Role`  <a name="cfn-glue-job-role"></a>
The name or Amazon Resource Name \(ARN\) of the IAM role associated with this job\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityConfiguration`  <a name="cfn-glue-job-securityconfiguration"></a>
The name of the `SecurityConfiguration` structure to be used with this job\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-glue-job-tags"></a>
The tags to use with this job\. You can use tags to limit access to the job\. For more information about tags in AWS Glue, see [AWS Tags in AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/monitor-tags.html) in the developer guide\.
*Required*: No
*Type*: Json
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-glue-job-return-values"></a>

### Ref<a name="aws-resource-glue-job-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the job name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-glue-job--examples"></a>

### <a name="aws-resource-glue-job--examples--"></a>

The following example creates a job with an associated role\.

#### JSON<a name="aws-resource-glue-job--examples----json"></a>

```
{
  "Description": "AWS Glue Job Test",
  "Resources": {
    "MyJobRole": {
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
        "Command": {
          "Name": "glueetl",
          "ScriptLocation": "s3://aws-glue-scripts//prod-job1"
        },
        "DefaultArguments": {
          "--job-bookmark-option": "job-bookmark-enable"
        },
        "ExecutionProperty": {
          "MaxConcurrentRuns": 2
        },
        "MaxRetries": 0,
        "Name": "cf-job1",
        "Role": {
          "Ref": "MyJobRole"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-glue-job--examples----yaml"></a>

```
---
Description: "AWS Glue Job Test"
Resources:
  MyJobRole:
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
      Command:
        Name: glueetl
        ScriptLocation: "s3://aws-glue-scripts//prod-job1"
      DefaultArguments:
        "--job-bookmark-option": "job-bookmark-enable"
      ExecutionProperty:
        MaxConcurrentRuns: 2
      MaxRetries: 0
      Name: cf-job1
      Role: !Ref MyJobRole
```
