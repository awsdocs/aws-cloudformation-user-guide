# AWS::SageMaker::Workteam MemberDefinition<a name="aws-properties-sagemaker-workteam-memberdefinition"></a>

Defines an Amazon Cognito or your own OIDC IdP user group that is part of a work team\.

## Syntax<a name="aws-properties-sagemaker-workteam-memberdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-workteam-memberdefinition-syntax.json"></a>

```
{
  "[CognitoMemberDefinition](#cfn-sagemaker-workteam-memberdefinition-cognitomemberdefinition)" : CognitoMemberDefinition,
  "[OidcMemberDefinition](#cfn-sagemaker-workteam-memberdefinition-oidcmemberdefinition)" : OidcMemberDefinition
}
```

### YAML<a name="aws-properties-sagemaker-workteam-memberdefinition-syntax.yaml"></a>

```
  [CognitoMemberDefinition](#cfn-sagemaker-workteam-memberdefinition-cognitomemberdefinition): 
    CognitoMemberDefinition
  [OidcMemberDefinition](#cfn-sagemaker-workteam-memberdefinition-oidcmemberdefinition): 
    OidcMemberDefinition
```

## Properties<a name="aws-properties-sagemaker-workteam-memberdefinition-properties"></a>

`CognitoMemberDefinition`  <a name="cfn-sagemaker-workteam-memberdefinition-cognitomemberdefinition"></a>
The Amazon Cognito user group that is part of the work team\.  
*Required*: No  
*Type*: [CognitoMemberDefinition](aws-properties-sagemaker-workteam-cognitomemberdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OidcMemberDefinition`  <a name="cfn-sagemaker-workteam-memberdefinition-oidcmemberdefinition"></a>
A list user groups that exist in your OIDC Identity Provider \(IdP\)\. One to ten groups can be used to create a single private work team\. When you add a user group to the list of `Groups`, you can add that user group to one or more private work teams\. If you add a user group to a private work team, all workers in that user group are added to the work team\.  
*Required*: No  
*Type*: [OidcMemberDefinition](aws-properties-sagemaker-workteam-oidcmemberdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)