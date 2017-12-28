# AWS::Glue::Job<a name="aws-resource-glue-job"></a>

The `AWS::Glue::Job` resource specifies an AWS Glue job in the data catalog\. For more information, see [Adding Jobs in AWS Glue](http://docs.aws.amazon.com/glue/latest/dg/add-job.html) and [Job Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-job.html#aws-glue-api-jobs-job-Job) in the *AWS Glue Developer Guide*\. 


+ [Syntax](#aws-resource-glue-job-syntax)
+ [Properties](#aws-resource-glue-job-properties)
+ [Return Values](#aws-resource-glue-job-returnvalues)
+ [Examples](#aws-resource-glue-job-examples)

## Syntax<a name="aws-resource-glue-job-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-job-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Job",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-role)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-defaultarguments)" : JSON object,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-connections)" : ConnectionsList,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-maxretries)" : Double,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-loguri)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-command)" : JobCommand,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-allocatedcapacity)" : Double,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-executionproperty)" : ExecutionProperty,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-name)" : String
  }
}
```

### YAML<a name="aws-resource-glue-job-syntax.yaml"></a>

```
Type: "AWS::Glue::Job"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-role): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-defaultarguments): JSON object
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-connections): 
    ConnectionsList
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-maxretries): Double
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-loguri): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-command): 
    JobCommand
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-allocatedcapacity): Double
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-executionproperty): 
    ExecutionProperty
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-name): String
```

## Properties<a name="aws-resource-glue-job-properties"></a>

`Role`  
The role that's associated with the job\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`DefaultArguments`  
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the default parameters for the job\.  
You can specify arguments here that your own job\-execution script consumes, as well as arguments that AWS Glue itself consumes\. For information about how to specify and consume your own Job arguments, see the [ Passing and Accessing Python Parameters in AWS Glue](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-pyspark-extensions-python-intro.html#aws-glue-api-crawler-pyspark-extensions-python-intro-parameters) in the *AWS Glue Developer Guide*\.  
AWS Glue consumes the following arguments to set up the Job script environment:  

+ `--scriptLocation` — The Amazon S3 location where your ETL script is located \(in a form like `s3://path/to/my/script.py`\)\.

+ `--extra-py-files` — Amazon S3 path\(s\) to additional Python modules that AWS Glue adds to the Python path before executing your script\. Multiple values must be complete paths separated by a comma \(,\)\. Note that only pure Python modules will work currently\. Extension modules written in C or other languages are not supported\.

+ `--extra-jars` — Amazon S3 path\(s\) to additional Java `.jar` file\(s\) that AWS Glue adds to the Java classpath before executing your script\. Multiple values must be complete paths separated by a comma \(,\)\.

+ `--extra-files` — Amazon S3 path\(s\) to additional files such as configuration files\) that AWS Glue copies to the working directory of your script before executing it\. Multiple values must be complete paths separated by a comma \(,\)\.
There are several argument names used by AWS Glue internally that you should never set:  

+ `--conf` — Internal to AWS Glue\. Do not set\!

+ `--debug` — Internal to AWS Glue\. Do not set\!

+ `--mode` — Internal to AWS Glue\. Do not set\!

+ `--JOB_NAME` — Internal to AWS Glue\. Do not set\!
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`Connections`  
The connections that are used by the job\.  
 *Required*: No  
 *Type*:   
 *Update requires*: No interruption 

`MaxRetries`  
The maximum number of times to retry this job if it fails\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: No interruption 

`Description`  
The description of the job\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`LogUri`  
The location of the logs for the job\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Command`  
The code that executes a job\.  
 *Required*: Yes  
 *Type*:   
 *Update requires*: No interruption 

`AllocatedCapacity`  
The number of capacity units that are allocated to this job\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: No interruption 

`ExecutionProperty`  
The execution property of the job, which specifies the maximum number of concurrent runs that are allowed for the job\.  
 *Required*: No  
 *Type*:   
 *Update requires*: No interruption 

`Name`  
The name of the job\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

## Return Values<a name="aws-resource-glue-job-returnvalues"></a>

### Ref<a name="w3ab2c21c10d669c10b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\. 

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
          "--continuation-option": "continuation-enabled"
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
        "--continuation-option": continuation-enabled
      ExecutionProperty:
        MaxConcurrentRuns: 2
      MaxRetries: 0
      Name: cf-job1
      Role: !Ref MyJobRole
```