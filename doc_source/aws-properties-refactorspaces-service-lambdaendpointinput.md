# AWS::RefactorSpaces::Service LambdaEndpointInput<a name="aws-properties-refactorspaces-service-lambdaendpointinput"></a>

The input for the AWS Lambda endpoint type\. 

## Syntax<a name="aws-properties-refactorspaces-service-lambdaendpointinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-refactorspaces-service-lambdaendpointinput-syntax.json"></a>

```
{
  "[Arn](#cfn-refactorspaces-service-lambdaendpointinput-arn)" : String
}
```

### YAML<a name="aws-properties-refactorspaces-service-lambdaendpointinput-syntax.yaml"></a>

```
  [Arn](#cfn-refactorspaces-service-lambdaendpointinput-arn): String
```

## Properties<a name="aws-properties-refactorspaces-service-lambdaendpointinput-properties"></a>

`Arn`  <a name="cfn-refactorspaces-service-lambdaendpointinput-arn"></a>
The Amazon Resource Name \(ARN\) of the Lambda function or alias\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)