# AWS::SSMIncidents::ResponsePlan SsmParameter<a name="aws-properties-ssmincidents-responseplan-ssmparameter"></a>

The key\-value pair parameters to use when running the automation document\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-ssmparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-ssmparameter-syntax.json"></a>

```
{
  "[Key](#cfn-ssmincidents-responseplan-ssmparameter-key)" : String,
  "[Values](#cfn-ssmincidents-responseplan-ssmparameter-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-ssmparameter-syntax.yaml"></a>

```
  [Key](#cfn-ssmincidents-responseplan-ssmparameter-key): String
  [Values](#cfn-ssmincidents-responseplan-ssmparameter-values): 
    - String
```

## Properties<a name="aws-properties-ssmincidents-responseplan-ssmparameter-properties"></a>

`Key`  <a name="cfn-ssmincidents-responseplan-ssmparameter-key"></a>
The key parameter to use when running the automation document\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-ssmincidents-responseplan-ssmparameter-values"></a>
The value parameter to use when running the automation document\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)