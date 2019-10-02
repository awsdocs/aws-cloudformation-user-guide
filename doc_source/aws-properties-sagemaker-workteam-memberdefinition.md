# AWS::SageMaker::Workteam MemberDefinition<a name="aws-properties-sagemaker-workteam-memberdefinition"></a>

Defines the Amazon Cognito user group that is part of a work team\.

## Syntax<a name="aws-properties-sagemaker-workteam-memberdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-workteam-memberdefinition-syntax.json"></a>

```
{
  "[CognitoMemberDefinition](#cfn-sagemaker-workteam-memberdefinition-cognitomemberdefinition)" : [CognitoMemberDefinition](aws-properties-sagemaker-workteam-cognitomemberdefinition.md)
}
```

### YAML<a name="aws-properties-sagemaker-workteam-memberdefinition-syntax.yaml"></a>

```
  [CognitoMemberDefinition](#cfn-sagemaker-workteam-memberdefinition-cognitomemberdefinition): 
    [CognitoMemberDefinition](aws-properties-sagemaker-workteam-cognitomemberdefinition.md)
```

## Properties<a name="aws-properties-sagemaker-workteam-memberdefinition-properties"></a>

`CognitoMemberDefinition`  <a name="cfn-sagemaker-workteam-memberdefinition-cognitomemberdefinition"></a>
The Amazon Cognito user group that is part of the work team\.  
*Required*: Yes  
*Type*: [CognitoMemberDefinition](aws-properties-sagemaker-workteam-cognitomemberdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-2`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
