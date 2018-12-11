# Amazon EMR Cluster StepConfig<a name="aws-properties-elasticmapreduce-cluster-stepconfig"></a>

<a name="aws-properties-elasticmapreduce-cluster-stepconfig-description"></a>The `StepConfig` property type specifies a cluster \(job flow\) step\.

<a name="aws-properties-elasticmapreduce-cluster-stepconfig-inheritance"></a> `StepConfig` is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-stepconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-stepconfig-syntax.json"></a>

```
{
  "[ActionOnFailure](#cfn-elasticmapreduce-cluster-stepconfig-actiononfailure)" : String,
  "[HadoopJarStep](#cfn-elasticmapreduce-cluster-stepconfig-hadoopjarstep)" : [HadoopJarStepConfig](aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig.md),
  "[Name](#cfn-elasticmapreduce-cluster-stepconfig-name)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-stepconfig-syntax.yaml"></a>

```
[ActionOnFailure](#cfn-elasticmapreduce-cluster-stepconfig-actiononfailure): String
[HadoopJarStep](#cfn-elasticmapreduce-cluster-stepconfig-hadoopjarstep): [HadoopJarStepConfig](aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig.md)
[Name](#cfn-elasticmapreduce-cluster-stepconfig-name): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-stepconfig-properties"></a>

`ActionOnFailure`  <a name="cfn-elasticmapreduce-cluster-stepconfig-actiononfailure"></a>
The action to take when the cluster step fails\.   
Possible values are `TERMINATE_CLUSTER`, `CANCEL_AND_WAIT`, and `CONTINUE`\. `TERMINATE_JOB_FLOW` is provided for backward compatibility\. We recommend using `TERMINATE_CLUSTER` instead\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`HadoopJarStep`  <a name="cfn-elasticmapreduce-cluster-stepconfig-hadoopjarstep"></a>
The JAR file used for the step\.  
 *Required*: Yes  
 *Type*: [HadoopJarStepConfig](aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig.md)   
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-elasticmapreduce-cluster-stepconfig-name"></a>
The name of the step\.  
Length Constraints: Minimum length of 0\. Maximum length of 256\.  
Pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-elasticmapreduce-cluster-stepconfig-seealso"></a>
+ [StepConfig](https://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_StepConfig.html) in the *Amazon EMR API Reference*