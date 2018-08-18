# Amazon EMR Step KeyValue<a name="aws-properties-emr-step-hadoopjarstepconfig-keyvalue"></a>

`KeyValue` is a property of the [Amazon EMR Step HadoopJarStepConfig](aws-properties-emr-step-hadoopjarstepconfig.md) property that specifies key\-value pairs, which are passed to a JAR file that Amazon EMR \(Amazon EMR\) executes\.

## Syntax<a name="w3ab2c21c14e1205b5"></a>

### JSON<a name="aws-properties-emr-step-hadoopjarstepconfig-keyvalue-syntax.json"></a>

```
{
  "[Key](#cfn-emr-step-hadoopjarstepconfig-keyvalue-key)" : String,
  "[Value](#cfn-emr-step-hadoopjarstepconfig-keyvalue-value)" : String
}
```

### YAML<a name="aws-properties-emr-step-hadoopjarstepconfig-keyvalue-syntax.yaml"></a>

```
[Key](#cfn-emr-step-hadoopjarstepconfig-keyvalue-key): String
[Value](#cfn-emr-step-hadoopjarstepconfig-keyvalue-value): String
```

## Properties<a name="w3ab2c21c14e1205b7"></a>

`Key`  <a name="cfn-emr-step-hadoopjarstepconfig-keyvalue-key"></a>
The unique identifier of a key\-value pair\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-emr-step-hadoopjarstepconfig-keyvalue-value"></a>
The value part of the identified key\.  
*Required*: No  
*Type*: String