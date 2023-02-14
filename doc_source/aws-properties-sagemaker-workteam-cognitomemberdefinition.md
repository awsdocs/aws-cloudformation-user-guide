# AWS::SageMaker::Workteam CognitoMemberDefinition<a name="aws-properties-sagemaker-workteam-cognitomemberdefinition"></a>

Identifies a Amazon Cognito user group\. A user group can be used in on or more work teams\.

## Syntax<a name="aws-properties-sagemaker-workteam-cognitomemberdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-workteam-cognitomemberdefinition-syntax.json"></a>

```
{
  "[CognitoClientId](#cfn-sagemaker-workteam-cognitomemberdefinition-cognitoclientid)" : String,
  "[CognitoUserGroup](#cfn-sagemaker-workteam-cognitomemberdefinition-cognitousergroup)" : String,
  "[CognitoUserPool](#cfn-sagemaker-workteam-cognitomemberdefinition-cognitouserpool)" : String
}
```

### YAML<a name="aws-properties-sagemaker-workteam-cognitomemberdefinition-syntax.yaml"></a>

```
  [CognitoClientId](#cfn-sagemaker-workteam-cognitomemberdefinition-cognitoclientid): String
  [CognitoUserGroup](#cfn-sagemaker-workteam-cognitomemberdefinition-cognitousergroup): String
  [CognitoUserPool](#cfn-sagemaker-workteam-cognitomemberdefinition-cognitouserpool): String
```

## Properties<a name="aws-properties-sagemaker-workteam-cognitomemberdefinition-properties"></a>

`CognitoClientId`  <a name="cfn-sagemaker-workteam-cognitomemberdefinition-cognitoclientid"></a>
An identifier for an application client\. You must create the app client ID using Amazon Cognito\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CognitoUserGroup`  <a name="cfn-sagemaker-workteam-cognitomemberdefinition-cognitousergroup"></a>
An identifier for a user group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CognitoUserPool`  <a name="cfn-sagemaker-workteam-cognitomemberdefinition-cognitouserpool"></a>
An identifier for a user pool\. The user pool must be in the same region as the service that you are calling\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)