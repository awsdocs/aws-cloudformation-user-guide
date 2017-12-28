# AWS::EMR::Step<a name="aws-resource-emr-step"></a>

The `AWS::EMR::Step` resource creates a unit of work \(a job flow step\) that you submit to an Amazon EMR \(Amazon EMR\) cluster\. The job flow step contains instructions for processing data on the cluster\.

**Note**  
You can't delete work flow steps\. During a stack update, if you remove a step, AWS CloudFormation takes no action\.


+ [Syntax](#aws-resource-emr-step-syntax)
+ [Properties](#w3ab2c21c10d634c11)
+ [Return Values](#w3ab2c21c10d634c13)
+ [Example](#w3ab2c21c10d634c15)

## Syntax<a name="aws-resource-emr-step-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-step-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::Step",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-actiononfailure)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstep)" : HadoopJarStepConfig,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-jobflowid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-name)" : String
  }
}
```

### YAML<a name="aws-resource-emr-step-syntax.yaml"></a>

```
Type: "AWS::EMR::Step"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-actiononfailure): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstep):
    HadoopJarStepConfig
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-jobflowid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-name): String
```

## Properties<a name="w3ab2c21c10d634c11"></a>

`ActionOnFailure`  
The action to take if the job flow step fails\. Currently, AWS CloudFormation supports `CONTINUE` and `CANCEL_AND_WAIT`\.  

+ `TERMINATE_CLUSTER` indicates that all associated cluster resources terminate if the step fails, and no subsequent steps or jobs are attempted\.

+ `CANCEL_AND_WAIT` indicates that the step is canceled, and all subsequent steps and jobs are attempted\.
For more information, see [Managing Cluster Termination](http://docs.aws.amazon.com//ElasticMapReduce/latest/ManagementGuide/UsingEMR_TerminationProtection.html) in the *Amazon EMR Management Guide*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`HadoopJarStep`  
The JAR file that includes the main function that Amazon EMR executes\.  
*Required: *Yes  
*Type*: [Amazon EMR Step HadoopJarStepConfig](aws-properties-emr-step-hadoopjarstepconfig.md)  
*Update requires*: Replacement

`JobFlowId`  
The ID of a cluster in which you want to run this job flow step\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Name`  
A name for the job flow step\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d634c13"></a>

### Ref<a name="w3ab2c21c10d634c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the step ID, such as `s-1A2BC3D4EFG56`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d634c15"></a>

The following example creates a step that submits work to the `TestCluster` cluster\. The step runs the `pi` program in the `hadoop-mapreduce-examples-2.6.0.jar` file with 5 maps and 10 samples, specified in the `Args` property\.

### JSON<a name="aws-resource-emr-step-example.json"></a>

```
"TestStep": {
  "Type": "AWS::EMR::Step",
  "Properties": {
    "ActionOnFailure": "CONTINUE",
    "HadoopJarStep": {
      "Args": [
        "5",
        "10"
      ],
      "Jar": "s3://emr-cfn-test/hadoop-mapreduce-examples-2.6.0.jar",
      "MainClass": "pi"
    },
    "Name": "TestStep",
    "JobFlowId": {
      "Ref": "TestCluster"
    }
  }
}
```

### YAML<a name="aws-resource-emr-step-example.yaml"></a>

```
TestStep: 
  Type: "AWS::EMR::Step"
  Properties: 
    ActionOnFailure: "CONTINUE"
    HadoopJarStep: 
      Args: 
        - "5"
        - "10"
      Jar: "s3://emr-cfn-test/hadoop-mapreduce-examples-2.6.0.jar"
      MainClass: "pi"
    Name: "TestStep"
    JobFlowId: 
      Ref: "TestCluster"
```