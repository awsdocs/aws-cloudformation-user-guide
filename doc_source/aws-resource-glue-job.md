# AWS::Glue::Job<a name="aws-resource-glue-job"></a>

The `AWS::Glue::Job` resource specifies an AWS Glue job in the data catalog\. For more information, see [Adding Jobs in AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/add-job.html) and [Job Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-job.html#aws-glue-api-jobs-job-Job) in the *AWS Glue Developer Guide*\. 

## Syntax<a name="aws-resource-glue-job-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-job-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Job",
  "Properties" : {
    "[Role](#cfn-glue-job-role)" : String,
    "[DefaultArguments](#cfn-glue-job-defaultarguments)" : JSON object,
    "[Connections](#cfn-glue-job-connections)" : [*ConnectionsList*](aws-properties-glue-job-connectionslist.md),
    "[MaxRetries](#cfn-glue-job-maxretries)" : Double,
    "[Description](#cfn-glue-job-description)" : String,
    "[LogUri](#cfn-glue-job-loguri)" : String,
    "[Command](#cfn-glue-job-command)" : [*JobCommand*](aws-properties-glue-job-jobcommand.md),
    "[AllocatedCapacity](#cfn-glue-job-allocatedcapacity)" : Double,
    "[ExecutionProperty](#cfn-glue-job-executionproperty)" : [*ExecutionProperty*](aws-properties-glue-job-executionproperty.md),
    "[Name](#cfn-glue-job-name)" : String
  }
}
```

### YAML<a name="aws-resource-glue-job-syntax.yaml"></a>

```
Type: AWS::Glue::Job
Properties:
  [Role](#cfn-glue-job-role): String
  [DefaultArguments](#cfn-glue-job-defaultarguments): JSON object
  [Connections](#cfn-glue-job-connections): 
    [*ConnectionsList*](aws-properties-glue-job-connectionslist.md)
  [MaxRetries](#cfn-glue-job-maxretries): Double
  [Description](#cfn-glue-job-description): String
  [LogUri](#cfn-glue-job-loguri): String
  [Command](#cfn-glue-job-command): 
    [*JobCommand*](aws-properties-glue-job-jobcommand.md)
  [AllocatedCapacity](#cfn-glue-job-allocatedcapacity): Double
  [ExecutionProperty](#cfn-glue-job-executionproperty): 
    [*ExecutionProperty*](aws-properties-glue-job-executionproperty.md)
  [Name](#cfn-glue-job-name): String
```

## Properties<a name="aws-resource-glue-job-properties"></a>

`Role`  <a name="cfn-glue-job-role"></a>
The role that's associated with the job\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DefaultArguments`  <a name="cfn-glue-job-defaultarguments"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the default parameters for the job\.  
You can specify arguments here that your own job\-execution script consumes, as well as arguments that AWS Glue itself consumes\. For information about how to specify and consume your own Job arguments, see the [ Passing and Accessing Python Parameters in AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-pyspark-extensions-python-intro.html#aws-glue-api-crawler-pyspark-extensions-python-intro-parameters) in the *AWS Glue Developer Guide*\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Connections`  <a name="cfn-glue-job-connections"></a>
The connections that are used by the job\.  
 *Required*: No  
 *Type*: [ConnectionsList](aws-properties-glue-job-connectionslist.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxRetries`  <a name="cfn-glue-job-maxretries"></a>
The maximum number of times to retry this job if it fails\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-glue-job-description"></a>
The description of the job\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LogUri`  <a name="cfn-glue-job-loguri"></a>
The location of the logs for the job\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Command`  <a name="cfn-glue-job-command"></a>
The code that executes a job\.  
 *Required*: Yes  
 *Type*: [JobCommand](aws-properties-glue-job-jobcommand.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AllocatedCapacity`  <a name="cfn-glue-job-allocatedcapacity"></a>
The number of capacity units that are allocated to this job\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ExecutionProperty`  <a name="cfn-glue-job-executionproperty"></a>
The execution property of the job, which specifies the maximum number of concurrent runs that are allowed for the job\.  
 *Required*: No  
 *Type*: [ExecutionProperty](aws-properties-glue-job-executionproperty.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-job-name"></a>
The name of the job\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-glue-job-returnvalues"></a>

### Ref<a name="w4ab1c21c10d138c26b9b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-glue-job-examples"></a>

### <a name="aws-resource-glue-job-example1"></a>

The following example creates a job with an associated role\.

#### JSON<a name="aws-resource-glue-job-example1.json"></a>

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

#### YAML<a name="aws-resource-glue-job-example1.yaml"></a>

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