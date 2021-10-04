# AWS::DataBrew::Dataset JsonOptions<a name="aws-properties-databrew-dataset-jsonoptions"></a>

Represents the JSON\-specific options that define how input is to be interpreted by AWS Glue DataBrew\.

## Syntax<a name="aws-properties-databrew-dataset-jsonoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-jsonoptions-syntax.json"></a>

```
{
  "[MultiLine](#cfn-databrew-dataset-jsonoptions-multiline)" : Boolean
}
```

### YAML<a name="aws-properties-databrew-dataset-jsonoptions-syntax.yaml"></a>

```
  [MultiLine](#cfn-databrew-dataset-jsonoptions-multiline): Boolean
```

## Properties<a name="aws-properties-databrew-dataset-jsonoptions-properties"></a>

`MultiLine`  <a name="cfn-databrew-dataset-jsonoptions-multiline"></a>
A value that specifies whether JSON input contains embedded new line characters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)