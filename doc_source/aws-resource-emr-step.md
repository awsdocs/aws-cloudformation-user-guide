# AWS::EMR::Step<a name="aws-resource-emr-step"></a>

Use `Step` to specify a cluster \(job flow\) step, which runs only on the master node\. Steps are used to submit data processing jobs to a cluster\.

## Syntax<a name="aws-resource-emr-step-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-step-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::Step",
  "Properties" : {
      "[ActionOnFailure](#cfn-elasticmapreduce-step-actiononfailure)" : String,
      "[HadoopJarStep](#cfn-elasticmapreduce-step-hadoopjarstep)" : HadoopJarStepConfig,
      "[JobFlowId](#cfn-elasticmapreduce-step-jobflowid)" : String,
      "[Name](#cfn-elasticmapreduce-step-name)" : String
    }
}
```

### YAML<a name="aws-resource-emr-step-syntax.yaml"></a>

```
Type: AWS::EMR::Step
Properties: 
  [ActionOnFailure](#cfn-elasticmapreduce-step-actiononfailure): String
  [HadoopJarStep](#cfn-elasticmapreduce-step-hadoopjarstep): 
    HadoopJarStepConfig
  [JobFlowId](#cfn-elasticmapreduce-step-jobflowid): String
  [Name](#cfn-elasticmapreduce-step-name): String
```

## Properties<a name="aws-resource-emr-step-properties"></a>

`ActionOnFailure`  <a name="cfn-elasticmapreduce-step-actiononfailure"></a>
This specifies what action to take when the cluster step fails\. Possible values are `CANCEL_AND_WAIT` and `CONTINUE`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HadoopJarStep`  <a name="cfn-elasticmapreduce-step-hadoopjarstep"></a>
The `HadoopJarStepConfig` property type specifies a job flow step consisting of a JAR file whose main function will be executed\. The main function submits a job for the cluster to execute as a step on the master node, and then waits for the job to finish or fail before executing subsequent steps\.  
*Required*: Yes  
*Type*: [HadoopJarStepConfig](aws-properties-elasticmapreduce-step-hadoopjarstepconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JobFlowId`  <a name="cfn-elasticmapreduce-step-jobflowid"></a>
A string that uniquely identifies the cluster \(job flow\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-elasticmapreduce-step-name"></a>
The name of the cluster step\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-emr-step-return-values"></a>

### Ref<a name="aws-resource-emr-step-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns returns the ID of the step\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.