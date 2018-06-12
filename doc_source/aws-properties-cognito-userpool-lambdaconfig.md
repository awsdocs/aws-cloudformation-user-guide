# Amazon Cognito UserPool LambdaConfig<a name="aws-properties-cognito-userpool-lambdaconfig"></a>

`LambdaConfig` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the AWS Lambda configuration of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-lambdaconfig-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.json"></a>

```
{
  "[CreateAuthChallenge](#cfn-cognito-userpool-lambdaconfig-createauthchallenge)" : String,
  "[CustomMessage](#cfn-cognito-userpool-lambdaconfig-custommessage)" : String,
  "[DefineAuthChallenge](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge)" : String,
  "[PostAuthentication](#cfn-cognito-userpool-lambdaconfig-postauthentication)" : String,
  "[PostConfirmation](#cfn-cognito-userpool-lambdaconfig-postconfirmation)" : String,
  "[PreAuthentication](#cfn-cognito-userpool-lambdaconfig-preauthentication)" : String,
  "[PreSignUp](#cfn-cognito-userpool-lambdaconfig-presignup)" : String,
  "[VerifyAuthChallengeResponse](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-lambdaconfig-syntax.yaml"></a>

```
[CreateAuthChallenge](#cfn-cognito-userpool-lambdaconfig-createauthchallenge): String
[CustomMessage](#cfn-cognito-userpool-lambdaconfig-custommessage): String
[DefineAuthChallenge](#cfn-cognito-userpool-lambdaconfig-defineauthchallenge): String
[PostAuthentication](#cfn-cognito-userpool-lambdaconfig-postauthentication): String
[PostConfirmation](#cfn-cognito-userpool-lambdaconfig-postconfirmation): String
[PreAuthentication](#cfn-cognito-userpool-lambdaconfig-preauthentication): String
[PreSignUp](#cfn-cognito-userpool-lambdaconfig-presignup): String
[VerifyAuthChallengeResponse](#cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse): String
```

## Properties<a name="aws-properties-cognito-userpool-lambdaconfig-properties"></a>

`CreateAuthChallenge`  <a name="cfn-cognito-userpool-lambdaconfig-createauthchallenge"></a>
Creates an authentication challenge\.  
*Type*: String  
*Required*: No

`CustomMessage`  <a name="cfn-cognito-userpool-lambdaconfig-custommessage"></a>
A custom Message AWS Lambda trigger\.  
*Type*: String  
*Required*: No

`DefineAuthChallenge`  <a name="cfn-cognito-userpool-lambdaconfig-defineauthchallenge"></a>
Defines the authentication challenge\.  
*Type*: String  
*Required*: No

`PostAuthentication`  <a name="cfn-cognito-userpool-lambdaconfig-postauthentication"></a>
A post\-authentication AWS Lambda trigger\.  
*Type*: String  
*Required*: No

`PostConfirmation`  <a name="cfn-cognito-userpool-lambdaconfig-postconfirmation"></a>
A post\-confirmation AWS Lambda trigger\.  
*Type*: String  
*Required*: No

`PreAuthentication`  <a name="cfn-cognito-userpool-lambdaconfig-preauthentication"></a>
A pre\-authentication AWS Lambda trigger\.  
*Type*: String  
*Required*: No

`PreSignUp`  <a name="cfn-cognito-userpool-lambdaconfig-presignup"></a>
A pre\-registration AWS Lambda trigger\.  
*Type*: String  
*Required*: No

`VerifyAuthChallengeResponse`  <a name="cfn-cognito-userpool-lambdaconfig-verifyauthchallengeresponse"></a>
Verifies the authentication challenge response\.  
*Type*: String  
*Required*: No