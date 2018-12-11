# Amazon EMR Cluster HadoopJarStepConfig<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig"></a>

<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig-description"></a>The `HadoopJarStepConfig` property type specifies a job flow step consisting of a JAR file whose main function will be executed\. The main function submits a job for Hadoop to execute and waits for the job to finish or fail\.

<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig-inheritance"></a> `HadoopJarStepConfig` is a property of the [Amazon EMR Cluster StepConfig](aws-properties-elasticmapreduce-cluster-stepconfig.md) property type\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig-syntax.json"></a>

```
{
  "[Args](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-args)" : [ String, ... ] ,
  "[Jar](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-jar)" : String,
  "[MainClass](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-mainclass)" : String,
  "[StepProperties](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-stepproperties)" : [ [KeyValue](aws-properties-elasticmapreduce-cluster-keyvalue.md), ... ]
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig-syntax.yaml"></a>

```
[Args](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-args)
  - String
[Jar](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-jar): String
[MainClass](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-mainclass): String
[StepProperties](#cfn-elasticmapreduce-cluster-hadoopjarstepconfig-stepproperties)
  - [KeyValue](aws-properties-elasticmapreduce-cluster-keyvalue.md)
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig-properties"></a>

`Args`  <a name="cfn-elasticmapreduce-cluster-hadoopjarstepconfig-args"></a>
A list of command line arguments passed to the JAR file's main function when executed\.  
Length Constraints: Minimum length of 0\. Maximum length of 10280\.  
Pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Jar`  <a name="cfn-elasticmapreduce-cluster-hadoopjarstepconfig-jar"></a>
A path to a JAR file run during the step\.  
Length Constraints: Minimum length of 0\. Maximum length of 10280\.  
Pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MainClass`  <a name="cfn-elasticmapreduce-cluster-hadoopjarstepconfig-mainclass"></a>
The name of the main class in the specified Java file\. If not specified, the JAR file should specify a Main\-Class in its manifest file\.  
Length Constraints: Minimum length of 0\. Maximum length of 10280\.  
Pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StepProperties`  <a name="cfn-elasticmapreduce-cluster-hadoopjarstepconfig-stepproperties"></a>
A list of Java properties that are set when the step runs\. You can use these properties to pass key value pairs to your main function\.  
 *Required*: No  
 *Type*: List of [Amazon EMR Cluster KeyValue](aws-properties-elasticmapreduce-cluster-keyvalue.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig-seealso"></a>
+ [HadoopJarStepConfig](https://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_HadoopJarStepConfig.html) in the *Amazon EMR API Reference*