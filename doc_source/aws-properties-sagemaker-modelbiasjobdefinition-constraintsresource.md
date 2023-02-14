# AWS::SageMaker::ModelBiasJobDefinition ConstraintsResource<a name="aws-properties-sagemaker-modelbiasjobdefinition-constraintsresource"></a>

The constraints resource for a monitoring job\.

## Syntax<a name="aws-properties-sagemaker-modelbiasjobdefinition-constraintsresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelbiasjobdefinition-constraintsresource-syntax.json"></a>

```
{
  "[S3Uri](#cfn-sagemaker-modelbiasjobdefinition-constraintsresource-s3uri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelbiasjobdefinition-constraintsresource-syntax.yaml"></a>

```
  [S3Uri](#cfn-sagemaker-modelbiasjobdefinition-constraintsresource-s3uri): String
```

## Properties<a name="aws-properties-sagemaker-modelbiasjobdefinition-constraintsresource-properties"></a>

`S3Uri`  <a name="cfn-sagemaker-modelbiasjobdefinition-constraintsresource-s3uri"></a>
The Amazon S3 URI for the constraints resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)