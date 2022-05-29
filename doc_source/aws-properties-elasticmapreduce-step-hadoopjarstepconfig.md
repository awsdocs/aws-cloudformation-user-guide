# AWS::EMR::Step HadoopJarStepConfig<a name="aws-properties-elasticmapreduce-step-hadoopjarstepconfig"></a>

A job flow step consisting of a JAR file whose main function will be executed\. The main function submits a job for Hadoop to execute and waits for the job to finish or fail\.

## Syntax<a name="aws-properties-elasticmapreduce-step-hadoopjarstepconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-step-hadoopjarstepconfig-syntax.json"></a>

```
{
  "[Args](#cfn-elasticmapreduce-step-hadoopjarstepconfig-args)" : [ String, ... ],
  "[Jar](#cfn-elasticmapreduce-step-hadoopjarstepconfig-jar)" : String,
  "[MainClass](#cfn-elasticmapreduce-step-hadoopjarstepconfig-mainclass)" : String,
  "[StepProperties](#cfn-elasticmapreduce-step-hadoopjarstepconfig-stepproperties)" : [ KeyValue, ... ]
}
```

### YAML<a name="aws-properties-elasticmapreduce-step-hadoopjarstepconfig-syntax.yaml"></a>

```
  [Args](#cfn-elasticmapreduce-step-hadoopjarstepconfig-args): 
    - String
  [Jar](#cfn-elasticmapreduce-step-hadoopjarstepconfig-jar): String
  [MainClass](#cfn-elasticmapreduce-step-hadoopjarstepconfig-mainclass): String
  [StepProperties](#cfn-elasticmapreduce-step-hadoopjarstepconfig-stepproperties): 
    - KeyValue
```

## Properties<a name="aws-properties-elasticmapreduce-step-hadoopjarstepconfig-properties"></a>

`Args`  <a name="cfn-elasticmapreduce-step-hadoopjarstepconfig-args"></a>
A list of command line arguments passed to the JAR file's main function when executed\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Jar`  <a name="cfn-elasticmapreduce-step-hadoopjarstepconfig-jar"></a>
A path to a JAR file run during the step\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MainClass`  <a name="cfn-elasticmapreduce-step-hadoopjarstepconfig-mainclass"></a>
The name of the main class in the specified Java file\. If not specified, the JAR file should specify a Main\-Class in its manifest file\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StepProperties`  <a name="cfn-elasticmapreduce-step-hadoopjarstepconfig-stepproperties"></a>
A list of Java properties that are set when the step runs\. You can use these properties to pass key value pairs to your main function\.  
*Required*: No  
*Type*: List of [KeyValue](aws-properties-elasticmapreduce-step-keyvalue.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)