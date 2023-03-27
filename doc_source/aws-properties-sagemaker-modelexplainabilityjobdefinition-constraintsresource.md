# AWS::SageMaker::ModelExplainabilityJobDefinition ConstraintsResource<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-constraintsresource"></a>

Input object for the endpoint

## Syntax<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-constraintsresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-constraintsresource-syntax.json"></a>

```
{
  "[S3Uri](#cfn-sagemaker-modelexplainabilityjobdefinition-constraintsresource-s3uri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-constraintsresource-syntax.yaml"></a>

```
  [S3Uri](#cfn-sagemaker-modelexplainabilityjobdefinition-constraintsresource-s3uri): String
```

## Properties<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-constraintsresource-properties"></a>

`S3Uri`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-constraintsresource-s3uri"></a>
The Amazon S3 URI for the constraints resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)