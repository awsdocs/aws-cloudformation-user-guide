# AWS::EMR::Cluster StepConfig<a name="aws-properties-elasticmapreduce-cluster-stepconfig"></a>

`StepConfig` is a property of the `AWS::EMR::Cluster` resource\. The `StepConfig` property type specifies a cluster \(job flow\) step, which runs only on the master node\. Steps are used to submit data processing jobs to the cluster\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-stepconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-stepconfig-syntax.json"></a>

```
{
  "[ActionOnFailure](#cfn-elasticmapreduce-cluster-stepconfig-actiononfailure)" : String,
  "[HadoopJarStep](#cfn-elasticmapreduce-cluster-stepconfig-hadoopjarstep)" : HadoopJarStepConfig,
  "[Name](#cfn-elasticmapreduce-cluster-stepconfig-name)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-stepconfig-syntax.yaml"></a>

```
  [ActionOnFailure](#cfn-elasticmapreduce-cluster-stepconfig-actiononfailure): String
  [HadoopJarStep](#cfn-elasticmapreduce-cluster-stepconfig-hadoopjarstep): 
    HadoopJarStepConfig
  [Name](#cfn-elasticmapreduce-cluster-stepconfig-name): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-stepconfig-properties"></a>

`ActionOnFailure`  <a name="cfn-elasticmapreduce-cluster-stepconfig-actiononfailure"></a>
The action to take when the cluster step fails\. Possible values are `CANCEL_AND_WAIT` and `CONTINUE`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HadoopJarStep`  <a name="cfn-elasticmapreduce-cluster-stepconfig-hadoopjarstep"></a>
The JAR file used for the step\.  
*Required*: Yes  
*Type*: [HadoopJarStepConfig](aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-elasticmapreduce-cluster-stepconfig-name"></a>
The name of the step\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)