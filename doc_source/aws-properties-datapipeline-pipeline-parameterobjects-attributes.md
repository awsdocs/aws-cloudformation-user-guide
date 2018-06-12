# AWS Data Pipeline Parameter Objects Attributes<a name="aws-properties-datapipeline-pipeline-parameterobjects-attributes"></a>

`Attribute` is a property of the [AWS Data Pipeline Pipeline ParameterObjects](aws-properties-datapipeline-pipeline-parameterobjects.md) property that defines the attributes of a parameter object as key\-value pairs\.

## Syntax<a name="w3ab2c21c14d558b5"></a>

### JSON<a name="aws-properties-datapipeline-pipeline-parameterobjects-attributes-syntax.json"></a>

```
{
  "[Key](#cfn-datapipeline-pipeline-parameterobjects-attribtues-key)" : String,
  "[StringValue](#cfn-datapipeline-pipeline-parameterobjects-attribtues-stringvalue)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-parameterobjects-attributes-syntax.yaml"></a>

```
[Key](#cfn-datapipeline-pipeline-parameterobjects-attribtues-key): String
[StringValue](#cfn-datapipeline-pipeline-parameterobjects-attribtues-stringvalue): String
```

## Properties<a name="w3ab2c21c14d558b7"></a>

`Key`  <a name="cfn-datapipeline-pipeline-parameterobjects-attribtues-key"></a>
Specifies the name of a parameter attribute\. To view parameter attributes, see [Creating a Pipeline Using Parameterized Templates](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-custom-templates.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: Yes  
*Type*: String

`StringValue`  <a name="cfn-datapipeline-pipeline-parameterobjects-attribtues-stringvalue"></a>
A parameter attribute value\.  
*Required*: Conditional if the key that you are using requires it\.  
*Type*: String