# AWS::EMRServerless::Application InitialCapacityConfigKeyValuePair<a name="aws-properties-emrserverless-application-initialcapacityconfigkeyvaluepair"></a>

The initial capacity configuration per worker\.

## Syntax<a name="aws-properties-emrserverless-application-initialcapacityconfigkeyvaluepair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrserverless-application-initialcapacityconfigkeyvaluepair-syntax.json"></a>

```
{
  "[Key](#cfn-emrserverless-application-initialcapacityconfigkeyvaluepair-key)" : String,
  "[Value](#cfn-emrserverless-application-initialcapacityconfigkeyvaluepair-value)" : InitialCapacityConfig
}
```

### YAML<a name="aws-properties-emrserverless-application-initialcapacityconfigkeyvaluepair-syntax.yaml"></a>

```
  [Key](#cfn-emrserverless-application-initialcapacityconfigkeyvaluepair-key): String
  [Value](#cfn-emrserverless-application-initialcapacityconfigkeyvaluepair-value): 
    InitialCapacityConfig
```

## Properties<a name="aws-properties-emrserverless-application-initialcapacityconfigkeyvaluepair-properties"></a>

`Key`  <a name="cfn-emrserverless-application-initialcapacityconfigkeyvaluepair-key"></a>
The worker type for an analytics framework\. For Spark applications, the key can either be set to `Driver` or `Executor`\. For Hive applications, it can be set to `HiveDriver` or `TezTask`\.  
*Minimum*: 1  
*Maximum*: 50  
*Pattern*: `^[a-zA-Z]+[-_]*[a-zA-Z]+$`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-emrserverless-application-initialcapacityconfigkeyvaluepair-value"></a>
The value for the initial capacity configuration per worker\.  
*Required*: Yes  
*Type*: [InitialCapacityConfig](aws-properties-emrserverless-application-initialcapacityconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)