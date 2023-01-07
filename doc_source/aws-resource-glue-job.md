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
      "[Command](#cfn-glue-job-command)" : JobCommand,
      "[Connections](#cfn-glue-job-connections)" : ConnectionsList,
      "[DefaultArguments](#cfn-glue-job-defaultarguments)" : Json,
      "[Description](#cfn-glue-job-description)" : String,
      "[ExecutionProperty](#cfn-glue-job-executionproperty)" : ExecutionProperty,
      "[GlueVersion](#cfn-glue-job-glueversion)" : String,
      "[LogUri](#cfn-glue-job-loguri)" : String,
      "[MaxCapacity](#cfn-glue-job-maxcapacity)" : Double,
      "[MaxRetries](#cfn-glue-job-maxretries)" : Double,
      "[Name](#cfn-glue-job-name)" : String,
      "[NotificationProperty](#cfn-glue-job-notificationproperty)" : NotificationProperty,
      "[NumberOfWorkers](#cfn-glue-job-numberofworkers)" : Integer,
      "[Role](#cfn-glue-job-role)" : String,
      "[SecurityConfiguration](#cfn-glue-job-securityconfiguration)" : String,
      "[Tags](#cfn-glue-job-tags)" : Json,
      "[Timeout](#cfn-glue-job-timeout)" : Integer,
      "[WorkerType](#cfn-glue-job-workertype)" : String
    }
}
```

### YAML<a name="aws-resource-glue-job-syntax.yaml"></a>

```
Type: AWS::Glue::Job
Properties: 
  [AllocatedCapacity](#cfn-glue-job-allocatedcapacity): Double
  [Command](#cfn-glue-job-command): 
    JobCommand
  [Connections](#cfn-glue-job-connections): 
    ConnectionsList
  [DefaultArguments](#cfn-glue-job-defaultarguments): Json
  [Description](#cfn-glue-job-description): String
  [ExecutionProperty](#cfn-glue-job-executionproperty): 
    ExecutionProperty
  [GlueVersion](#cfn-glue-job-glueversion): String
  [LogUri](#cfn-glue-job-loguri): String
  [MaxCapacity](#cfn-glue-job-maxcapacity): Double
  [MaxRetries](#cfn-glue-job-maxretries): Double
  [Name](#cfn-glue-job-name): String
  [NotificationProperty](#cfn-glue-job-notificationproperty): 
    NotificationProperty
  [NumberOfWorkers](#cfn-glue-job-numberofworkers): Integer
  [Role](#cfn-glue-job-role): String
  [SecurityConfiguration](#cfn-glue-job-securityconfiguration): String
  [Tags](#cfn-glue-job-tags): Json
  [Timeout](#cfn-glue-job-timeout): Integer
  [WorkerType](#cfn-glue-job-workertype): String
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

`GlueVersion`  <a name="cfn-glue-job-glueversion"></a>
Glue version determines the versions of Apache Spark and Python that AWS Glue supports\. The Python version indicates the version supported for jobs of type Spark\.   
For more information about the available AWS Glue versions and corresponding Spark and Python versions, see [Glue version](https://docs.aws.amazon.com/glue/latest/dg/add-job.html) in the developer guide\.  
Jobs that are created without specifying a Glue version default to Glue 0\.9\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogUri`  <a name="cfn-glue-job-loguri"></a>
This field is reserved for future use\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCapacity`  <a name="cfn-glue-job-maxcapacity"></a>
The number of AWS Glue data processing units \(DPUs\) that can be allocated when this job runs\. A DPU is a relative measure of processing power that consists of 4 vCPUs of compute capacity and 16 GB of memory\.  
Do not set `Max Capacity` if using `WorkerType` and `NumberOfWorkers`\.  
The value that can be allocated for `MaxCapacity` depends on whether you are running a Python shell job or an Apache Spark ETL job:  
+ When you specify a Python shell job \(`JobCommand.Name`="pythonshell"\), you can allocate either 0\.0625 or 1 DPU\. The default is 0\.0625 DPU\.
+ When you specify an Apache Spark ETL job \(`JobCommand.Name`="glueetl"\), you can allocate from 2 to 100 DPUs\. The default is 10 DPUs\. This job type cannot have a fractional DPU allocation\.
*Required*: No  
*Type*: Double  
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

`NotificationProperty`  <a name="cfn-glue-job-notificationproperty"></a>
Specifies configuration properties of a notification\.  
*Required*: No  
*Type*: [NotificationProperty](aws-properties-glue-job-notificationproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfWorkers`  <a name="cfn-glue-job-numberofworkers"></a>
The number of workers of a defined `workerType` that are allocated when a job runs\.  
The maximum number of workers you can define are 299 for `G.1X`, and 149 for `G.2X`\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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
The tags to use with this job\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-glue-job-timeout"></a>
The job timeout in minutes\. This is the maximum time that a job run can consume resources before it is terminated and enters TIMEOUT status\. The default is 2,880 minutes \(48 hours\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkerType`  <a name="cfn-glue-job-workertype"></a>
The type of predefined worker that is allocated when a job runs\. Accepts a value of Standard, G\.1X, or G\.2X\.  
+ For the `Standard` worker type, each worker provides 4 vCPU, 16 GB of memory and a 50GB disk, and 2 executors per worker\.
+ For the `G.1X` worker type, each worker maps to 1 DPU \(4 vCPU, 16 GB of memory, 64 GB disk\), and provides 1 executor per worker\. We recommend this worker type for memory\-intensive jobs\.
+ For the `G.2X` worker type, each worker maps to 2 DPU \(8 vCPU, 32 GB of memory, 128 GB disk\), and provides 1 executor per worker\. We recommend this worker type for memory\-intensive jobs\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-job-return-values"></a>

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