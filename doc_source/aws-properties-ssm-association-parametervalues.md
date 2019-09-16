# AWS::SSM::Association ParameterValues<a name="aws-properties-ssm-association-parametervalues"></a>

`ParameterValues` is a property of the [AWS::SSM::Association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-association.html) resource that specifies the parameters for the runtime configuration of the document\. 

## Syntax<a name="aws-properties-ssm-association-parametervalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-association-parametervalues-syntax.json"></a>

```
{
  "[ParameterValues](#cfn-ssm-association-parametervalues-parametervalues)" : [ [String](#aws-properties-ssm-association-parametervalues), ... ]
}
```

### YAML<a name="aws-properties-ssm-association-parametervalues-syntax.yaml"></a>

```
  [ParameterValues](#cfn-ssm-association-parametervalues-parametervalues): 
    - [String](#aws-properties-ssm-association-parametervalues)
```

## Properties<a name="aws-properties-ssm-association-parametervalues-properties"></a>

`ParameterValues`  <a name="cfn-ssm-association-parametervalues-parametervalues"></a>
The parameters for the runtime configuration of the document\.  
*Required*: Yes  
*Type*: [List](#aws-properties-ssm-association-parametervalues) of [String](#aws-properties-ssm-association-parametervalues)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)