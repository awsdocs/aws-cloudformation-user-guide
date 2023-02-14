# AWS::ServiceCatalog::ServiceAction DefinitionParameter<a name="aws-properties-servicecatalog-serviceaction-definitionparameter"></a>

The list of parameters in JSON format\. For example: `[{\"Name\":\"InstanceId\",\"Type\":\"TARGET\"}] or [{\"Name\":\"InstanceId\",\"Type\":\"TEXT_VALUE\"}]`\.

## Syntax<a name="aws-properties-servicecatalog-serviceaction-definitionparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicecatalog-serviceaction-definitionparameter-syntax.json"></a>

```
{
  "[Key](#cfn-servicecatalog-serviceaction-definitionparameter-key)" : String,
  "[Value](#cfn-servicecatalog-serviceaction-definitionparameter-value)" : String
}
```

### YAML<a name="aws-properties-servicecatalog-serviceaction-definitionparameter-syntax.yaml"></a>

```
  [Key](#cfn-servicecatalog-serviceaction-definitionparameter-key): String
  [Value](#cfn-servicecatalog-serviceaction-definitionparameter-value): String
```

## Properties<a name="aws-properties-servicecatalog-serviceaction-definitionparameter-properties"></a>

`Key`  <a name="cfn-servicecatalog-serviceaction-definitionparameter-key"></a>
The parameter key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-servicecatalog-serviceaction-definitionparameter-value"></a>
The value of the parameter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)