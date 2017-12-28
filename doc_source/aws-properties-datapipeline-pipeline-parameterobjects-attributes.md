# AWS Data Pipeline Parameter Objects Attributes<a name="aws-properties-datapipeline-pipeline-parameterobjects-attributes"></a>

`Attribute` is a property of the [AWS Data Pipeline Pipeline ParameterObjects](aws-properties-datapipeline-pipeline-parameterobjects.md) property that defines the attributes of a parameter object as key\-value pairs\.

## Syntax<a name="w3ab2c21c14d476b5"></a>

### JSON<a name="aws-properties-datapipeline-pipeline-parameterobjects-attributes-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-datapipeline-pipeline-parameterobjects-attribtues-key)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-datapipeline-pipeline-parameterobjects-attribtues-stringvalue)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-parameterobjects-attributes-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-datapipeline-pipeline-parameterobjects-attribtues-key): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-datapipeline-pipeline-parameterobjects-attribtues-stringvalue): String
```

## Properties<a name="w3ab2c21c14d476b7"></a>

`Key`  
Specifies the name of a parameter attribute\. To view parameter attributes, see [Creating a Pipeline Using Parameterized Templates](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-custom-templates.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required: *Yes  
*Type*: String

`StringValue`  
A parameter attribute value\.  
*Required: *Conditional if the key that you are using requires it\.  
*Type*: String