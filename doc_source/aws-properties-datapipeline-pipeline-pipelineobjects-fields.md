# AWS Data Pipeline Pipeline Field<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields"></a>

Key\-value pairs that describe the properties of a [data pipeline object](aws-properties-datapipeline-pipeline-pipelineobjects.md)\.

## Syntax<a name="w3ab2c21c14d570b5"></a>

### JSON<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields-syntax.json"></a>

```
{
  "[Key](#cfn-datapipeline-pipeline-pipelineobjects-fields-key)" : String,
  "[RefValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-refvalue)" : String,
  "[StringValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-stringvalue)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-pipelineobjects-fields-syntax.yaml"></a>

```
[Key](#cfn-datapipeline-pipeline-pipelineobjects-fields-key): String
[RefValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-refvalue): String
[StringValue](#cfn-datapipeline-pipeline-pipelineobjects-fields-stringvalue): String
```

## Properties<a name="w3ab2c21c14d570b7"></a>

`Key`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields-key"></a>
Specifies the name of a field for a particular object\. To view fields for a data pipeline object, see [Pipeline Object Reference](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.  
*Required*: Yes  
*Type*: String

`RefValue`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields-refvalue"></a>
A field value that you specify as an identifier of another object in the same pipeline definition\.  
You can specify the field value as either a string value \(`StringValue`\) or a reference to another object \(`RefValue`\), but not both\.
*Required*: Conditional if the key that you are using requires it\.  
*Type*: String

`StringValue`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields-stringvalue"></a>
A field value that you specify as a string\. To view valid values for a particular field, see [Pipeline Object Reference](http://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/dp-pipeline-objects.html) in the *AWS Data Pipeline Developer Guide*\.  
You can specify the field value as either a string value \(`StringValue`\) or a reference to another object \(`RefValue`\), but not both\.
*Required*: Conditional if the key that you are using requires it\.  
*Type*: String