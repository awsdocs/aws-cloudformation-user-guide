# AWS::Pipes::Pipe BatchEnvironmentVariable<a name="aws-properties-pipes-pipe-batchenvironmentvariable"></a>

The environment variables to send to the container\. You can add new environment variables, which are added to the container at launch, or you can override the existing environment variables from the Docker image or the task definition\.

**Note**  
Environment variables cannot start with "`AWS Batch`"\. This naming convention is reserved for variables that AWS Batch sets\.

## Syntax<a name="aws-properties-pipes-pipe-batchenvironmentvariable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-batchenvironmentvariable-syntax.json"></a>

```
{
  "[Name](#cfn-pipes-pipe-batchenvironmentvariable-name)" : String,
  "[Value](#cfn-pipes-pipe-batchenvironmentvariable-value)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-batchenvironmentvariable-syntax.yaml"></a>

```
  [Name](#cfn-pipes-pipe-batchenvironmentvariable-name): String
  [Value](#cfn-pipes-pipe-batchenvironmentvariable-value): String
```

## Properties<a name="aws-properties-pipes-pipe-batchenvironmentvariable-properties"></a>

`Name`  <a name="cfn-pipes-pipe-batchenvironmentvariable-name"></a>
The name of the key\-value pair\. For environment variables, this is the name of the environment variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-pipes-pipe-batchenvironmentvariable-value"></a>
The value of the key\-value pair\. For environment variables, this is the value of the environment variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)